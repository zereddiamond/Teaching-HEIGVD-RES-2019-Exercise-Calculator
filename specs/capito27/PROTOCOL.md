## Network calculation protocol definition.

 - transport protocol : TCP
 - server discovery : manual address, with port 1060 (free port according to [this](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#Registered_ports))
 - the client will initiate the connection
 
 
 
  1 The client will request if the server provides the network calculation protocol, providing a 32 bit nonce (in hexadecimal format) and the magic string "NetCalc".
 
  2 The server will reply with the nonce and a list of operation it provides, and the amount of parameters required by each. 
  
  3 The client with reply with an operation ID, followed by their parameters
  
  4 The server will either reply with the magic "OpOk", followed by the result of the operation if the operation requested was valid, or with the magic "OpKo" followed by the list of supported operations, if the operation requested was invalid or the argument count was wrong.
  
  5.a The server will wait for at least 10 seconds for a new operation request before timing out the client, and closing its connection.
  
  5.b The client will send a new operation request withing the next 10 seconds, otherwise the server may have closed the client's 
    
  - The client will ignore any unsolicited messages in that protocol
  - The server will ignore any request which doesn't provide a known nonce (IE an operation request with the connection step 1)
  - The client may send at any point a message "ConnClose" to close the connection
  - All communication will contain the nonce chosen by the client
  
The messages will be sent in JSON format.
  
## Communication example :

client : localhost (port 6665)
server: localhost (port 1060)

 - client -> server (initial greetings message)

```json
{
	"NetCalc": {
		"Nonce": "6041b310"
	}
}
```

 - server -> client (reply with supported operations)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"Operations": {
			"Addition": {
				"ID": 0,
				"Operands": 2
			},
			"Substraction": {
				"ID": 1,
				"Operands": 2
			},
			"Inversion": {
				"ID": 2,
				"Operands": 1
			},
			"Floor": {
				"ID": 3,
				"Operands": 1
			},
			"Max": {
				"ID": 4,
				"Operands": 2
			}
		}
	}
}
```

 - client -> server (request for a supported operation)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"Operation": 0,
		"0": "56",
		"1": "13.6"

	}
}
```

 - server -> client (reply with result)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"OpOk": "69.6"
	}
}
```
 -  client -> server (request for an unsupported operation within 10 seconds)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"Operation": 5,
		"0": "56",
		"1": "13.6"

	}
}
```

 - server -> client (reply with operation list)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"OpKo": {
			"Addition": {
				"ID": 0,
				"Operands": 2
			},
			"Substraction": {
				"ID": 1,
				"Operands": 2
			},
			"Inversion": {
				"ID": 2,
				"Operands": 1
			},
			"Floor": {
				"ID": 3,
				"Operands": 1
			},
			"Max": {
				"ID": 4,
				"Operands": 2
			}
		}
	}
}
```

 -  client -> server (request for a supported operation  with wrong argument count within 10 seconds)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"Operation": 0,
		"0": "56"

	}
}
```

 - server -> client (reply with operation list)

```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"OpKo": {
			"Addition": {
				"ID": 0,
				"Operands": 2
			},
			"Substraction": {
				"ID": 1,
				"Operands": 2
			},
			"Inversion": {
				"ID": 2,
				"Operands": 1
			},
			"Floor": {
				"ID": 3,
				"Operands": 1
			},
			"Max": {
				"ID": 4,
				"Operands": 2
			}
		}
	}
}
```

 - client -> server (request to close the connection)
 
 ```json
{
	"NetCalc": {
		"Nonce": "6041b310",
		"ConnClose" : 0
	}
}
```
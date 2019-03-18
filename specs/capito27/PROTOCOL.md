## Network calculation protocol definition.

 - transport protocol : TCP
 - server discovery : manual address, with port 1060 (free port according to [this](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#Registered_ports))
 - the client will initiate the connection
 
 
 
  1 The client will request if the server provides the network calculation protocol, providing a nonce and the magic string "NetCalc".
 
  2 The server will reply with the nonce and a list of operation it provides, and the amount of parameters required by each. 
  
  3 The client with reply with an operation ID, followed by their parameters
  
  4 The server will either reply with the magic "OpOk", followed by the result of the operation if the operation requested was valid, or with the magic "OpKo", if the operation requested was invalid.
  
  5.a The server will wait for at least 10 seconds for a new operation request before timing out the client, and closing its connection.
  
  5.b The client will send a new operation request withing the next 10 seconds, otherwise the server may have closed the client's 
  
  - The client will ignore any unsolicited messages in that protocol
  - The server will ignore any request which doesn't provide a known nonce (IE an operation request with the connection step 1)
  
  The messages will be wrapped in JSON.
  
  
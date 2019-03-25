# Transport protocol
We can use TCP/IP to ensure the connection between client and server.

# Connection to the server
The server will use une IP address given by Docker (like 127.17.0.2) and connect to the port 80 (for simplicity purpose)

# Enabling the connection
The first to open a new connection will be the client, this is logical because the server can't ask everybody in a given network if they want to use the app.

# Exchange type
the best way to exchange informations for a calculator would be to use json files.

# Receiving message
We need to parse the json.
If the receiver is the server, he do the calculation ased by the client and send a json back with the result.
If the receiver is the client, he parse the json and display the result.

# Syntax of the message
client:
{
	"Calculation": ""
}

server:
{
	"Calculation": "",
	"Result": "",
	"Error": ""
}

# Closing connection
The client close the connexion when the user close the app.
The server close the connexion after a given timeout.
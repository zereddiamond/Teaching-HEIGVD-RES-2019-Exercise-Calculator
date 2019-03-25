#Phase 1: definition of specs

##The transport protocol
The control protocol should be TCP.
##How to find the server
The client find the server by using his IP and the port 43252
##Who speaks first
The client speak first
##Message sequence
	Client initialize the connection
	Server ask for the operation and number
	Client is waiting for reponse
	Server answer client and take next one.

##What happends when the message is received
The message is parsed and we look in which part of the connexion we are in
	"Init" / "AskNumber" / "SendNumber" / "Result" / "Cancel"

##All messages should have this syntax
"Init" for Init (Client send)
"AskNumber" for AskNumber (Server response)
"SendNumber";"Number1";"Number2";"Operation" for SendNumber(Client answer)
"Result";"Value" for Result(Server answer)
"Cancel" For Cancel


If the client don't answer for 5minutes, the server send "Cancel"
Otherwise the client send Cancel when he have the result.
Cancel closes the connection.


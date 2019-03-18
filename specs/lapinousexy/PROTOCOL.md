# Protocol

## Questions
Transport protocol :
UDP

How does the client find the server (addresses and ports)? :
The port must be 5653.

Who speaks first? :
The client

What is the sequence of messages exchanged by the client and the server? :
1) The client send an UDP packets containing numbers and an operation.
2) The server compute the operation on the given numbers and send the result to the client.

What happens when a message is received from the other party? :
If the client is receiving a message but he didn't ask for a computation he ignore it.
And the server is always anwering message, but for both of them if the message doesn't respect the specification it's ignored.

What is the syntax of the messages? How we generate and parse them? :
Syntax : NUMBER1 OPERATION NUMBER2
The client is generating them with the user input, and the server is parsing the UDP packets.

Who closes the connection and when? :
The client when he receive the result.
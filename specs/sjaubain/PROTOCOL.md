## What transport protocol do we use?
TCP protocol
## How does the client find the server (addresses and ports)?
We choose an arbitrary port for the application
## Who speaks first?
The client
## What is the sequence of messages exchanged by the client and the server?
The operation synthax for the client and the response from the server
## What happens when a message is received from the other party?
??
## What is the syntax of the messages? How we generate and parse them?
[OP] [arg1] [arg2] where OP is ADD | SUB | MULT | DIV
## Who closes the connection and when?
The server when there are no more clients

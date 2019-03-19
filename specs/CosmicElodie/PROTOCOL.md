

What transport protocol do we use?
It's a client-server protocol -> TCP for Http

How does the client find the server (addresses and ports)?
He uses the bind command. 

Who speaks first?
the server 

What is the sequence of messages exchanged by the client and the server?
socket, bind, accept, read, write, close.

What happens when a message is received from the other party?

What is the syntax of the messages? How we generate and parse them?
With strings, I suppose.
Who closes the connection and when?

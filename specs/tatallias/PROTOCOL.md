1. What transport protocol do we use?
	TCP
2. How does the client find the server (addresses and ports)?
	The server will be at a static IP and port (10.0.0.1:2019)
3. Who speaks first?
	The client asks the server to open a connection
4. What is the sequence of messages exchanged by the client and the server?
	client -> server : Open connection
	server -> client : Connection opened
	client -> server : OK
	client -> server : Compute : 3 + 1
	server -> client : result : 3 + 1 = 4
	client -> server : Stop
	server -> client : Stopped
5. What happens when a message is received from the other party?
	Depending on the situation or the connection or the first token given
	the receiving party is respectively answering or waiting for a new query.
6. What is the syntax of the messages? How we generate and parse them?
	The message are in form of char buffers. the first token gives the general 
	command to be excecuted (open, compute, stop) or a approbation message 
	(connection, result, ok, stopped).
7. Who closes the connection and when?
	The client closes the connection once he doesn't need any more computing 
	from the server.
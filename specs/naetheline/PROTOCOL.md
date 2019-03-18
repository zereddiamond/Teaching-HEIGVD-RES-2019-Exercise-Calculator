# Specification for the protocol 

TODO mise en page !

##

We use TCP transprort protocol

The adress and port of the server are predetermined :
adress ip: 1234.12.34.1  port : 8987
-Server waits for a client to connect and send a calculation request.
-Once the calculation request send, the client wait for the server to answer.
-The client then print the answer of the server.
-Once the client has recieved the answer it submit a new calculation request or choose to close the connection.


##Format of the calculation request
Inverse Polish notation for the calculation


# Specification for the protocol 

TODO mise en page !

##

We use TCP transprort protocol

The adress and port of the server are predetermined (TODO : how ?)
adress ip: TODO  port : 8987
-Server waits for a client to connect and send a calculation request.
-Once the calculation request send, the client wait for the server to answer.
-The client the print the answer of the server.
-Once the client has recieved the answr it closes the connection.


##Format of the calculation request
Inverse Polish notation for the calculation

    What transport protocol do we use?
    How does the client find the server (addresses and ports)?
    Who speaks first?
    What is the sequence of messages exchanged by the client and the server?
    What happens when a message is received from the other party?
    What is the syntax of the messages? How we generate and parse them?
    Who closes the connection and when?
    Submit a PR

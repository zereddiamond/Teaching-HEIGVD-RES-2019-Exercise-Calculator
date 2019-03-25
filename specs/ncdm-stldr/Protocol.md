*What transport protocol do we use?
TCP.

*How does the client find the server (addresses and ports)?
The port could be hardcoded, and the adress is specified by the client who already knows the adress of the server.

*Who speaks first?
The client speaks first.

*What is the sequence of messages exchanged by the client and the server?
The client initiate a tcp connection with the server.
Once the connection is etablished, the client can submit a calculation. The server answer to say if he accept to perform the calculation.
When the server terminates, he notify the client by sending the answer.

*What happens when a message is received from the other party?
An error or ok message is sent back.

*What is the syntax of the messages? How we generate and parse them?
The message content is stored in xml format. A flag called calculation stores the calculation.

*Who closes the connection and when?
The client closes the connection when he doesn't need to submit calculation requests anymore.
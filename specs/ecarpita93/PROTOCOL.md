#What transport protocol do we use? 
TCP/IP

#How does the client find the server (addresses and ports)?
It makes a connection request on the server IP address and port (8080)

#Who speaks first?
The client

#What is the sequence of messages exchanged by the client and the server?
create a socket ->make a connection request via IP and port -> read and write bytes thought the socket (the "real" communication) 


#What happens when a message is received from the other party?
It's stored in a buffer to be treated

#What is the syntax of the messages? How we generate and parse them?
A stream of bytes, the last one is -1 so we know when stop the buffering


#Who closes the connection and when?
The client closes the socket when finished transmitting data
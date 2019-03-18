##My Protocol
#What transport protocol do we use?
We use TCP because it's a connexion-full protocol

#How does the client find the server (addresses and ports)?
The client find the server with his IP adress + listening port (also call the socket) e.g. 192.168.1.10:3333

#Who speaks first?
The client speaks first to open to connexion

#What is the sequence of messages exchanged by the client and the server?
 SYN SYN ACK ACK then datas

#What happens when a message is received from the other party?
We send an ACK to validate that we have received

#What is the syntax of the messages? How we generate and parse them?
 Syntaxe is SYN SYN-ACK ACK for the connexion and then DATA ACK

#Who closes the connection and when?
 Anyone can close the conenxion with a FIN and the other send ACK then FIN-ACK and the other one send ACK

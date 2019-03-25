What transport protocol do we use?
TCP

How does the client find the server (addresses and ports)?
IP_SERVER:80

Who speaks first?
The client

What is the sequence of messages exchanged by the client and the server?
SYN
SYN + ACK
ACK

What happens when a message is received from the other party?
It sends a confirmation to the other party.

What is the syntax of the messages? How we generate and parse them?
Head,From,To,Message
Parsed by ","

Who closes the connection and when?
The client, when the server has sent all of the bytes.
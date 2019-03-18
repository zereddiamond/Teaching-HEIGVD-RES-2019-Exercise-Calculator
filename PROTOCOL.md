1. TCP
2. Using a DNS (requesting the corresponding IP adress of the domain name)
3. The client
4. 	Client: Asking connection
	Server: ACK and Accept connection
	Client: ACK
	---
	DATA TRANSFER
	---
	Client: Close connection
	Server: ACK and prepare to close
	Client: ACK and close
	Server: Close
5. The other party send an acknowledge to confirm that the message has been recieved.
6. The message contains meta-data first, and the following byte are the rest of the message. We generate and parse them using conventional rules.
7. The server partially close the connection when the client asks to.


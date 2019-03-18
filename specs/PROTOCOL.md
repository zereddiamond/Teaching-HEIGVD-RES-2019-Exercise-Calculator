# Specification for Exercise-Calculator

## 1) Transport protocol used: 
TCP
## 2) Server's adresses and ports: 
port 80
## 3) Messages:
Client speaks first.

### Sequence of messages : 
	C : "HELLO SERVER"
	S : "HELLO CLIENT" + indicates if busy or ready to listen
	C : <message>
	S : <ACK>
	(repeat message-ack)
	C : "END CONNECTION"
	S : <ACK END CONNEĈTION>
The Server closes the connection when he receives the message "END 
CONNECTION" from Client.

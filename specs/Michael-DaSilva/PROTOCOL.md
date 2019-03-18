What transport protocol do we use?
How does the client find the server (addresses and ports)?
Who speaks first?
What is the sequence of messages exchanged by the client and the server?
What happens when a message is received from the other party?
What is the syntax of the messages? How we generate and parse them?
Who closes the connection and when?

##Exercise : Calculatrice
###What transport protocol do we use?  
We will be using the TCP protocol.
###How does the client find the server (addresses and ports)?
The client will find the server through the following fixed IP address and port: 
###Who speaks first?
The client will speak first. The server only wait until the client speak.
###What is the sequence of messages exchanged by the client and the server?
The client ask for a calcul to do by the server (ex: `calculate 1 + 2`).
###What happens when a message is received from the other party?
 The server answer the client's demand (ex: `The calcul 1 + 2 give the following answer: 3).
###What is the syntax of the messages? How we generate and parse them?
###Who closes the connection and when?
The client close the connection after a specific command is given (ex: `calculate stop`)
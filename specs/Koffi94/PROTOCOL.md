# My Client-Server Protocol

### What transport protocol do we use ?

It uses TCP as layer 4 because we full state connexion. The server should memorize some informations in the conversation.

### How does the client find the server (addresses and ports) ?

The client find the server with his IP adress + listening port (also call the socket).

The server will be in a Docker container so IP 172.17.0.x and listening on the port 12345

### Who speaks first?

The client speaks first to open to connexion.

### What is the sequence of messages exchanged by the client and the server?

| Client   | Server   |
| :------- | -------- |
| SYN      | -        |
| -        | SYN ACK  |
| ACK      | -        |
| Data     | -        |
| -        | Data ACK |
| -        | Data     |
| Data ACK | -        |
| etc      | etc      |

### What happens when a message is received from the other party?

Send back a Data ACK to inform that the message has been well received and then send the response.

### What is the syntax of the messages? How we generate and parse them?
The message could be a CSV. Generated with OpenCSV and parsed with Apache Commons CSV.

### Who closes the connection and when?
The server closes the connexion because the server compute (or not) the calculation asked by the client and then closes the connexion by sending a FIN.
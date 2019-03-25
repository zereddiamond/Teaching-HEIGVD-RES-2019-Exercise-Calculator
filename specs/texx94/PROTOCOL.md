# RES - Labo 3

## Exercise Calculator

### What transport protocol do we use?

I think I will use TCP.

### How does the client find the server (addresses and ports)?

The client must know the server IP and the port.

The IP will be choose by Docker but it will be like 172.17.0.?.

The port can be choose so I decide to use 8080.

### Who speaks first?

I think the client must be the first to talk.

### What is the sequence of messages exchanged by the client and the server?

+ Is server ready ?
+ Yes, I'am
+ How much is ... ?
+ ... is ... !
+ Thanks, I'm done.
+ Ciao!

### What happens when a message is received from the other party?

It have to reply somethings like "Roger, I do that".

### What is the syntax of the messages? How we generate and parse them?

I dont know and it's time ...

### Who closes the connection and when?

The server close the connection after the ACK of the client.
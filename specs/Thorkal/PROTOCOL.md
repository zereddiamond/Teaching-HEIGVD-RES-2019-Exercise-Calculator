# Exercise Calculator - Specification

## Tommy Gerardi

### What transport protocol do we use?

We use TCP

### How does the client find the server (addresses and ports)?

We give the client those informations

### Who speaks first?

The client

### What is the sequence of messages exchanged by the client and the server?

Client tries to connect to the server -> server responds -> if connection is successful client and server can start their business -> client and server close connection

### What happens when a message is received from the other party?

We read it and react accordingly

### What is the syntax of the messages? How we generate and parse them?

We use TCP syntax using writers and readers

### Who closes the connection and when?

The client or the server, depending on what we're trying to achieve (most likely the client though).


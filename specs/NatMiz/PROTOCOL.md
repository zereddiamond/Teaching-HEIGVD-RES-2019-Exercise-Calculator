## Client-sever protocol

# What transport protocol do we use ?
We use the TCP protocol.

# How does the client find the server (addresses and ports) ?
We use the port 80 and the addresse provided by Docker, for exemple 192.168.99.100.

# Who speak first ?
The client speaks first.

# What is the sequence of messages exchanged by the client and the server ?
Handshake protocol.

# What happens when a message is received from the other party ?
The message is processed and a response is sent.

# What is the syntax of the messages? How we generate and parse them ?
We use the xml syntax for the message and a xml parser to parse it.

# Who closes the connection and when ?
- The client when its task is done.
- The server when its task is done or when a problem occurs.

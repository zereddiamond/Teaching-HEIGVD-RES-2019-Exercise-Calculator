### What transport protocol do we use?

- TCP

### How does the client find the server (addresses and ports)?

- The ip and ports are fixed. Could use something like 1123 and the ip would be the one hosting the server.

### Who speaks first?

- The client tells the servers he needs something first

### What is the sequence of messages exchanged by the client and the server?

- Client: Hello?
- Server: What do you need?
- Client: I need a tea please.
- Server: Here is you tea.
- Client: Thanks, here is the money!
- Server: Your welcome. Need something else?
- Client: No its okay. Bye!
- Server: Bye!

### What happens when a message is received from the other party?

- A new connection is opened

### What is the syntax of the messages? How we generate and parse them?

- Json

### Who closes the connection and when?

- The server after the client says he's done.
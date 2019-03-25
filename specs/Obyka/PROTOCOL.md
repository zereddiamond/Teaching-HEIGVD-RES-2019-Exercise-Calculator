# Protocol draft
- What transport protocol do we use?

We will use UDP since no sync is really needed for sending and processing operations. 
- How does the client find the server (addresses and ports)?

We will specify a default port (>1024) in the documentation. The address is the service's host one.
- Who speaks first?

The client who needs an operation to be computed.
- What is the sequence of messages exchanged by the client and the server?

Client: Hello I need a calculus to be compute. Are you available ?
Server: (Yes I am, send it | No | No response)
Client: Here is my calculus: (send formatted calculus)
Server: Here is your answer (send formatted answer)
- What happens when a message is received from the other party?

Depending on the state they are, they will process it or reject it.
- What is the syntax of the messages? How we generate and parse them?

(Header (state of the message) | Data associated with the request)
- Who closes the connection and when?

The server closes the connection right after sending its answer. It allows to manage less socket at a time.

## Phase 1: write the specification

- What transport protocol do we use?

  TCP

- How does the client find the server (addresses and ports)?

  The client 

- Who speaks first?

  The client speaks first (the client sends a request, and the server returns a response).

- What is the sequence of messages exchanged by the client and the server?
  *client* open TCP connection
  *server* accept TCP connection
  *client*  send election name
  *server* look up election,  send candidate list
  *client*  selects a candidate, send candidate name 
  *server* add vote to candidate, send receipt
  *client* closes tcp connection
  

- What happens when a message is received from the other party?
  It will be analysed and process.

- What is the syntax of the messages? How we generate and parse them?

  yet to be define

- Who closes the connection and when?

  The client close the connection or the server with a timeout.

  


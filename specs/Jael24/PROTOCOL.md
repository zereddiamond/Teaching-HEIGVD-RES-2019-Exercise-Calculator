### Protocol

Here is the specification about my protocol:

1. What transport protocol do we use?

We use the **TCP** protocol

2. How does the client find the server (addresses and ports)?

The client find the server with the IP address of the server and port number 4444.

3. Who speaks first?

The client speak first

4. What is the sequence of messages exchanged by the client and the server?

The client send a SYN, the server answers with a SYNACK. Finally, the client confirm with an ACK.

5. What happens when a message is received from the other party?

We try to read the message.

6. What is the syntax of the messages? How we generate and parse them?

The messages are one line written and separate by an "end of line".

7.Who closes the connection and when?

The client closes the connection when he has received the information he wants.
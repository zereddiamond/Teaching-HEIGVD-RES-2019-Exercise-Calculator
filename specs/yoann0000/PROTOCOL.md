1. What transport protocol do we use?
client-server protocol - TCP

2. How does the client find the server (addresses and ports)?
fixed url for the server
random port

3. Who speaks first?
the server

4. What is the sequence of messages exchanged by the client and the server?
socket - bind - accept - read - write - close

5. What happens when a message is received from the other party?
reply if one is expected

6. What is the syntax of the messages? How we generate and parse them?
Strings?

7. Who closes the connection and when?
The user and whenever he wants
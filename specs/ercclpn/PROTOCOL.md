# PROTOCOL Specification
Author : Tran Eric
Date : 18.03.2019

1. What transport protocol do we use?
   We use the TCP protocol.

2. How does the client find the server (addresses and ports)?
3. Who speaks first?
   The client.

4. What is the sequence of messages exchanged by the client and the server?
   Instruction to calculate from the client.
   Computing and answer by the server to the client.
   
5. What happens when a message is received from the other party?
   The server store the message and the ip from the client. 

6. What is the syntax of the messages? How we generate and parse them?
   The syntax is "A" and "operator" and "B". It will be stored in a json file.

7. Who closes the connection and when?
   The server close the connection when the sequence of messages is done.

##Specification
#### What transport protocol do we use?

TCP-IP transport protocol will be used to make sure that all information is received from both side.

####How does the client find the server (addresses and ports)?

The client has the server ip  and the server port hard coded in his program. 

####Who speaks first?
Client will speak first because he want to calculate.

####What is the sequence of messages exchanged by the client and the server?
- Client : Can I send you a calculation? 
- Server : Respond yes or no. If no, server close connection. If yes, the server send the operation available on the calculator.
- Client : Send the calculation.
- Server : Calculate and return the response.
- Server : Ask if the client has received the answer
- Client : Answer yes or no. If no Server resend it.
- Server : If the client received the answer, I close the connection. 

####What happens when a message is received from the other party?
He analyzes the message to be able to process it.

####What is the syntax of the messages? How we generate and parse them?
TO BE DEFINED
####Who closes the connection and when?
Server if the client received the anwser or that he tried to send the answer several times without success

# RES - Exercice Calculator

Author : Julien Huguet



- What transport protocol do we use?
  - TCP/IP
- How does the client find the server (addresses and ports)?
  - With ip address 127.0.0.1 and port 80
- Who speaks first?
  - The client speaks first, it need to do a request to the server to create the connexion
- What is the sequence of messages exchanged by the client and the server?
  - SYN -> SYN/ACK -> ACK
- What happens when a message is received from the other party?
  - The party need to check the validity of the message before execution
  - Then the client display the request in a generated file
- What is the syntax of the messages? How we generate and parse them?
  - Type : String, need to be convert in INT for operation Format : (number1,number2, operation) one line, separate each value with a comma
- Who closes the connection and when?
  - The server close the connection when the client disconnect
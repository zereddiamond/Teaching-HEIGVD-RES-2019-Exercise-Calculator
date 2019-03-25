+ What transport protocol do we use?        
  We're using TCP protocol.
+ How does the client find the server (addresses and ports)?        
  + Server: 10.10.10.2        
  + Client: 10.10.10.3 - 10.10.10.254       
  + Submask: 255.255.255.0        
  + Port: 12000 
+ Who speaks first?     
  The server.
+ What is the sequence of messages exchanged by the client and the server?
  + GET
  + PUSH
  + BYE
+ What happens when a message is received from the other party?     
  We can send a ACK after eache operation
+ What is the syntax of the messages? How we generate and parse them?       
  **Not completed yet**
+ Who closes the connection and when?       
  The client, with the BYE command.
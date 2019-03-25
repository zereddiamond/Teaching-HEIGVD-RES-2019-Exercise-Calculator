What transport protocol do we use?   
    - TCP / IP

How does the client find the server (addresses and ports)?   
    - The client has the IP address and port (6666) of the server 

Who speaks first?   
    - The client

What is the sequence of messages exchanged by the client and the server?   
    - The client want to connect    
    - The server responds and allow the connection   
    - The client asks for calculation   
    - The serveur responds and send calculation

What happens when a message is received from the other party?   
    - Check of the connection and then treat the message

What is the syntax of the messages? How we generate and parse them?   
    - We use the command calcul with 3 parameters :   
        - Operand 1   
        - Operand 2   
        - Sign

Who closes the connection and when?   
    - The client
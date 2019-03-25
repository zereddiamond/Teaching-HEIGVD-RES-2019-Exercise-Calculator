What transport protocol do we use?
    TCP
How does the client find the server (addresses and ports)?
    With a broadcast
Who speaks first?
    The client
What is the sequence of messages exchanged by the client and the server?
    SYN - ACK - SYNACK - MSG - RESP - CLOSE - CLOSE
What happens when a message is received from the other party?
    It triggers an ACK that the message is indeed received
What is the syntax of the messages? How we generate and parse them?
    
Who closes the connection and when?
    The client closes the connection when it doesn't want any more information
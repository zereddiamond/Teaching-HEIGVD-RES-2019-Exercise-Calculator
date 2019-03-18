What transport protocol do we use?
    TCP.
How does the client find the server (addresses and ports)?
    10.0.0.10::1025
Who speaks first?
    Client.
What is the sequence of messages exchanged by the client and the server?
    Hello -> Hello,Ack -> Ask,Ack -> Answer,Ack -> ... -> Bye -> Bye,Ack.
What happens when a message is received from the other party?
    control syntax then send a answer and a Ack.
What is the syntax of the messages?
    How we generate and parse them? maybe with a XML syntax and we can use JDOM.
Who closes the connection and when?
    Client close the connection when he has the last( if we consider multiple question) answer.
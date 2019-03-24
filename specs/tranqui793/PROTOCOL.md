###### <center>PROTOCOL CALCULATRICE </center>
What transport protocol do we use?
TCP
How does the client find the server (addresses and ports)?
le client doit connaitre l'addresse du serveur sinon il peut pas se connecter

Who speaks first?
serveur 
What is the sequence of messages exchanged by the client and the server?
le client se connecte .
seveur:
ADD inf1 inf2
SUB inf1 inf2
MULT inf1 inf2
DIV inf1 inf2
client :
ADD 1 3 
serveur :
RESULT 
4 = 1 + 3
 PS : le client peut envoyer autant de commande ,une fois il a finis il envoie BYE piur quitter

What happens when a message is received from the other party?
identification du la commande et traitement de la reponse.
What is the syntax of the messages? How we generate and parse them?
Who closes the connection and when?
le client fermera la connection une fois il a finis .
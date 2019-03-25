<<<<<<< HEAD
## Exercice RES - protocol

#### A. Gabriel Catel Torres

- What transport protocol do we use?

  TCP est le plus approprié

  

- How does the client find the server (addresses and ports)?

  

- Who speaks first?

  C'est le client qui annonce au serveur qu'il souhaite se connecter

  

- What is the sequence of messages exchanged by the client and the server?

  



- What happens when a message is received from the other party?

  On vérifie la provencance du message, s'il vient de celui que l'on souhaitait, on le traite sinon on l'ignore

  

- What is the syntax of the messages? How we generate and parse them?

  

- Who closes the connection and when?

  C'est en général le client qui va fermer la connection, mais c'est possible que le serveur le fasse aussi
=======
1. Transport Protocol : TCP
2. For the IP it will depend on the host, the port won't be a reserved one so >1023, let's use 1337
3. The client speaks first in order to connect
4. The client send the calcul he wants to execute : CALCULATE x + y and the server replies with a RESULT z
5. Connection -> Connection aknowledgment -> CALCULATE -> RESULT -> end Connection
6. The message is treated and a reply is sent
7. CALCULATE | RESULT	(x,op,y)|(z) : the keyword is CALCULATE/RESULT. Value to calculate are x and y and op is the operation. 
8. The client closed the connection whenever he wants.
>>>>>>> 8a1abdd7b84538473d18a784e9ce51d40f1eeeb8

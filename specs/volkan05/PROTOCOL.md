### What transport protocol do we use ?

TCP

### How does the client find the server (addresses and ports) ?

En tapant une adresse ip comme 192.168.2.5 et le port 2020

### Who speaks first ?

Client

### What is the sequence of messages exchanged by the client and the server ?

Le client commence par envoyer un message, ici un calcul. Puis le serveur calcul et envoit la réponse

### What happens when a message is received from the other party ?

Si c'est le client qui reçoit, il peut renvoyer à nouveau un autre calcul. Si c'est le serveur, il doit traiter le message et renvoyer une réponse.

### What is the syntax of the messages? How we generate and parse them ? 

### Who closes the connection and when ?

Le client arrête la connexion lorsqu'il a terminé et le serveur fermera la connexion établie au départ.
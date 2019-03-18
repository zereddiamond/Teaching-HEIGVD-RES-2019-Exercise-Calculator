##Julien Benoit

###What transport protocol do we use?
On utilise TCP.
###How does the client find the server (addresses and ports)?
l'adresse ip et le port sont fixe (par exemple 192.168.10.10 et le port 1010)
###Who speaks first?
le client.

###What is the sequence of messages exchanged by the client and the server?
le client essaie de se connecter au serveur, puis le serveur réponds, des que la connection est établie et qu'ils ont pu communiquer la connection se termine finalement.

###What happens when a message is received from the other party?


###What is the syntax of the messages? How we generate and parse them?

###Who closes the connection and when?
cela dépend, mais en général le client décide d'arreter et le serveur ferme la connection.
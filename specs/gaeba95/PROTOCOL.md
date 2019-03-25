# What transport protocol do we use?

Nous allons utiliser le protocol TCP.

# How does the client find the server (addresses and ports)?

Le client communiquera avec le serveur au travers du protocol TCP. Il lui faudra donc l'adresse ip du serveur et du port ouvert à la communication. Il envera une requête de connexion à cette adresse et port. Si il reçois une réponse positive, il pourra communiquer. Il communiquera sur le port 420.

# Who speaks first?

Le client parlera en premier. Il enverra une requete de connexion au serveur pour pouvoir communiquer.

# What is the sequence of messages exchanged by the client and the server?



# What happens when a message is received from the other party?



# What is the syntax of the messages? How we generate and parse them?



# Who closes the connection and when?

C'est le client qui ferme la connexion quand il a fini de communiquer avec le serveur.
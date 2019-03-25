# Spécifications
## Protocole de transport
TCP, car on veut s'assurer que le client puisse toujours recevoir une réponse , a moins que le serveur soit hors connexion. De plus, nous voulons nous assurer que le calcul du client soit fait dans l'ordre et avec tous les opérandes, ce qui n'est pas assuré par UDP.
## Adresses et ports
Nous partons du principe que l'adresse et le port du serveur sont passé au client par argument lors de l'appel du programme client. Le port du serveur est 8080. Par contre son adresse ip peut varié.
## Cycle
Le client commence par récupérer l'adresse et le port du serveur grace aux argument. Il crée une requete contenant l'opération a effectuer , et tente d'abord de se connecter au serveur, par l'envoi d'un message de test.
Lorsque le serveur reçoit le message de test, il répond par un autre message de test, affirmant ainsi qu'il est prêt a communiquer avec le client. Le client envoie alors sa requete, qui est traitée par le serveur. Une fois la requete traiter , le serveur renvoit le resultat au client, qui une fois le resultat obtenu, clôt la connexion.
## Forme du message
Le formatage de l'opération peut s'effectuer de différentes manières. Ici, l'opération est passé sous la forme d'une chaine de caractère ou chaque membre de l'opération est séparé par un espace. Le traitement de l'opération est laissé au serveur.

# Exercise calculator

## Phase 1

### What transport protocol do we use ?

Nous allons utilisé le protocole TCP car pour chaque commande que nous allons envoyé au serveur nous devons recevoir la réponse au client du résultat

### How does the client find the server (addresses and ports) ?

### Who speak first ?

Le serveur va parler en premier lorsque l'on va se connecter dessus. Il va nous envoyé les différent commande que l'on peut faire

### What is the sequence of messages exchanged by the client and the server

Server		Client

init		-> 	list

calc		<-	calc	

resul	->	resul

### What happens when a message is received from the other party ?

Du coté client on recevera au tout début la liste de commande que l'on peut faire. Et par la suite le resultat des opération qu'il aura fait

### What is the syntax of the messages ? How we generate and parse them ?

Pour la syntaxe du message nous pouvons avoir ça :

- Addition : **add nbr1 nbr2** --> nbr1 + nbr2
- Soustraction : **sub nbr1 nbr2** --> nbr1 - nbr2
- Division : **div nbr1 nbr2** -->  nbr1 / nbr2
- Multiplication : **mult nbr1 nbr2** --> nbr1 * nbr2



Les messages seront envoyé en json

###  Who closes the connection and when?

Le client va quitter la connection quand il va faire la command quit. LE serveur quand il recevera cette commande sera qu'il devra quitter la connection
# Protocol client-serveur pour calculatrice

## Spécifications
Le protocole implémentera TCP/IP.
Le serveur sera accessible via le port 1060 à son adresse.

## Exemple de communication

1. Le client sera le premier à parler, afin de s'annoncer au serveur.
2. Le serveur répond au client, afin d'annoncer qu'il est prêt à recevoir des requêtes, et informe des opérandes qu'il connaient, ainsi que leur symbol.
3. Le client peut maintenant envoyer un calcul
4. Le serveur envoie la réponse, ou l'éventuelle erreur engendrée
5. Retour au point 3. autant de fois que le client le souhaite
6. Le client termine la communication

## Syntaxe d'une requête type

Le message de requête devra contenir une liste de nombres, ainsi qu'une liste d'opérations.
Cela permettra ensuite au serveur de résoudre le calcule en notation polonaise inverse.

```json
{
    "request": {
        "numbers": [1, 2, 3],
        "operands": ['*', '/']
    }
}
```

Le serveur répond à une requête en envoyant le résultat, ou l'erreur correspondante.

```json
{
    "response": {
        "message": "ok",
        "value": 6
    }
}
```

# Protocol de communication client-server pour une calculatrice

Le serveur sera disponible sur le port 1100 en TCP/IP à l'adresse du serveur `jzaehrin.xyz`.

La communication se fera sous forme de structure JSON.

## Sequence

1. Le serveur commence par notifié sa présence et son attente d'une demande. `{"response":"Hello"}`
2. Le client peut alors envoyé une première requête demandant une première operation, la calculatrice sera en polonaise inverse.
    C'est différente opération permetteront à l'utilisateur de modifié l'état de la calculatrice.

```json
{
    "request": { 
        "operation" : <string>,
        "value" : <number>
    }
}
```

3. Le serveur founira un `ACK` quand l'operation est un success avec potentiellement un payload contenant un resultat, ou un `NACK` en cas d'erreur avec un payload d'information.

```json
{
    "reponse" : {
        "type" : <ACK, NACK>,
        "message" : <string>,
        "value" : <number>
    }
}
```

4. 

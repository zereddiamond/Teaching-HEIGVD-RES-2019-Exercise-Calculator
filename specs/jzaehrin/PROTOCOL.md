# Protocol de communication client-server pour une calculatrice

Le serveur sera disponible sur le port 1100 en TCP/IP à l'adresse du serveur `jzaehrin.xyz`.

La communication se donnera par des champs séparer de tab.

## Sequence

1. Le serveur commence par notifié sa présence, son et son attente d'une demande. `HELLO\t<operations>:\t[<operation>\t]+`
2. Le client peut maintenant envoyé une liste d'operand/operation de type polonaise inverse,
    c'est à dire que les nombres seront empilés et dépilés deux par deux lors de l'arrivé d'une operation. `REQUEST\t<operand>\t<operand>\t<operation>`
    Ce schema permet d'être extensible à plusieurs opérations concecutives. Le resultat sera empilé.
3. Le serveur renvoi la première valeur de la pile. `ACK\t<result>`
    1. Si une erreur est rencontré, le serveur repondra `NACK\t<message d'erreur>`
4. Le cycle recommence à partir du point `2`
    1. Si le client souhaite stoppé la connection, il coupe le canal. Le serveur attendra un timeout.

# Teaching-HEIGVD-RES-2019-Exercise-Calculator
### Author Bruno Legrand

* What transport protocol do we use?


        We should use TCP-IP protocole transport to guarantee  request and responce to be send


* How does the client find the server (addresses and ports)?

        server address could be static as well as the port. For example server address 10.192.105.200, port 3333

  
* Who speaks first?

        Client speaks first to establish connection and send request.


* What is the sequence of messages exchanged by the client and the server?

        * Client send resquest calculus
        * Server send answer calculus


* What happens when a message is received from the other party?

        Server recieve message from client :
        * client message is well formed, server send answer calculus
        * client message is not well formed, server send error message
        Client recieve message from server : 
        * if message is a responce well formed for a previous request, client accept message
        * client send error message


* What is the syntax of the messages? How we generate and parse them?

        syntaxe could be in XML 
        [<calcul request> | <result calculus>]

* Who closes the connection and when?

        * Client can close connection on user demand
        * Client can close connection if timer is over
        * Server can close connection if timer is over


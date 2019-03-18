# Lab Calculator

## Part 1 


1. We want to use TCP to be sure that packets are not lost
2. We will give the adresse and port of the server to the client with argument for exemple
3. It will be the client that will speak first. The server will wait for a connection from a client
4. The client will send the calcul and the server will parse the string received and find operators and numbers
5. We will check that the data are correct, no letters for exemple
6. We are going to send a String like: "Number operator number operator" ... We will have a list of operator and number and we will test each char to see if the order is correct and if char is an operator or a number
7. The client will close the connection when he's done

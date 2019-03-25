# Protocol for Calculator Exercise

## What transport protocol do we use?
We will use TCP.

## How does the client find the server (addresses and ports)?

## Who speaks first?
The client will speak first to request a caclculation.

## What is the sequence of messages exchanged by the client and the server?
client : I want a calculation computed.
server : What is your request ?
The client will send his request to the server. 
The server will send the result and will ask if the client has another request. 
The client will send another request or will close the connection.

## What happens when a message is received from the other party?


## What is the syntax of the messages? How we generate and parse them?


## Who closes the connection and when?
The client closes the connection when he does not have any more request.
## What transport protocol do we use?
We are going to use a TCP/IP protocol

## How does the client find the server (addresses and ports)?
The client finds the server with a given port (2554).

## Who speaks first?
The client speaks first.


## What is the sequence of messages exchanged by the client and the server?
1. Client asks for a connection
2. Server responds with a welcome message
3. Client asks for an operation
4. Server responds with a result 

## What happens when a message is received from the other party?
The party concerned looks up the message and checks what part of the conversation he is in.

## What is the syntax of the messages? How we generate and parse them?

The syntax should be simple as we need to communicate between a client and a server. Therefore, we are going to use an internationnal syntax for the client part that we are going to parse with commas.
Dots will be used for double and floatiing values. 

## Who closes the connection and when?
The client.


# Protocol

## What transport protocol do we use?
We use TCP protocol.

## How does the client find the server (addresses and ports)?
Ip no idea ????
Port : 9000

## Who speaks first?
The client

## What is the sequence of messages exchanged by the client and the server?
1. Client establish connection
2. Server accept connection
3. Client request a computation
4. Server respond with computation result
5. Server asks if client want another computation
6 Client respond
6.1 client then gives another computation
6.2 client says quit to finish exchange 
	 

## What happens when a message is received from the other party?
Other party aknowledge to have receive the message.

## What is the syntax of the messages? How we generate and parse them?
Messages are encoded in UTF-8.

Classical math notation is used with some functions :

log(x)

sqrt(x)

pow(x,y)

eg: 1 + 5 + sqrt(2) / 2

## Who closes the connection and when?
Client closes connection by saying quit

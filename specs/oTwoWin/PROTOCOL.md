# Specification

## Protocol used

TPC/IP

## How does the client find the server (addressess and port ? )

The server has a fixed address and port and the client has the address hard coded.

Port 6789.

## Who speaks first ?

The client speaks first to the server

## What is the sequence of messages exchanged by the client and the server?

1. The client asks for calculation
2. The server answer that he's avaible or not 
3. If the server is not avaible wait a random time and repeat step 1
4. Else send the calculation to be done
5. The server send the response of the calculation
6. The client can repeat step 1

## What happens when a message is received from the other party?

The party check the state of the conversation to defined what is going to do

## What is the syntax of the messages? How we generate and parse them?

The syntax must be like this

- Number
- Operand
- Number

We can use the Java String Class to generate them.



## Who closes the connection and when?

The client closes the connection when he has finished or he the server can closes the connection after a time without communicating. 


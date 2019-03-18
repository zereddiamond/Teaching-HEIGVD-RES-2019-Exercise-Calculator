# Specifications about a calculator protocol
## Ports and protocol

We'll use TCP because we want to make sure the calculation is correctly received and that is a stateful comm.

The server will listen on port 20000 the client requests, the client have to know the server address.
## Who speaks first ?

The client will send an INIT request

The server will send a LIST of options in response in which it has the calculations he can do
## Sequence
Client			Server
INIT 		->	
		<-	LIST
CALCULATE	->	
		<-	RESULT
FINISH		->	

## Message received
We'll check the syntax of the req and check for the syntax. If ok we'll continue the communication, If not we'll send a RESEND req, max : 3 RESEND.

## Syntax
The syntax of the requests will be XML as it's not dificult to parse.
<CalculatorProt>
	<client ip="192.168.0.1">
		<reqType id="INIT" />
	</client>
</CalculatorProt>


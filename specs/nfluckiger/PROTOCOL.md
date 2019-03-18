*What transport protocol do we use?
The transport protocol we use is TCP

*How does the client find the server (addresses and ports)?
They are in a properties file. The port use by the server is the 4666

*Who speaks first?
The client speaks first

*What is the sequence of messages exchanged by the client and the server?
The client ask for a calculation and then the server return the result

*What happens when a message is received from the other party?
The server compute the calculation
The client has no reaction

*What is the syntax of the messages? How we generate and parse them?
The message are JSON request with data set this way
	{
		calculation:{
			OPERATION:'x',
			OPERANDEONE:'x'(can be a calculation)
			OPERANDETWO:'y'(can be a calculation)
		}
	}
	
*Who closes the connection and when?
After an anwser the server closes the connection.
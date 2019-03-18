 ### specification:

 #### What transport protocol do we use?

	TCP

 #### How does the client find the server (addresses an ports)?

	il doit le savoir, le port 2234


 #### Who speaks first?

	le client
 #### What is the sequence of messages exchanged by the client and the server?
> 	c>hello
> 	s>hello
> 	c>calcule 
> 	s>resultat or "calcule imposible"
> 	c>exit

  #### What happens when a message is received from the other party?

	start a new server.
  #### What is the syntax of the messages? How we generate and parse them?

	<operator>mull</operator>
	<oprand>3</operand>
	<oprand>4</operand>
  #### Who closes the connection and when?

	le client quand il a fini





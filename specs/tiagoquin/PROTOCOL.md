# Spécifications

* What transport protocol do we use?

  TCP

* How does the client find the server (addresses and ports)?

  Address: The address of the docker

  Port: 8080

* Who speaks first?

  The client

* What is the sequence of messages exchanged by the client and the server?

  ```sequence
  Alice->Bob:
  
  ```

* What happens when a message is received from the other party?

* What is the syntax of the messages? How we generate and parse them?

  * calc [op] [var1] [var2]

* Who closes the connection and when?

  * The client in general case
  * The server in case of a Timeout
  * The server if an error occurred
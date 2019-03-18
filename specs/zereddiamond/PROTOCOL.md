## Protocol of zereddiamond

1. The transport protocol that we use is TCP. It is better than UDP,
and the connexion between client and server is guaranteed.

2. The client makes a socket with address 127.0.0.1 or with server's IP address.
The port will be 8384.

3. The server is on and in listening mode. The client sends a
 request to the server.

4. SYN, SYN+ACK, ACK (TCP protocol), client sends the operation,
the server solves calculation and sends response to the client.

5. The client simply displays the response in a file.

6. Format :  <firstNumber> + <lastNumbrer> (Separate with spaces).
The user write in a terminal, the operation will write in a file,
sends to the server. The server reads files and appends the responses
in the file and sends to the clients that reads this file.

7. Connexion closed by the client at the end of the operation.  

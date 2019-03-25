## Protocol of zereddiamond

1. The transport protocol that we use is TCP. It is better than UDP,
and the connexion between client and server is guaranteed. And finally it is easier to manage than UDP with Java.

2. The client can etablish a connection with the server thanks to a socket
with the server's IP address and the port 8384.

3. The server is on and in listening mode. The client sends a
 request to the server. So the client speaks first.

4. After to etablish a TCP connection, the client enters and sends
in a file to the server the operation. The server reads and splits 
the file and sends in a file the answer.

5. The client simply reads and displays the answer in a terminal

6. Format :  <first number> <last number> <operande> (separate with spaces and
like the reverse polish notation).
Format for the answer : <first number> <operande> <last number> = <answer>

7. Connexion closed by the client at the end of the operation.

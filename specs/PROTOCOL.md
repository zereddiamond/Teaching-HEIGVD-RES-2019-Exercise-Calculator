1. Transport Protocol : TCP
2. For the IP it will depend on the host, the port won't be a reserved one so >1023, let's use 1337
3. The client speaks first in order to connect
4. The client send the calcul he wants to execute : CALCULATE x + y and the server replies with a RESULT z
5. Connection -> Connection aknowledgment -> CALCULATE -> RESULT -> end Connection
6. The message is treated and a reply is sent
7. CALCULATE | RESULT	(x,op,y)|(z) : the keyword is CALCULATE/RESULT. Value to calculate are x and y and op is the operation. 
8. The client closed the connection whenever he wants.

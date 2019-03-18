1. Transport protocol: TCP
2. For the IP it will depend on the host, for the port we can choose one for the protocol, let's say 6789.
3. The client must first establish the connection and send the computation he wants the server to execute.
4. The client send a COMPUTE message followed by the computation, e.g. COMPUTE 1 + 1. This is the data part of the TCP payload. The server replies with a RESULT message followed by the result, e.g. RESULT 2.
5. The connection is closed by the client.
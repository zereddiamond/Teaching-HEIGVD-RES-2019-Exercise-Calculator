1. Transport protocol: TCP
2. For the IP it will depend on the host, for the port we can choose one for the protocol, let's say 6789.
3. The client must first establish the TCP connection and send the computation he wants the server to execute.
4. The client send a COMPUTE_X message followed by the computation, e.g. COMPUTE_1 1 + 1. Here X represents an ID to identify the computation. This is the data part of the TCP payload. The server then replies with a RESULT_X message followed by the result, e.g. RESULT_1 2. The same id must be used. This way, the client can send multiple computations and wait for the server to compute them and return the results.
6. The connection is closed by the client.

We could also produce a version for UDP.
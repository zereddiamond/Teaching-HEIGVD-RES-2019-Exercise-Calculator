### Protocol specifications

1. TCP/IP
2. The IP is defined by the server owner. The default port is 1234
3. The client ask the server for a computation
4. The client sends a request to the server with the compute datas. Then the server reply with the compute result.
5. The server starts  to compute. The client read the response and use it. 
6. The message is send serialized in JSON. The object contains three fields: operation, val1, val2. 
7. Once the client has received the answers.
<div style="text-align: right">Nathan Séville<div>

# Specification

> - What transport protocol do we use?

TCP

> - How does the client find the server (addresses and ports)?

In the documentation.

> - Who speaks first?

The client

> - What is the sequence of messages exchanged by the client and the server?

The client send a calculation request. The server replies with the result if accepted or deny the request.

> - What happens when a message is received from the other party?

The message is processed. The client read the result. The server compute the operation.

> - What is the syntax of the messages? How we generate and parse them?

JSON is used for the messages. Content: `Value1, Value2, Operation, Result`, `Result` attribute is only for the response from the server.

> - Who closes the connection and when?

The client close the connection or the server with a timeout.
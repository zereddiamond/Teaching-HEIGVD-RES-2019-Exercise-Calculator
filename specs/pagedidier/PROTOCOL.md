# Teaching-HEIGVD-RES-2019-Exercise-Calculator
> Didier Page

---

## Design

- What transport protocol do we use?

  TCP

- How does the client find the server (addresses and ports)?

  localhost:3000, We can imagine pass them as arguments to the executable file or in the environnment varable

- Who speaks first?

  The client init the connection, if the server is running

- What is the sequence of messages exchanged by the client and the server?

  The client send his data parsed and the server returns an acknowledge berfore he returns the result of the treatment

- What happens when a message is received from the other party?

  He's directly treated if the part is not to busy

- What is the syntax of the messages? How we generate and parse them?

  The message is passed in a json format

- Who closes the connection and when?

  The client when he doesn't need anymore the server
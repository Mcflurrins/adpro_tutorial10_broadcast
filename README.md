# Advanced Programming Module 10
## Reflection

### Experiment 2.1:

#### Running the server
![alt text](image.png)

#### Running client 1
![alt text](image-1.png)

#### Running client 2
![alt text](image-2.png)

#### Running client 3
![alt text](image-3.png)

To run this code, I open four terminals first. Then I put in `cargo run --bin server` in one terminal and `cargo run --bin client` in 3 terminals. I type 'hello' or 'hi' from each of the client terminals. The server listens for incoming TCP connections, upgrades them to websocket connections, and uses a broadcast channel to pass on messages from any client to all the clients.

### Experiment 2.2:
In the server, I changed the port to `TcpListener::bind("127.0.0.1:8080")`, and in the client, the connection URI I changed to `ws://127.0.0.1:8080`. The protocol is specified by the ws:// prefix in the URI, which both sides use for WebSocket communication. We just have to make sure both files already match in the port and protocol.
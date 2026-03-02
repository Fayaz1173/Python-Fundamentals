# Socket Programming

## 1. What is Socket Programming?

Socket programming allows two devices to communicate over a network using endpoints called **sockets**.

A socket is defined by:

- IP Address
- Port Number
- Protocol (TCP or UDP)

---

## 2. Basic Networking Concepts

### IP Address

Identifies a device on a network.

Example: `127.0.0.1` (localhost)

### Port Number

Identifies a specific application or service on a device.

Examples:

- 80 → HTTP
- 443 → HTTPS
- 22 → SSH

A connection is represented as:

```
(IP Address, Port)
```

---

## 3. Types of Protocols

### TCP (Transmission Control Protocol)

- Connection-oriented
- Reliable
- Ordered data delivery
- Used for web, email, file transfer

Python type:

```
socket.SOCK_STREAM
```

### UDP (User Datagram Protocol)

- Connectionless
- Faster
- No guarantee of delivery
- Used in streaming, gaming

Python type:

```
socket.SOCK_DGRAM
```

---

## 4. Client–Server Architecture

### Server

- Waits for incoming connections
- Listens on a specific port

### Client

- Connects to the server
- Sends and receives data

Flow:

```
Client → Server
Client ← Server
```

---

## 5. Steps to Create a TCP Server

1. Import socket module
2. Create a socket
3. Bind IP and port
4. Listen for connections
5. Accept client
6. Receive and send data
7. Close connection

# Client and Server (Socket Programing)

## Server side

```python
import socket

HOST = "127.0.0.1"
PORT = 5000

server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

server.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)

server.bind((HOST, PORT))
server.listen(1)

print(f"Server running on {HOST}:{PORT}")
print("Waiting for connection...")

conn, addr = server.accept()
print("Connected by:", addr)

while True:
    data = conn.recv(1024)

    if not data:
        break

    message = data.decode()
    print("Client:", message)

    if message.lower() == "exit":
        break

    reply = input("Server: ")
    conn.send(reply.encode())

    if reply.lower() == "exit":
        break

conn.close()
server.close()
print("Server closed.")
```

## Client side

```python
import socket

HOST = "127.0.0.1"
PORT = 5000

client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

client.connect((HOST, PORT))
print("Connected to server.")

while True:
    message = input("Client: ")
    client.send(message.encode())

    if message.lower() == "exit":
        break

    data = client.recv(1024)
    print("Server:", data.decode())

    if data.decode().lower() == "exit":
        break

client.close()
print("Connection closed.")
```

# What This Program Does

- Uses **TCP (SOCK_STREAM)**
- Allows two-way communication
- Stops when either side types `exit`
- Uses `encode()` and `decode()` properly
- Handles clean socket shutdown

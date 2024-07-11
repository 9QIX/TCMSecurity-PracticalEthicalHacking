# Introduction to Sockets in Python

## Overview

- Final module focusing on sockets
- Sockets used to connect nodes and reach out to IP addresses and ports
- Important for port scanning and exploit development

## Basic Socket Script

1. Create a file named `s.py` (avoid naming it `socket.py`)
2. Import the socket module
3. Define variables:
   - `host = "127.0.0.1"` (localhost)
   - `port = 7777` (or any desired port)
   - `s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)`
     - `AF_INET`: IPv4 connection
     - `SOCK_STREAM`: Port
4. Establish connection: `s.connect((host, port))`

## Demonstration

- Use `netcat` to listen on the specified port
- Run the Python script to establish a connection
- Connection is made and immediately closed

## Key Points

- Sockets connect one node to another
- This basic script only establishes a connection without further actions
- Forms the foundation for more complex scripts like port scanners

## Next Steps

- Building a simple port scanner in the next lesson

## `Socket.py`

```python
#!/usr/bin/env python3

# Import the socket module
import socket

# Define the server's hostname or IP address and the port to connect to
HOST = '127.0.0.1'
PORT = 7777

# Create a TCP/IP socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # AF_INET specifies IPv4, SOCK_STREAM specifies a TCP connection

try:
    # Connect the socket to the specified server and port
    s.connect((HOST, PORT))
    print(f"Connected to {HOST} on port {PORT}")
except ConnectionError as e:
    # Handle connection errors
    print(f"Failed to connect to {HOST} on port {PORT}: {e}")
finally:
    # Always close the socket after use
    s.close()

```

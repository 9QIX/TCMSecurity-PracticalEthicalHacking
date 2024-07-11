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

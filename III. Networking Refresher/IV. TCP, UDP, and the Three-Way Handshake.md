# TCP, UDP, and the Three-Way Handshake

## Layer 4 Networking Overview

### Introduction to Layer 4

- Focus on the Transport Layer of the OSI model.
- Discussing TCP (Transmission Control Protocol) and UDP (User Datagram Protocol).

### TCP vs. UDP

- **TCP:**
  - Stands for Transmission Control Protocol.
  - Connection-oriented protocol.
  - High reliability (e.g., HTTP, HTTPS, SSH, FTP).
- **UDP:**
  - Stands for User Datagram Protocol.
  - Connectionless protocol.
  - Used for streaming services, DNS, Voice over IP.

### Importance of TCP and UDP in Scanning

- Scanning both TCP and UDP is essential for penetration testers.
- Understanding TCP and UDP helps in defining scanning strategies.

### TCP Three-Way Handshake

- TCP uses a three-way handshake for connection establishment:
  - **SYN packet:** Initiates connection.
  - **SYN-ACK packet:** Acknowledges and responds to SYN.
  - **ACK packet:** Confirms connection establishment.
- Analogy: Saying "hello" to a neighbor and receiving a greeting back.

### Understanding Ports

- Ports facilitate communication with specific protocols.
  - Examples: HTTP (port 80), HTTPS (port 443).
- There are over 65,000 ports available for various protocols.

### Practical Example Using Wireshark

- Demonstration of capturing packet data with Wireshark.
- Explanation of packet flow during a TCP connection.
  - Sending SYN packet to initiate connection.
  - Receiving SYN-ACK packet if port is open.
  - Sending ACK packet to confirm connection.

## Key Takeaways

- The three-way handshake is crucial for TCP connections.
- Understanding the handshake process is important for scanning and network communication.
- Tools like Wireshark can help visualize and analyze network traffic.

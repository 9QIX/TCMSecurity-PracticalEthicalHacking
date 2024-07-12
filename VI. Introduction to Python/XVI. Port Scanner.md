# Building a Simple Port Scanner in Python

## Overview

- Final video in the Python module
- Creating a basic but functional port scanner
- Discussing potential improvements and limitations

## Script Structure

1. Import required modules:

   ```python
   import sys
   import socket
   from datetime import datetime
   ```

2. Define target and handle arguments:

   ```python
   if len(sys.argv) == 2:
       target = socket.gethostbyname(sys.argv[1])
   else:
       print("Invalid amount of arguments")
       print("Syntax: python3 scanner.py <ip>")
   ```

3. Create a banner:

   ```python
   print("-" * 50)
   print(f"Scanning target {target}")
   print(f"Time started: {str(datetime.now())}")
   print("-" * 50)
   ```

4. Main scanning loop:

   ```python
   try:
       for port in range(50, 85):
           s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
           socket.setdefaulttimeout(1)
           result = s.connect_ex((target, port))
           if result == 0:
               print(f"Port {port} is open")
           s.close()
   ```

5. Handle exceptions:
   ```python
   except KeyboardInterrupt:
       print("\nExiting program")
       sys.exit()
   except socket.gaierror:
       print("Hostname could not be resolved")
       sys.exit()
   except socket.error:
       print("Couldn't connect to server")
       sys.exit()
   ```

## Key Points

- The script scans a range of ports (50-85 in the example)
- It's relatively slow due to sequential scanning
- Improvements could include threading for faster scanning
- Error handling is implemented for common issues

## Usage

```
python3 scanner.py <ip_address>
```

## Limitations and Potential Improvements

- Slow for large port ranges
- Could benefit from threading for faster scanning
- More robust error handling and input validation could be added
- Additional features like service detection could be implemented

The instructor emphasizes that this is a basic implementation to demonstrate Python concepts and serve as a foundation for more advanced tools.

### Port Scanner

```python
#!/usr/bin/env python3

import sys
import socket
from datetime import datetime

# Validate and parse command line arguments
if len(sys.argv) == 2:
    target = socket.gethostbyname(sys.argv[1])  # Translate hostname to IPv4
else:
    print("Invalid amount of arguments")
    print("Syntax: python3 scanner.py <ip>")
    sys.exit()

# Display scanning information
print("-" * 50)
print(f"Scanning target {target}")
print(f"Time started: {str(datetime.now())}")
print("-" * 50)

# Main scanning loop
try:
    for port in range(50, 85):  # Adjust the port range as needed
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)  # Create a socket
        socket.setdefaulttimeout(1)  # Set a timeout for socket operations
        result = s.connect_ex((target, port))  # Attempt to connect to the port
        if result == 0:  # Port is open
            print(f"Port {port} is open")
        s.close()  # Close the socket
except KeyboardInterrupt:
    print("\nExiting program")
    sys.exit()
except socket.gaierror:
    print("Hostname could not be resolved")
    sys.exit()
except socket.error:
    print("Couldn't connect to server")
    sys.exit()
```

# Bash Scripting: Creating a Ping Sweeper Script

## Overview

- Building a basic ping sweeper script
- Learning concepts like `grep`, `cut`, `tr`, and for loops
- Watching the video first, then following along for hands-on learning

## Narrowing Down Results

- Using `grep` to grab lines containing a specific string (e.g., "64 bytes")
- Using `cut` to extract a specific field (e.g., IP address) based on delimiter
- Using `tr` to remove unwanted characters (e.g., colon from IP address)

## Writing the Ping Sweeper Script

- Shebang line: `#!/bin/bash`
- Ping command with count of 1: `ping -c 1 $1.$IP`
- Narrowing down with `grep`, `cut`, `tr`
- For loop to iterate through IP range: `for IP in {1..254}`
- User input with `$1` for network prefix
- Error handling with if statement: `if [ -z "$1" ]; then ... else ... fi`

## Testing the Script

- Making the script executable: `chmod +x ip_sweep.sh`
- Running the script: `./ip_sweep.sh 192.168.1`
- Saving results to a file: `./ip_sweep.sh 192.168.1 > ip_list.txt`

## One-Liner for Loop

- Running a command for each IP in the list
- Example: `for IP in $(cat ip_list.txt); do nmap -p 80 -sS -T4 $IP & done`
  - Pings port 80 on each IP in the list using nmap

The video covers creating a basic ping sweeper script in Bash, demonstrating concepts like `grep`, `cut`, `tr`, and for loops. It also shows how to run commands for each IP in a list using a one-liner for loop.

### IP Sweep

```bash
#!/bin/bash

# Check if the first argument ($1) is empty
if [ "$1" == "" ]
then
    # If no argument is provided, print an error message
    echo "You forgot an IP address!"
    # Provide the correct syntax for running the script
    echo "Syntax: ./ipsweep.sh 192.168.1"

else
    # If an argument is provided, proceed with the for loop
    # Loop through the numbers 1 to 254
    for ip in `seq 1 254`; do
        # Send one ping packet to the IP address composed of the argument and the current loop number
        # Example: if $1 is 192.168.1, then it pings 192.168.1.1, 192.168.1.2, ..., 192.168.1.254
        ping -c 1 $1.$ip |
        # Check the output for the presence of "64 bytes", indicating a successful ping
        grep "64 bytes" |
        # Extract the 4th field from the output (which is the IP address), and remove the trailing colon
        cut -d " " -f 4 | tr -d ":" &
    done
    # The '&' at the end of the ping command runs each ping in the background, allowing multiple pings to be sent simultaneously
fi
```

### Explanation:

1. **Shebang (`#!/bin/bash`)**:

   - Specifies the script should be run using the Bash shell.

2. **Checking for Argument**:

   - `if [ "$1" == "" ]`: Checks if the first argument (`$1`) is empty.
   - `then`: If the argument is empty, it prints a message indicating that the user forgot to provide an IP address and shows the correct syntax for running the script.

3. **Loop and Ping**:
   - `else`: If the argument is provided, the script enters the loop.
   - `for ip in \`seq 1 254\`; do`: Loops through numbers 1 to 254.
   - `ping -c 1 $1.$ip`: Pings each IP address formed by appending the loop number (`ip`) to the provided base IP (`$1`), e.g., `192.168.1.1`, `192.168.1.2`, ..., `192.168.1.254`.
   - `grep "64 bytes"`: Filters the output of the ping command to lines containing "64 bytes", indicating a successful ping.
   - `cut -d " " -f 4`: Extracts the 4th field of the filtered output, which is the IP address.
   - `tr -d ":"`: Removes the trailing colon from the extracted IP address.
   - `&`: Runs the ping command in the background to allow parallel execution of pings, speeding up the scanning process.

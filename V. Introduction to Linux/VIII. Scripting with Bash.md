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

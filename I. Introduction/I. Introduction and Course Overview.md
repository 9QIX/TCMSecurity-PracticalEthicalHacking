# Practical Ethical Hacking Course Introduction

## About the Instructor

- The instructor's name is Heath Adams (known online as The Cyber Mentor)
- He is a husband, hacker, military veteran, former accountant, and owner of TCM Security (penetration testing company)
- He is active on various social media platforms like Twitch, YouTube, and Twitter

## Course Overview

### What Makes This Course Different?

- Focuses on practical experience and concepts, not just tools
- Explains concepts in a simple, easy-to-understand manner
- Covers topics often overlooked, like Active Directory penetration testing

### Cour se Topics

1. **Introduction**
   - Effective note-taking
2. **Foundations**
   - Networking
   - Linux
   - Python
3. **External Network Hacking**
4. **Active Directory Exploitation**
   - Building and exploiting an Active Directory lab
5. **Web Application Exploitation**
   - Common attacks
6. **Wireless Exploitation**
7. **Report Writing and Legal Documentation**
   - Sample penetration testing report
   - Documentation for client meetings
8. **Career Advice**

## Additional Resources

- The instructor recommends checking out the bonus video first
- It provides information about joining the course's Discord channel (with 4000+ members)
- The Discord channel is a resource for troubleshooting and asking questions related to the course

Overall, the course promises a practical and comprehensive approach to ethical hacking, covering various aspects from foundations to advanced topics like Active Directory exploitation.

### IP Sweep

```bash
#!/bin/bash
# The shebang line specifies the script's interpreter

if [ "$1" == "" ]
then
    # If no argument is provided (i.e., the first argument is an empty string), the script informs the user they forgot an IP address
    echo "You forgot an IP address!"
    echo "Syntax: ./ipsweep.sh 192.168.1"
else
    # If an IP address prefix is provided, the script proceeds to the for loop
    for ip in `seq 1 254`; do
        # seq 1 254 generates a sequence of numbers from 1 to 254
        # For each number, it performs the following actions:

        # Ping the constructed IP address once (ping -c 1), appending the current number to the provided IP prefix
        # grep "64 bytes" filters the ping output to lines containing "64 bytes", indicating a successful ping
        # cut -d " " -f 4 extracts the 4th field of the filtered line, which is the IP address
        # tr -d ":" removes the trailing colon from the IP address
        ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
        # The ampersand (&) at the end makes the ping command run in the background, allowing the loop to continue immediately
    done
fi
```

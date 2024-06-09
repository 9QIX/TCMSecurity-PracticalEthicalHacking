# Introduction to Basic Linux Networking Commands

The transcript covers several fundamental networking commands in Linux that are useful for penetration testing:

## ifconfig

- Shows network interface configuration details like IP address, netmask, broadcast address, MAC address
- Helps identify network interfaces like wired ethernet (ethX) or wireless (wlanX)

## ping

- Tests connectivity to a target IP address or hostname
- Sends ICMP echo request packets and listens for responses
- Can be stopped with Ctrl+C

## arp

- Shows the IP to MAC address mappings cached by the system
- Used to map an IP address to a MAC address on the local network

## netstat

- Displays active network connections and ports
- `netstat -anl` shows listening TCP/UDP ports and programs
- Useful for seeing what services are running

## route

- Prints the system's routing table
- Shows gateways and network interfaces used to reach destinations
- Helps understand network topology for pivoting during attacks

These basics of configuring network interfaces, testing connectivity, mapping addresses, viewing connections and routing give penetration testers essential visibility into the networking environment before exploiting vulnerabilities.

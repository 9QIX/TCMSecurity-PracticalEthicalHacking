# Subnetting Practice

This video walks through solving a subnetting challenge together. Here are the key points:

## Challenge

- IP Address: 192.168.0.0/22
- Determine the subnet mask and range of usable IP addresses

## Solution

### /22 Subnet

- Number of Hosts: 1024 (2^10 - 2 reserved IPs)
- Subnet Mask: 255.255.252.0
- Network Address: 192.168.0.0
- Broadcast Address: 192.168.3.255
- Usable IP Range: 192.168.0.1 - 192.168.3.254 (divided into 4 subnets)

### /26 Subnet

- Number of Hosts: 62 (2^6 - 2 reserved IPs)
- Subnet Mask: 255.255.255.192
- Network Address: 192.168.1.0
- Broadcast Address: 192.168.1.63
- Usable IP Range: 192.168.1.1 - 192.168.1.62

### /27 Subnet

- Number of Hosts: 30 (2^5 - 2 reserved IPs)
- Subnet Mask: 255.255.255.224
- Network Address: 192.168.1.0
- Broadcast Address: 192.168.1.31
- Usable IP Range: 192.168.1.1 - 192.168.1.30

## Key Takeaways

- Understand the subnet notation (/x) and how it relates to the number of hosts
- Recognize the most common subnet mask (/24 or 255.255.255.0)
- Larger subnet numbers (/28, /29, etc.) mean fewer available hosts
- Additional resources and support are provided for further understanding

The instructor emphasizes that subnetting can be challenging, but it's essential to grasp the basics presented in this video.

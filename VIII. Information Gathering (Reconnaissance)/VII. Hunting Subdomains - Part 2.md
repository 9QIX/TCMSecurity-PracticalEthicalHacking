# Subdomain Enumeration: Results and Advanced Tools

## Sublister Results

- Found 87 subdomains for Tesla.com
- Automatically includes fourth-level domains
- Interesting findings:
  - dev.tesla.com
  - staging.tesla.com
  - sso-dev.tesla.com
  - qa.tesla.com
  - vpn.tesla.com
  - webmail.tesla.com

## Improving Sublister Performance

- Use `-h` to check help options
- `-t` flag for specifying threads (e.g., `-t 100`)
- `-v` flag for verbosity and real-time results

## Advanced Tools

### 1. Amass

- Popular tool for bug bounty hunters
- More comprehensive than Sublister
- Available on GitHub: [Amass Project](https://github.com/OWASP/Amass)
- Takes longer to run but finds more subdomains

### 2. HTTProbe

- Used to verify if discovered subdomains are active
- Helps narrow down the list of potential targets

## Key Points

- Not all discovered subdomains will be active or accessible
- Subdomain enumeration is crucial for expanding the scope of testing
- Consider using multiple tools for better coverage

## Challenge

Install Amass and compare its results with Sublister to see how many more subdomains can be discovered.

The content emphasizes the importance of thorough subdomain discovery, introduces more advanced tools, and provides tips for improving the enumeration process.

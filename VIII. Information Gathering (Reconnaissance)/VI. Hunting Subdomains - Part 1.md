# Web Information Gathering for Penetration Testing

## Importance of Subdomain Discovery

- Critical for web penetration testing and bug bounty hunting
- Helps identify potentially vulnerable or unintended sites
- Expands the scope of assessment beyond the main domain

## Tools for Subdomain Enumeration

### 1. Sublister

- Installation: `apt install sublister`
- Usage: `sublister -d domain.com`
- Searches through multiple search engines

### 2. crt.sh

- Web-based tool using certificate fingerprinting
- Can find subdomains and sub-subdomains
- Example search: `%.tesla.com`

## Key Points

- Wildcard domains (e.g., \*.tesla.com) open up the entire scope
- Look for interesting subdomains like dev, test, vpn, api, etc.
- Consider different levels of subdomains (e.g., third-level, fourth-level)

## Next Steps

- Exploring more efficient tools written in Go
- Reviewing and analyzing the results of subdomain enumeration

The content emphasizes the importance of thorough subdomain discovery in web penetration testing and introduces basic tools and techniques for this process.

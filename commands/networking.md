### Networking Commands
```bash
ip a  # Show all network interfaces and their IP addresses
ping -c 5 google.com  # Ping a host with 5 packets
netstat -tulnp  # Show active network connections with process IDs
traceroute google.com  # Show the path packets take to a host
dig +short google.com  # Get only the IP address of a domain
nslookup -type=MX google.com  # Get mail exchange records of a domain
nmap -sS -p 22 192.168.1.1  # Scan a host for open SSH port
curl -I https://example.com  # Fetch HTTP headers of a website
wget -c http://example.com/file.iso  # Download a file with resume support
```

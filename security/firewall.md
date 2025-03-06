### Managing Firewalls with UFW
```bash
sudo ufw status  # Check firewall status
sudo ufw enable  # Enable firewall
sudo ufw disable  # Disable firewall
sudo ufw allow 22  # Allow SSH traffic
sudo ufw deny 80  # Deny HTTP traffic
sudo ufw delete allow 22  # Remove a rule
```

### Managing Firewalls with IPTables
```bash
sudo iptables -L  # List current rules
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT  # Allow SSH
sudo iptables -A INPUT -p tcp --dport 80 -j DROP  # Block HTTP
sudo iptables -D INPUT -p tcp --dport 22 -j ACCEPT  # Delete SSH rule
sudo iptables-save > /etc/iptables.rules  # Save rules
```

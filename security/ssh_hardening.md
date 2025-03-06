### Enhancing SSH Security
```bash
sudo vim /etc/ssh/sshd_config
```
Modify the following settings:
```bash
PermitRootLogin no  # Disable root login
PasswordAuthentication no  # Disable password authentication
AllowUsers username  # Restrict SSH access to specific users
Protocol 2  # Use SSH protocol version 2
```

### Restart SSH Service
```bash
sudo systemctl restart ssh
```

### Using SSH Keys
```bash
ssh-keygen -t rsa -b 4096  # Generate an SSH key
ssh-copy-id user@server  # Copy public key to remote server
```

### Fail2Ban for SSH Protection
```bash
sudo apt install fail2ban  # Install Fail2Ban
sudo systemctl enable fail2ban  # Enable Fail2Ban service
sudo vim /etc/fail2ban/jail.local  # Configure SSH protection
```

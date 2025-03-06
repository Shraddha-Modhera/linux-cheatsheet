### Analyzing System Logs
Linux stores system logs in various locations, which can be useful for debugging issues.

#### Viewing Logs
```bash
journalctl -xe  # View detailed system logs with explanations
journalctl -u sshd --since "1 hour ago"  # Filter logs for SSH service in the last hour
journalctl --since "2024-01-01" --until "2024-01-31"  # View logs for a specific date range
sudo dmesg | tail -20  # View last 20 kernel logs (useful for hardware issues)
cat /var/log/syslog | grep 'error'  # Search for errors in syslog
cat /var/log/messages | grep -i 'failed'  # Find failed operations in logs
```

#### Viewing Logs of Specific Services
```bash
sudo systemctl status apache2  # Check the status and logs of a service
journalctl -u nginx --since "30 min ago"  # Check logs of the Nginx service for the last 30 minutes
```

### Monitoring Logs in Real-Time
```bash
tail -f /var/log/auth.log  # Monitor authentication logs in real-time
sudo journalctl -f  # Follow system logs live
sudo dmesg -wH  # Follow kernel logs live with human-readable timestamps
```

### Log Rotation Management
Log rotation prevents logs from growing indefinitely and consuming disk space.

#### Checking Log Rotation Configuration
```bash
cat /etc/logrotate.conf  # View global log rotation settings
cat /etc/logrotate.d/syslog  # View specific log rotation settings
```

#### Forcing Log Rotation
```bash
sudo logrotate -d /etc/logrotate.conf  # Dry run to test log rotation
sudo logrotate -f /etc/logrotate.conf  # Force log rotation
```

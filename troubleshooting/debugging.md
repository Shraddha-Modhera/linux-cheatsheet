### Debugging System Issues
#### Monitoring System Resource Usage
```bash
top  # Identify high CPU/memory usage processes
htop  # Interactive process viewer (better than top)
vmstat 1 5  # Monitor system performance with updates every second for 5 iterations
mpstat -P ALL 1  # CPU usage across all cores
iostat -dx 1  # Disk I/O usage per second
free -m  # Display free and used memory in MB
```

### Network Debugging
#### Checking Network Connectivity
```bash
ping -c 5 google.com  # Check network connectivity to a remote host
traceroute google.com  # Trace network route to the target server
```

#### Analyzing Open Ports and Connections
```bash
netstat -tulnp  # Show open ports and listening services
ss -tulnp  # Show active network connections (replacement for netstat)
sudo lsof -i :22  # Check which process is using a specific port (SSH in this case)
```

#### Capturing and Analyzing Network Traffic
```bash
tcpdump -i eth0 port 80  # Capture HTTP traffic on eth0 interface
sudo tcpdump -i any -n -c 100  # Capture 100 packets from all interfaces
```

### Debugging Disk Issues
#### Checking Disk Space and Usage
```bash
df -h  # Show available disk space in human-readable format
du -sh /var/log  # Show size of a specific directory
find / -type f -size +1G  # Find large files (greater than 1GB)
```

#### Checking and Repairing Filesystems
```bash
sudo fsck /dev/sda1  # Check and repair filesystem errors
mount | column -t  # Check mounted filesystems and their options
```

### Debugging Application Issues
#### Identifying Resource-Intensive Processes
```bash
ps aux --sort=-%cpu | head -10  # Show top 10 CPU-consuming processes
ps aux --sort=-%mem | head -10  # Show top 10 memory-consuming processes
```

#### Tracing System Calls
```bash
strace -p PID  # Trace system calls of a running process
strace -e open,read,write -p PID  # Trace file operations for a process
```

#### Checking Open Files
```bash
lsof -p PID  # List files opened by a specific process
lsof +D /var/www/html  # Find open files in a specific directory
```

#### Checking Logs for Application Errors
```bash
tail -f /var/log/nginx/error.log  # Monitor Nginx error logs
journalctl -u apache2 --since "1 hour ago"  # Check Apache logs from the last hour
```


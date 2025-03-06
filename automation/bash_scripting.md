### Bash Scripting Basics
```bash
#!/bin/bash
# This script prints system information
echo "Hostname: $(hostname)"
echo "Uptime: $(uptime -p)"
echo "Logged-in Users: $(who | wc -l)"
```

### Looping in Bash
```bash
for i in {1..5}; do echo "Iteration $i"; done
while true; do echo "Press Ctrl+C to stop"; sleep 1; done
```

### Conditional Execution
```bash
if [ -f /etc/passwd ]; then
    echo "User database exists."
else
    echo "File not found."
fi
```

### Functions in Bash
```bash
function greet() {
    echo "Hello, $1!"
}
greet "DevOps Engineer"
```

### Automating Backups
```bash
#!/bin/bash
tar -czf backup_$(date +%F).tar.gz /home/user/data/
echo "Backup completed successfully!"
```
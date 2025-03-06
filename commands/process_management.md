### Process Management
```bash
ps aux | grep apache  # Find a running process by name
top -o %CPU  # Show processes sorted by CPU usage
htop  # Interactive process manager (requires installation)
pkill -f processname  # Kill all processes matching name
kill -9 1234  # Force kill a process by its PID
nohup command &  # Run a command in the background that survives logout
jobs  # List background jobs
bg %1  # Resume job 1 in the background
fg %1  # Resume job 1 in the foreground
```

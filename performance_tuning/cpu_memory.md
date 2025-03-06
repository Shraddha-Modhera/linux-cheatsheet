### Monitoring CPU & Memory Usage
```bash
top       # Real-time CPU and memory usage
iostat -c 1  # CPU usage per second
mpstat -P ALL 1  # CPU usage across all cores
vmstat 1 10  # Memory, swap, and CPU activity over time
free -h  # Display available memory in human-readable format
```

### Optimizing CPU Performance
```bash
nice -n 10 command  # Run a process with lower priority
renice -n -5 -p PID  # Increase priority of a running process
cpulimit -l 50 -p PID  # Limit CPU usage of a process to 50%
```

### Managing Memory Usage
```bash
sysctl vm.swappiness=10  # Reduce swap usage
sync && echo 3 > /proc/sys/vm/drop_caches  # Free cached memory
ulimit -a  # Show user resource limits
```

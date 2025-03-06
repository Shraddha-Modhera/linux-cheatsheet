### Monitoring Disk I/O
```bash
iostat -dx 1  # Show disk I/O usage
iotop  # Display real-time I/O usage per process
df -h  # Display disk space usage
lsblk -o NAME,FSTYPE,SIZE,MOUNTPOINT  # List block devices and mount points
```

### Improving Disk Performance
```bash
tune2fs -o journal_data_writeback /dev/sda1  # Optimize ext4 journaling
mount -o noatime,commit=60 /dev/sda1 /mnt  # Reduce write operations
```

### Managing Disk Space
```bash
ncdu /  # Interactive disk usage analyzer
find / -type f -size +1G  # Find files larger than 1GB
```

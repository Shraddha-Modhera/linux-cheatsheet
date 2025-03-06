### Disk Management
```bash
df -h  # Show disk usage in human-readable format
du -sh dir/  # Show total size of a directory
lsblk  # List all block storage devices
fdisk -l  # Show partition table of all disks
parted /dev/sdb print  # View detailed partition information
mkfs.ext4 /dev/sdb1  # Format a partition with ext4 filesystem
mount /dev/sdb1 /mnt  # Mount a partition
umount /mnt  # Unmount a partition
e2fsck -f /dev/sdb1  # Check and repair an ext4 filesystem
```
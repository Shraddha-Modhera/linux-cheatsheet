### File Permissions
```bash
ls -ld dir/  # Show permissions of a directory
chmod 755 script.sh  # Set executable permissions for the owner
chmod -R 777 dir/  # Give full permissions to everyone (not recommended)
chown user:group file.txt  # Change file ownership
chown -R user:group dir/  # Change ownership of a directory recursively
umask 022  # Set default permissions for new files
gpasswd -a user group  # Add user to a group
```

### Understanding Crontab Syntax
```bash
# ┌──────── minute (0 - 59)
# │ ┌────── hour (0 - 23)
# │ │ ┌──── day of the month (1 - 31)
# │ │ │ ┌── month (1 - 12)
# │ │ │ │ ┌─ day of the week (0 - 6) (Sunday = 0 or 7)
# │ │ │ │ │
# * * * * * command_to_execute
```

### Example Cron Jobs
```bash
0 3 * * * /usr/bin/find /var/log -type f -name '*.log' -mtime +7 -delete  # Delete logs older than 7 days
*/5 * * * * /home/user/monitor.sh  # Run a monitoring script every 5 minutes
@reboot /home/user/startup.sh  # Run a script at system startup
```

### Managing Cron Jobs
```bash
crontab -l  # List current cron jobs
crontab -e  # Edit crontab jobs
crontab -r  # Remove all cron jobs
```

### Logging Crontab Output
```bash
0 2 * * * /home/user/script.sh >> /var/log/script.log 2>&1  # Redirect output to a log file
```

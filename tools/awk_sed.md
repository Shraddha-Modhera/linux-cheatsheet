### Using `awk`
```bash
awk '{print $1}' file.txt  # Print first column
awk -F: '{print $1, $3}' /etc/passwd  # Print username and UID
awk '{sum+=$3} END {print sum}' data.txt  # Sum values in the third column
```

#### Filtering and Formatting
```bash
awk '$3 > 1000' /etc/passwd  # Print users with UID > 1000
awk '{print NR, $0}' file.txt  # Print line numbers before each line
```

#### Using Patterns
```bash
awk '/error/ {print $0}' logfile.txt  # Print lines containing 'error'
awk '/start/,/end/' file.txt  # Print lines between 'start' and 'end'
```

### Using `sed`
```bash
sed 's/old/new/g' file.txt  # Replace 'old' with 'new'
sed '/pattern/d' file.txt  # Delete lines matching pattern
sed -n '5,10p' file.txt  # Print lines 5 to 10
```

#### Modifying Files
```bash
sed -i 's/error/success/g' log.txt  # Replace text in a file directly
sed -e '1,10d' file.txt  # Delete lines 1 to 10
```

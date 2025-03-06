### Tmux Basics
```bash
tmux  # Start a new Tmux session
tmux new -s mysession  # Start a named session
tmux ls  # List all active sessions
```

#### Detaching and Attaching
```bash
Ctrl + b, d  # Detach session
tmux attach -t mysession  # Reattach to a named session
tmux kill-session -t mysession  # Kill a specific session
```

#### Managing Windows
```bash
Ctrl + b, c  # Create a new window
Ctrl + b, w  # List all windows
Ctrl + b, n  # Switch to next window
Ctrl + b, p  # Switch to previous window
Ctrl + b, &  # Close the current window
```

#### Managing Panes
```bash
Ctrl + b, "  # Split pane horizontally
Ctrl + b, %  # Split pane vertically
Ctrl + b, arrow  # Navigate between panes
Ctrl + b, x  # Close current pane
Ctrl + b, z  # Toggle pane zoom
```
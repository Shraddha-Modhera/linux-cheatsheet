### Vim Basics
```bash
vim filename  # Open a file in Vim
vim -R filename  # Open a file in read-only mode
vim +10 filename  # Open file and go to line 10
```

#### Switching Modes
- `i` : Insert mode (allows typing)
- `Esc` : Return to normal mode
- `v` : Visual mode (for selecting text)
- `V` : Visual line mode (select whole lines)
- `Ctrl + v` : Visual block mode (select a block of text)
- `:` : Command mode (for running commands)

#### Saving and Exiting
```bash
:w  # Save file
:q  # Quit Vim
:wq  # Save and quit
:x  # Save and quit (if changes were made)
:q!  # Quit without saving
```

#### Navigation
```bash
h  # Move left
l  # Move right
j  # Move down
k  # Move up
0  # Move to beginning of line
^  # Move to first non-blank character of line
$  # Move to end of line
G  # Move to last line of file
```

#### Searching and Replacing
```bash
/word  # Search for 'word'
n  # Jump to next occurrence
N  # Jump to previous occurrence
:%s/old/new/g  # Replace all occurrences of 'old' with 'new'
:%s/old/new/gc  # Confirm before replacing
```

#### Advanced Editing
```bash
yy  # Copy (yank) a line
p  # Paste copied text
dd  # Delete entire line
u  # Undo last change
Ctrl + r  # Redo last undone change
```
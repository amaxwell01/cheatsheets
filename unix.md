# Bash / Command Line Shortcuts
Replace CMD with Ctrl for PC
- CMD + A    Go to the beginning of the line you are currently typing on
- CMD + E  Go to the end of the line you are currently typing on
- CMD + L                  Clears the Screen, similar to the clear command
- CMD + U  Clears the line before the cursor position. If you are at the end of the line, clears the entire line.
- CMD + H  Same as backspace
- CMD + R  Let’s you search through previously used commands
- CMD + C  Kill whatever you are running
- CMD + D  Exit the current shell
- CMD + Z  Puts whatever you are running into a suspended background process. fg restores it.
- CMD + W  Delete the word before the cursor
- CMD + K  Clear the line after the cursor
- CMD + T  Swap the last two characters before the cursor
- Esc + T   Swap the last two words before the cursor
- Alt + F   Move cursor forward one word on the current line
- Alt + B   Move cursor backward one word on the current line
- Tab   Auto-complete files and folder names

## iTerm2 Tips and Tricks:
- Search: Cmd+f
- Autocomplete: Cmd+;
- Paste history: Cmd+Shift+H
- Instant replay: Cmd+Alt+B
- iTerm2 Exposé: Cmd+ Alt+E
- Support for many of the readline bindable commands:
- Ctrl+a: beginning of line
- Ctrl+e: end of line
- Ctrl+f: forward 1 char
- Ctrl+b: back 1 char
- Ctrl+l: clear screen
- Ctrl+p: previous history
- Ctrl+r: history reverse search
- Ctrl+d: delete current char
- Ctrl+h: delete previous char
- Ctrl+w: kill the word behind point
- Ctrl+k: kill text from the point to the end of the line


## Compression

### Tar'ing a file
```
tar -cvf <tar_file_name.tar> <folder to tar>
```

### Un-Tar'ing a file
```
tar -xvf <tar_file_name.tar> <folder to tar>
```

### How to unzip a file
```
unzip filename.zip
```

### How to remove all files recursively
```
find . -name '*.DS_Store' -type f -delete
```


### SCP'ing a file onto a machine
```
scp -i <location_of_pem_file> <file_to_transfer> user@machineip:/<location_to_upload_to>
```

### SCP'ing a file from a machine
```
scp -i <location_of_pem_file> user@machineip:<file_to_transfer> <folder_to_transfer_to>
```

### SSH'ing into a machine with a pem file
```
ssh -i <location_of_pem_file> user@machineip
```

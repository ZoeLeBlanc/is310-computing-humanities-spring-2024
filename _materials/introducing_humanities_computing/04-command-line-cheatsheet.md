---
title: "Command Line Cheatsheet"
permalink: /materials/introducing-humanities-computing/04-command-line-cheatsheet
excerpt: "A resource to help with command line syntax"
toc: true
---

## Why use the Command Line?

Though Command Line might sounds a bit intimidating, it is very useful and like we read about in the *Verge* article can be enormously useful for when you work with many files and folders. It is also a great way to get a sense of how your computer works and how to navigate it. Finally, it's incredibly useful for coding, as we'll see throughout this semester.

If you are using the WSL (Windows Subsystem for Linux), a Mac, or a Linux, you can should use the MacOS cheatsheet. If you are using a Windows PowerShell, you should use the Windows cheatsheet. Remember, you can use all of these via VS Code's terminal, but you should always check to see which operating system you are using.

## Command Line Cheatsheet for Windows

| Command | Description |
| ------------- | ------------- |
| `cd` | Print full working path |
| `dir` or `gci`| List contents of a directory  |
| `chdir [folder]` or `sl` | Change into a directory |
| `sl ..` | Go one directory up |
| `cls` | Clear the view |
| `open [file]` | Opens a file |
| `open .` | Opens the directory |
| `ni [file name]`| Creates a new file |
| `del [file name]`| Remove a single file |
| `ni -ItemType dir [directory name]` | Make a new directory |
| `copy [file] [new file/new directory]` | Copy file to file or new directory |
| `move [file] [new file/new directory]` | Move file into new file or directory |
| `rmdir [directory]` | Remove directory ( only operates on empty directories ) |
| `rmdir /s [directory name]` | Force remove a directory and all its contents |
| `help` | Prints all possible commands |
| `Get-ChildItem -Path [directory] -Recurse -Force -File` | List all files (including hidden ones) in a directory and subdirectories. All the flags are optional. You would use `-Path` if you wanted to specify a different directory than the one you're in. You would use `-Recurse` if you wanted to list all files in subdirectories. You would use `-Force` if you wanted to list hidden files. You would use `-File` if you wanted to list only files and not directories. |

### Advanced Commands

| Command | Description |
| ------------- | ------------- |
| `sudo [command]` | Run command with the security privileges of the superuser (Super User DO) |
| `cp *.js`| Use wildcards to get all files of a certain type when moving or copying|
| `edit [file]` | Opens file in Terminal editor |
| `exit` | Exit |

## Command Line Cheatsheet for MacOS

| Command | Description |
| ------------- | ------------- |
| `pwd` | Print full working path |
| `.` | Current folder |
| `cd [folder]` | Change into a directory |
| `cd ..` | Change directory upwards |
| `ls` | List contents of a directory |
| `ls -la` | List all contents including hidden files |
| `clear` | Clear the view |
| `open [file]` | Opens a file |
| `open .` | Opens the directory |
| `touch [file name]`| Creates a new file |
| `rm [file name]`| Remove a single file |
| `mkdir [directory name]` | Make a new directory |
| `cp [file] [new file/new directory]` | Copy file to file or new directory |
| `mv [file] [new file/new directory]` | Move file into new file or directory |
| `rmdir [directory]` | Remove directory ( only operates on empty directories ) |
| `rm -rf [directory name]` | Force remove a directory and all its contents |

### Advanced Commands

| Command | Description |
| ------------- | ------------- |
| `sudo [command]` | Run command with the security privileges of the superuser (Super User DO) |
| `cp *.js`| Use wildcards to get all files of a certain type when moving or copying|
| `!!` | Use double bang to repeat last command |
| `nano [file]` | Opens file in Terminal editor |
| `q` | Exit |

## Tips for the Command Line

### Basic Navigation

- **Tab Auto-Complete**: Typing the first few letters of a directory or file name and then pressing `Tab` will auto-complete the name. This is incredibly useful in saving time and avoiding typos, especially with long or complex names.

- **Up Arrow for History**: Press the `Up Arrow` key to scroll through your previously entered commands. This is handy for repeating or modifying past commands without retyping them.

- **Ctrl + A and Ctrl + E**:
  - `Ctrl + A` moves your cursor to the beginning of the line. Use this when you need to quickly go back to the start of your command.
  - `Ctrl + E` takes you to the end of the line. This is useful if you're editing a command at the beginning and need to jump to the end.

### Searching Commands

- **Ctrl + R for Reverse Search**: Press `Ctrl + R` and start typing to search through your command history. This reverse search allows you to find and reuse complex commands without having to remember them in full.

### Managing Processes

- **Ctrl + C to Stop Processes**: If you run a command that takes too long or starts behaving unexpectedly, `Ctrl + C` will interrupt and stop it. This can be crucial for stopping scripts or commands that are leading you in circles.

### Exiting

- **Exit Command**: Type `exit` to leave the current shell session. This is like finding the exit in a maze; use it when you've reached your goal, or if you need to start over.

## Additional Tips

- **Stay Organized**: Keep track of your location. Use `pwd` to print your current directory and `ls` to list the contents of the directory you're in.
- **Explore Carefully**: Before running scripts or opening files, use commands like `cat`, `less`, or `head` to preview their contents. This way, you avoid unexpected outcomes.
- **Document Your Journey**: Consider taking notes in a separate document or on paper about the paths you've taken. This will help you avoid going in circles and make it easier to retrace your steps.
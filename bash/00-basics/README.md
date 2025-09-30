# Navigating in file system

## Useful commands

- `pwd` - Print working directory, shows where we are.
- `cd` - Change directory, move to another folder
- `ls` - Shows files and directories in a folder

## Terminal key binds
- `Tab` - The most important key. Do not write names and commands whole, keep pressing `Tab` to keep getting hints. Never write whole names yourself.
- `Q` - The usual key to close when reading some file in terminal
- `Ctrl+C` - Terminate current command, delete what I am currently writing
- `Ctrl+D` - End or input, Close the terminal session
- `Ctrl+Shift+C` - Copy something
- `Ctrl+Shift+V` - Paste something

## Paths

Paths can be:
- Relative - evaluated from the working directory
  * Do not start with `/` symbol
  * Example: `LearnByExample/bash` 
- Absolute - evaluated from the file system root
  * Always start with `/` symbol
  * Example: `/mnt/c/Users/ryth/Documents/Projects/LearnByExample`

Helpful shortcuts:
 - `~` - The home directory
 - `./` - The current directory
 - `../` - The parent directory
 - `/` - The root directory
 - `-` - The previous directory

### Hidden files
Hidden files name start with a dot `.` and will not show when viewing a folder.

## Getting help
All programs should provide information on how to use them. The usual way is to provide help when ran with `--help` or `-h` flag. This is usually faster than having to Google everything.

### Excercise
Try to get and read the help section for all the commands in this chapter. Don't forget you can press 'Q' to exit the help pages.

### Solution
```bash
pwd -h 
cd -h
ls --help
```

### Additional Info
To get even more information, we can also read the manual. To open a manual for a command, simpy type `man [command]`. So to get manual for ls, type `man ls`. Curiously, there is even a manual for manual `man man`.

We can scroll the manual using Arrows, PageUp, PageDown and Q to quit.

## Navigating File system
Use the previous infomation to solve the following tasks

### Excercise
1. Go to folder called `bash` and print its contents
2. Go to the root directory and check the working directory
3. Go back to the previous folder
4. Go to the parent folder and print its contents as list with human readable sizes and hidden folders, sorted by size

Use manual and help pages to solve number 4.

### Solutions
```bash
# Number 1
cd bash
ls
# Number 2
cd / 
pwd
# Number 3
cd - 
# Number 4
cd ..
ls -laSh
```
- `-l` - long listing format
- `-a` - show hidden files (starting with `.`)
- `-S` - sort by size
- `-h` - human readable sizes

Flags can be chained together, so instead of typing `ls -l -a -S -h`, you can type `ls -laSh`, it doest the same.
# The Command Line

- command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text

- The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands

- shell is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you

```bash
echo $SHELL 
```

***This command used to know which shell you are using***

<br/>

## For more info check out this source [The Command Line!](https://ryanstutorials.net/linuxtutorial/commandline.php)

<br/>

# Basic Navigation

- pwd: stands for Print Working Directory

```bash
pwd
```

- ls: short for list

```bash
ls [options] [location]
```

- cd: change directory

```bash
cd [location]
```

## IMPORTANT CONCEPTS

- Relative path: A file or directory location relative to where we currently are in the file system.
- Absolute path: A file or directory location in relation to the root of the file system.

<br/>

## For more info check out this source [Basic Navigation!](https://ryanstutorials.net/linuxtutorial/navigation.php)

<br/>

# More About Files

- file: obtain information about what type of file a file or directory is.

```bash
file [path]
```

- ls -a: List the contents of a directory, including hidden files.

```bash
ls -a
```

## IMPORTANT CONCEPTS

- Everything is a file under Linux: Even directories.
-Linux is an extensionless system: Files can have any extension they like or none at all.
-Linux is case sensitive: Beware of silly typos.

<br/>

## For more info check out this source [More About Files!](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)

<br/>

# Manual Pages

- man < someCommand > : Look up the manual page for a particular command.

```bash
man <someCommand>
```

- man -k < someSearchTerm > : Do a keyword search for all manual pages containing the given search term.

```bash
man -k <someSearchTerm>
```

- /< term > : Within a manual page, perform a search for 'term'

```bash
/<term>
```

- n : After performing a search within a manual page, select the next found item.

```bash
n
```

## IMPORTANT CONCEPTS

The man pages are your friend: Instead of trying to remember everything, instead remember you can easily look stuff up in the man pages.

<br/>

## For more info check out this source [Manual Pages!](https://ryanstutorials.net/linuxtutorial/manual.php)

<br/>

# File Manipulation

- mkdir: Make Directory - ie. Create a directory.

```bash
mkdir [options] <Directory>
```

- rmdir: Remove Directory - ie. Delete a directory.

```bash
rmdir [options] <Directory>
```

- touch: Create a blank file.

```bash
touch [options] <filename>
```

- cp: Copy - ie. Copy a file or directory.

```bash
cp [options] <source> <destination>
```

- mv: Move - ie. Move a file or directory (can also be used to rename).

```bash
mv [options] <source> <destination>

mv [options] <oldName> <newName>
```

- rm: Remove - ie. Delete a file.

```bash
rm [options] <file>
```

## IMPORTANT CONCEPTS

- No undo: The Linux command line does not have an undo feature. Perform destructive actions carefully.

- Command line options: Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.

<br/>

## For more info check out this source [File Manipulation!](https://ryanstutorials.net/linuxtutorial/filemanipulation.php)

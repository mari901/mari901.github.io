---
layout: default
---

# Command-Line Course Overview

This Command-Line Course promises to build foundational skills and extend to advanced concepts, such as scripting and web development with Jekyll and GitHub Pages, offering a vital skill set for any tech enthusiast.

## Week 1: Introduction to Command Line Environments

This week, we learned about setting up the command-line environment, which is essential for the entire course. I setup WSL2 with the help of the videos. 

Learned about basic fundamental commands like `ls` (list directory contents), `cd` (change directory), and `pwd` (print working directory) laid the groundwork for efficient navigation and task execution in the terminal. I also experimented with `nano`, a terminal-based text editor.

**Example Commands:**

- Navigating to a specific directory and listing its contents:

 ```console
  cd ~/KIK-LG221/week1
  ls -l
  ```
  This command changes the directory to `~/KIK-LG221/week1` and lists all files with detailed information.

- Using `echo` with output redirection to create a simple text file:

 ```console
  echo "Hello, Command Line World!" > greeting.txt
  ```
  This command outputs the text into a file named `greeting.txt`, demonstrating how commands can be used to manipulate files effortlessly.
  
## Week 2: Navigating a UNIX System

During this week, the focus was on system navigation, directory structures, and file permissions. I learned how to manage files and directories, utilizing commands such as `cp`, `mv`, and `rm`. Understanding the structure of UNIX directories and learning about user permissions was crucial in understanding how UNIX ensures user privacy and security. Additionally, I explored processes and process management, grasping how commands like `ls` or `nano` invoke new processes and how these can be controlled from the command line.

In the second part of the week, I explored connecting to remote servers using `ssh` and transferring files with `scp`, which opened up new possibilities for remote data management.

### Commands Reference Table

| Command                | Description                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------|
| `cp source dest`       | Copies a file from `source` to `dest`; if `dest` is a directory, it places the file inside.  |
| `mv source dest`       | Moves `source` to `dest`; can also be used to rename files or directories.                  |
| `rm file`              | Removes a file; use with caution. Adding `-r` removes directories and their contents.       |
| `chmod options file`   | Changes the permissions of `file`; `-R` applies changes recursively for directories.        |
| `ssh user@host`        | Opens a secure shell to a remote host, allowing terminal operations on the remote system.   |
| `scp source user@host:dest` | Copies files securely to/from a remote system using the same syntax as `cp`.                    |

## Week 3: Basic Corpus Processing

This week learned about UNIX text processing tools and character encodings.

<div style="text-align: center;">
  <img src="{{ '/assets/images/regex.jpg' | relative_url }}" alt="How to ReGex" width="340" height="340"/>
</div>


I've also learned about ReGex (regular expressions). Through the `grep` command and its variant `egrep`, we applied regular expressions to efficiently search through large texts.

Commands like `grep` for pattern matching in text, `tr` for character translation, and `sort` for ordering lines enhanced our ability to manipulate text data.


### Key Commands and Utilities:

| Command             | Description                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| `grep 'pattern' file`     | Searches for lines matching a pattern in the file using regular expressions.                           |
| `tr SET1 SET2`            | Translates or deletes characters from input data. For example, `tr 'A-Z' 'a-z'` converts upper to lowercase. |
| `sort`                    | Sorts lines in the specified files, useful for ordering text data alphabetically or numerically.    |
| `cut -d, -f1 file.csv`    | Extracts sections from each line of files, useful for handling CSV data.                                |
| `wc file`                 | Counts the lines, words, and bytes in files, useful for getting quick stats on text data.              |
---
layout: default
---

# Command-Line Tools for Linguists Course Overview

This command-line course is an introductory course to UNIX command line environment. It will teach you basics on command line tools and focuses on skills such as handling text files, writing basic scripts, working on a server, version control tools and web development with Jekyll and GitHub Pages.

## Week 1: Introduction to Command Line Environments

The first week is about setting up the command-line environment and learning some basic commands, which is essential for the entire course. I set up WSL 2 with the help of the videos. 

I learned about basic fundamental commands such as `ls` (list directory contents), `cd` (change directory), and `pwd` (print working directory). I also explored `nano`, a terminal-based text editor.

**Example Commands:**

- Navigating to a specific directory and listing its contents:

 ```console
  cd ~/KIK-LG221/week1
  ls -l
  ```
  This command changes the directory to `~/KIK-LG221/week1` and lists all the files.

- Using `echo` to create a simple text file:

 ```console
  echo "Hello, World!" > hello_world.txt
  ```
  This command outputs the text into a file named `hello_world.txt`.
  
## Week 2: Navigating a UNIX System

During the second week, the focus is on handling directories, managing processes and working with remote servers.

I learned how to manage files and directories, utilizing commands such as `cp`, `chmod`, and `ps`.
I connected to remote servers using `ssh` and transferring files with `scp`, which is used for data transfer.

### Commands Learned:

| Command                | Description                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| `cp source destination`       | Copies a file from `source` to `destination`; if `destination` is a directory, it places the file inside.   |
| `ln source target`     | Creates a link to `source` at `target`. Use `-s` to create a symbolic link instead of a hard link. |
| `chmod options file`   | Changes the permissions of `file`. `-R` can be used to apply changes recursively for directories.          |
| `ssh user@host`        | Opens a secure shell to a remote host which allows terminal operations on the remote system.     |
| `scp source user@host:dest` | Copies files securely to/from a remote system using the same syntax as `cp`.                   |
| `ps`                   | Displays information about active processes. Use options like `aux` to see detailed process information. |

## Week 3: Basic Corpus Processing

This week is about UNIX text processing tools and learning about different character encodings, such as ASCII and UTF-8.

<div style="text-align: center;">
  <img src="{{ '/assets/images/regex.jpg' | relative_url }}" alt="How to ReGex" width="340" height="340"/>
  <br>
  <a href="https://x.com/garabatokid/status/1147063121678389253" target="_blank">Source: Garabato Kid</a>
</div>

During this week I learned about ReGex (regular expressions). Through the `grep` command and its variant `egrep`, I used regular expressions to search through large texts. Using commands like `grep` for pattern matching in text, `tr` for character translation, and `sort` for ordering lines to manipulate text data.


### Commands Learned:

| Command             | Description                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------|
| `grep 'pattern' file`     | Searches for lines matching a pattern in the file using regular expressions.                           |
| `tr SET1 SET2`            | Translates or deletes characters from input data. For example, `tr 'A-Z' 'a-z'` converts upper to lowercase. |
| `sort`                    | Sorts lines in the specified files, useful for ordering text data alphabetically or numerically.    |
| `wc file`                 | Counts the lines, words, and bytes in files, useful for getting quick stats on text data.              |

## Week 4: Advanced Corpus Processing

This week is about corpus processing and focusing on piping commands by utilizing `sed` for text transformations. I learned about extended regular expressions which uses the grep command learned on the previous week and how to generate frequency lists and separate sentences on separate lines which is useful for text analysis and data processing.


### Commands Learned:

- **`sed 's/pattern/replacement/g' file`**: 
  - Substitutes a pattern with a replacement in a text stream, useful for text transformations.

- **`egrep '[aeiou]{2}' words.txt`**: 
  - Searches for words that contain a double vowel like: boot, pool, tool

- **`sort`**: 
  - Arranges lines of text files in a specified order by default sorts alphabetically. 

- **`uniq -c`**: 
  - Reports or omits repeated lines in a text file, useful for identifying unique entries.

- **`diff file1 file2`**: 
  - Compares two files line by line, showing differences. Very helpful for version control.


## Week 5: Scripting and Configuration Files

This week teaches about scripting and managing configuration files in UNIX. I explored the basics of Bash scripting, including variables, conditional statements, and environment variables. I also configured environment variables in `.bashrc` or `.bash_profile` to personalize the command-line experience.

### Example Scripts:

- **Simple Bash Script:**

  ```bash
  #!/bin/bash
  echo "Hello, World!"
  ```

  This script prints "Hello, World!" to the terminal.

- **Using Variables:**

  ```bash
  #!/bin/bash
  NAME="User"
  echo "Hello, $NAME!"
  ```

  This script defines a variable `NAME` and uses it to personalize the output.

- **Conditional statements:**

  ```bash
  #!/bin/bash
  if [ -f "myfile.txt" ]; then
      echo "myfile.txt exists."
  else
      echo "myfile.txt does not exist."
  fi
  ```

  This script checks if `myfile.txt` exists and prints a message based on the condition.

## Week 6: Installing and Running Programs

This week is about package managers like `apt` (Linux) and `brew` (macOS), the difference between `sudo` and `su` and how to use Makefiles. I also learned about `pip` and virtual environments in Python, which are essential for managing dependencies and isolating project environments.

### Concepts learned:

| Tool/Concept      | Description                                                                                             |
|-------------------|---------------------------------------------------------------------------------------------------------|
| `pip`             | A package manager for Python used to install and manage Python libraries and dependencies.              |
| `make`            | A tool that automatically builds executable programs and libraries from source code.   |
| `su` & `sudo`     | Commands for executing tasks with superuser privileges.                                                 |
| Package Managers  | Tools like `apt` and `brew` that automate the process of installing and removing software. |

## Week 7: Version Control

This week is about version control, `git` and Github. I learned about setting up repositories, branching, merging, and reverting changes. This made version control easier to understand and use. 

### Commands Learned

| Command                                    | Description                                                                                      |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|
| `git clone <repo-url>`                     | Clones an existing repository.                                                                   |
| `git add <file(s)>`                        | Stages changes for commit.                                                                       |
| `git commit -m "commit message"`           | Commits staged changes with a message.                                                           |
| `git push`                                 | Pushes committed changes to a remote repository.                                                 |
| `git log`                                  | Views the commit history.                                                                        |
| `git revert <commit>`                      | Creates a new commit that undoes changes from a specified commit.                                |
| `git switch <branch>`                      | Switches to the specified branch.                                                                |
| `git merge <branch>`                       | Merges the specified branch into the current branch.    

## Week 8: Building and Hosting a Website with Jekyll and GitHub Pages

The final week involved creating a personal website using Jekyll and hosting it on GitHub Pages. This project made me practice what I've learned weeks prior about version control and markdown. 

### Commmands Learned:

| Command                                    | Description                                                                                      |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|
| `sudo apt-get install ruby ruby-dev`       | Installs Ruby and Ruby development libraries.                                                    |
| `gem install jekyll bundler`               | Installs Jekyll and Bundler gems.                                                                |
| `bundle exec jekyll serve`                 | Builds the Jekyll site and serves it locally.                                                    |
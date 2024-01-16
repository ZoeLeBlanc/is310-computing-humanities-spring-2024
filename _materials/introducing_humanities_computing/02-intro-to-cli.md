---
title: "🔗 Coming Online: Introduction to the Command Line and Version Control"
permalink: /materials/getting-started/02-command-line
excerpt: "An introduction to the command line and version control"
toc: true
---

## Weekly Assessment Goals

*We will review concepts on Tuesday and all material should be submitted before next Thursday's class.*

1. [Introduction/review of the command line (with the instructor, optional)](#command-line-intro)
2. [Complete command line assignment](#command-line-assignment)

## What is the Command Line and how do we work with it?

- Command Line might sounds a bit intimidating
- But ask yourself, how do you find files and manipulate files on your computer? Probably using Windows Explorer or Mac Finder, right?
- Command Line is a text-based way of doing the same thing you do with your files
- Command Line is used a lot in coding because we manipulate our code files and run them all in the terminal

![command-line](https://image.slidesharecdn.com/cli-101-170406170732/95/commandline-101-3-638.jpg?cb=1491498863)

This is a helpful but brief overview. Often you might get confused, because we'll talk about command line interface/CLI, terminal, shell, console. While these terms are overlapping, my colleague [Shane Lin at UVA](https://github.com/scholarslab/CodeLab/blob/master/Week01/commandline.md) helped me understand that a lot of the differences between these terms has to do with the history of early computers, when computers looked like this 👇🏽.

![early-computer](https://www.computerhope.com/cdn/eniac.jpg)

According to Shane,
> Operators would interact with these machines through a smaller device dedicated to input and output, called a console or terminal. In the very early days, these consoles would use literal printers to print out output from the computer onto paper. In modern computing, "console" and "terminal" are analogies for software programs that replicate these technologies. The application "Terminal" on MacOS is a terminal software.

> A "shell" is a program that lives within a terminal that interprets commands from users and parses output from the computer. The name Shell comes out of the influential Unix operating system and is intended to convey the idea that shell programs completely surround and hide away the complex details of different underlying computer systems from users to provide a simplified and common interface. BASH (Bourne Again SHell) and Zsh (Z Shell) are the most popular shell programs.

We've already interacted with the command line, terminal, and shell through our installation instructions.

### Let's do an exercise together

1. Open the [cheatsheet](command-line-cheatsheet). Copying is encouraged in coding, so make sure you use the cheatsheet!

2. Create a directory called `workspace` in your home directory.

```sh
mkdir ~/workspace
```

3. Create the following directory structure in your `workspace` directory, using `mkdir`.

    ```sh
    workspace
    +-- cli
        +-- practice
            +-- create
    ```

4. Enter (change) into the `create` directory, using `cd`. Remember to use tab completion.
2. While in this directory, create a new file named `is310`.

    ```sh
    touch is310
    ```

3. Put some simple content in the file using the `echo` command.

    ```sh
    echo 'Coding is ...' > is310
    ```

4. Now use the `cat` command to read those contents.

    ```sh
    cat is310
    ```

5. Remove the `is310` file you created earlier with the `rm` command.
6. `cd` back up to the `cli` directory.
7. Remove the `practice` directory and all of its contents.

Let's dive further through the following tutorials developed by [Melanie Walsh](https://melaniewalsh.org/):

- [https://melaniewalsh.github.io/Intro-Cultural-Analytics/01-Command-Line/01-The-Command-Line.html#command-line-cheatsheet](https://melaniewalsh.github.io/Intro-Cultural-Analytics/01-Command-Line/01-The-Command-Line.html#command-line-cheatsheet)

## Command Line Assignment

### Time to get lost in the Command Line

*In Class Assignment:*

1. First, using the command line commands and your terminal create a series of nested directories and files.

- At least one your directories needs to have nothing in it.
- At least one of your directories needs to have a file with the text, "You're lost" on it.
- At least one your directories, needs to have a file with the text "You've made it to the center of the maze!"

2. Once you've completed your corn maze, pair up with another student and have them try and navigate to the center of your maze using command line commands.
   - Since we're virtual, feel free to share your via ~~discord~~ [google drive folder](https://drive.google.com/drive/folders/1JF2viPdcFmQUDcTmsx_K7cEsTdXIKHgS?usp=sharing) with your classmates.

![maze](https://media.giphy.com/media/Xbn2CXq5u2Wc0/giphy.gif)

*Additional/Homework Assignment:*
Following [Melanie Walsh's working with Text Files in the command line tutorial](https://melaniewalsh.github.io/Intro-Cultural-Analytics/01-Command-Line/01-The-Command-Line.html#working-with-files-and-texts), complete the following steps:

1. Select a book from [Project Gutenberg](https://www.gutenberg.org/ebooks/search/) and download a text file version using the command line (you can use the [wget](https://www.gnu.org/software/wget/manual/wget.html) command or [curl](https://curl.se/docs/manpage.html) command).
2. Using the command line, rename your downloaded file to be the title of the book.
3. Count the number of words in your book file and print the result to the screen.
4. Search for a word (would recommend not using "the") in your book file and print the number of times it appears.
5. Take a 📸 screenshot of your output and send it to the instructor in discord.

### More Information

#### In Depth Dive into the Command Line and Shells

At its base, a shell is simply a macro processor that executes commands. The term macro processor means functionality where text and symbols are expanded to create larger expressions.

A bash shell is both a command interpreter and a programming language. As a command interpreter, the shell provides the user interface to the rich set of utilities for your operating system. The programming language features allow these utilities to be combined. Files containing commands can be created, and become commands themselves. These new commands have the same status as system commands in directories such as /bin, allowing users or groups to establish custom environments to automate their common tasks.

Shells may be used interactively or non-interactively. In interactive mode, they accept input typed from the keyboard. When executing non-interactively, shells execute commands read from a file.

Shells also provide a small set of built-in commands (builtins) implementing functionality impossible or inconvenient to obtain via separate utilities. For example, cd, break, continue, and exec cannot be implemented outside of the shell because they directly manipulate the shell itself. The history, getopts, kill, or pwd builtins, among others, could be implemented in separate utilities, but they are more convenient to use as builtin commands. All of the shell builtins are described in subsequent sections.

While executing commands is essential, most of the power (and complexity) of shells is due to their embedded programming languages. Like any high-level language, the shell provides variables, flow control constructs, quoting, and functions.

Shells offer features geared specifically for interactive use rather than to augment the programming language. These interactive features include job control, command line editing, command history and aliases.

### Resources

1. Ian Milligan and James Baker, "Introduction to the Bash Command Line," *The Programming Historian* 3 (2014), [https://programminghistorian.org/en/lessons/intro-to-bash]. This is an introduction to the Bash shell, which will serve well enough as an introduction to other shells like Zsh as well.
2. [Bash Basics Part 1 of 8 | Access and Navigation](https://youtu.be/eH8Z9zeywq0?t=885)
3. [Beginner's Guide to the Bash Terminal](https://www.youtube.com/watch?v=oxuRxtrO2Ag)
4. [The Most Important Thing You'll Learn in the Command Line](https://www.youtube.com/watch?v=q7-aEspwwEI)
5. Go through the CodeAcademy [command line course](https://www.codecademy.com/learn/learn-the-command-line).
6. [Shell Scripting Tutorial](https://www.youtube.com/watch?v=hwrnmQumtPw)

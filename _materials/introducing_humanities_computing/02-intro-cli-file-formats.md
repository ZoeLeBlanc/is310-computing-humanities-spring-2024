---
title: "Introduction to the Command Line and File Formats"
permalink: /materials/introducing-humanities-computing/05-intro-cli-file-formats/
excerpt: "An introduction to the Command Line and File Formats"
toc: true
---


- why work with the command line
  - example of commands
    - Command Line Cheatsheet
- coding with GitHub CoPilot
  - in class exercise
    - creating folders
      - creating files
    - adding text to a file
    - searching for text in a file
    - counting words in a file
    - deleting a file
- Tips
  - tab auto-complete
  - up arrow to scroll through previous commands
  - ctrl + a to go to the beginning of the line you are currently typing on
  - ctrl + e to go to the end of the line you are currently typing on
  - ctrl + r to search through previously used commands
  - ctrl + c to kill whatever you are running
  - exit to exit the current shell
- intro to file formats
  - proprietary vs open source
  - Markdown and plain text

- Homework
  - command line assignment
  - file format assignment

<div class="notice--info">⚡️ This lesson has been adapted from and inspired by Melanie Walsh's Textbook <i>Introduction to Cultural Analytics & Python</i> <a href="https://melaniewalsh.github.io/Intro-Cultural-Analytics/01-Command-Line/01-The-Command-Line.html">https://melaniewalsh.github.io/Intro-Cultural-Analytics/01-Command-Line/01-The-Command-Line.html</a> and the Digital Humanities Research Institute's Workshop on the Command Line <a href="https://github.com/DHRI-Curriculum/command-line">https://github.com/DHRI-Curriculum/command-line</a>. Many thanks to all authors for sharing their materials!</div>

## Introducing the Command Line

So far, you have been installing software via something called the terminal, but we have yet to explain what the terminal is or how it works.

Terminals are a way to interact with your computer via **text** commands. Today, we give usually commands to a computer via a Graphical User Interface (GUI), pronounced "gooey". Any time you download an app, whether on your phone or computer, you are using a GUI. GUIs let us click on icons, drag items, and interact with our computers in a visual way. Terminals let us do many of the same functions, but we have to be more explicit and write these commands.

You've already experienced this when you checked your version of Python, for example, with this command `python3 --version`.

### What are Terminals?

To really understand what terminals are, we need to learn a bit about the history of computing.

<figure>
  <a href="https://www.computerhope.com/cdn/eniac.jpg">
    <img src="https://www.computerhope.com/cdn/eniac.jpg" alt="Early computer" class="image-popup">
  </a>
  <figcaption>Early computer <a href="https://www.computerhope.com/cdn/eniac.jpg">https://www.computerhope.com/cdn/eniac.jpg</a></figcaption>
</figure>

Back in the 1950s and 1960s, computers were the size of entire rooms and functioned through the use of something called punch cards.

<figure>
  <a href="https://theoreti.ca/wp-content/uploads/2016/03/IMG_1628.jpg">
    <img src="https://theoreti.ca/wp-content/uploads/2016/03/IMG_1628.jpg" alt="Example punch card from the Index Thomisticus, one of the first Computing in the Humanities projects started in the 1940s to digitize the writings of Thomas Aquinas" class="image-popup">
  </a>
  <figcaption>Example punch card from the Index Thomisticus, one of the first Computing in the Humanities projects started in the 1940s to digitize the writings of Thomas Aquinas. More information available here <a href="https://theoreti.ca/?p=6096">https://theoreti.ca/?p=6096</a></figcaption>
</figure>

As you can see in this example image, punch cards contained a series of holes that encoded information like numbers, letters, and even instructions for programs. These cards were fed into machines called card readers, translating the hole patterns into electrical signals the computer could understand. This enabled data entry for tasks like payroll calculations, statistical analysis, and even early gaming. The punch cards and computers were run by teams of *operator*, often comprised of women, who inputted these punch cards, prompting the computers to process and output the results on paper.

The term *terminal* then refers to the device that allowed operators to interact with the computer, and the *command line* refers to the text-based interface that allowed operators to input commands to the computer. The command line was the only way to interact with computers until the 1970s, when the first Graphical User Interface (GUI) was developed at Xerox PARC. This GUI was later adopted by Apple and Microsoft, and is the basis for the GUIs we use today.

Today when we use **terminals**, we are not just using the terminal but also using often using something called a **shell**. A "shell" is a program within a terminal that interprets user commands and processes computer output. Originating from the Unix operating system, the term "shell" signifies a user-friendly interface that encapsulates the complexities of various computer systems. Popular shell programs include **bash** (Bourne Again SHell), which is the default shell for most Linux distributions and MacOS; **PowerShell**, which is Windows default option, and **zsh** (Z Shell) -- the optional configuration from our course tools. Each shell has its own set of commands and syntax, but they all share the same basic functionality.

**The most important thing to understand is that the terminal is how you interface with the computer, the shell is the program that interprets your commands, and the command line is the text-based interface that allows you to input commands to the shell.**

To help make this more concrete, compare these two images from Melanie Walsh's textbook:

<figure>
  <a href="https://melaniewalsh.github.io/Intro-Cultural-Analytics/_images/GUI-example.gif">
    <img src="https://melaniewalsh.github.io/Intro-Cultural-Analytics/_images/GUI-example.gif" alt="GUI example" class="image-popup">
  </a>
</figure>

<figure>
  <a href="https://melaniewalsh.github.io/Intro-Cultural-Analytics/_images/CLI-example.gif">
    <img src="https://melaniewalsh.github.io/Intro-Cultural-Analytics/_images/CLI-example.gif" alt="CLI example" class="image-popup">
  </a>
</figure>

In the first image, we see that Melanie is using the Mac Finder App to interact graphically with her file folders. This app is a GUI, so she is clicking and moving files around with her mouse.

In the second image, we see that Melanie is using the terminal and typing commands to move files around. We can see that the top of her program says `bash`, indicating which shell she is using, and then she is typing commands like `mkdir` and `rmdir` to create and remove directories.

These images give you a sense of how the command line works, and how we use it. So let's start learning some commands!

### Working With The Command Line

From Melanie's example, we can see that the command to create a directory is `mkdir`. Let's try it out!

First, we need to open our terminal, which we can do through VS Code. To do this, click on the Terminal tab in the top menu bar and select New Terminal. This will open a new terminal window at the bottom of your screen.

Then we need to figure out the correct syntax or wording to use the `mkdir` command. We can see from Melanie's example that she types `mkdir` and then `Intro-CA-Notes`. 

```sh
mkdir Intro-CA-Notes
```

<figure>
  <a href="{{site.baseurl}}/assets/images/demo_terminal.png">
    <img src="{{site.baseurl}}/assets/images/demo_terminal.png" alt="Demo example" class="image-popup">
  </a>
</figure>

If we press enter, it should seem like this works but how do we know for sure? 

We have two options. First, we should take a look at the Command Line cheatsheet that contains a number of these commands





### In Class Exercise

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

## Introducing File Formats

This is a huge topic in LIS and CS but to put it simply a file is a collection of data stored in a single unit, identified by a filename. It can be a document, an image, a video, a sound, or any other collection of data. The file extension is the part of the file name after the period. For example, in the file name `DH-Tool.md`, the file extension is `.md`. The file extension tells the computer what type of file it is and what program to use to open it.

![file formats](https://www.filecenter.com/blog/wp-content/uploads/2022/04/The-Giant-List-of-Document-File-Types-and-Extensions.jpg)

There are many different file formats and each one has its own purpose. For example, a `.docx` file is a Microsoft Word document, a `.jpg` file is an image, and a `.mp3` file is an audio file. Some file formats are proprietary, meaning they are owned by a company and can only be opened by certain programs. For example, `.docx` files can only be opened by Microsoft Word. So if you try to open up a word document in a PDF Viewer you might see what looks like a bunch of gibberish.

![corrupted word doc](https://www.fonelab.com/images/data-retriever/fonelab-data-retriever-how-to-corrupt-a-word-file-doc-text-only.jpg)

This gibberish is actually the code that makes up the file, but since the PDF Viewer doesn't know how to read the code it just shows you the code itself rather than the data stored in the files.

Other file formats are open source, meaning they are not owned by a company and can be opened by many different programs. For example, `.txt` files are plain text files that can be opened by any text editor. 

### What is plain text and Markdown?

Plain text is a file format that only contains text and no formatting. It is the simplest file format and can be opened by any text editor. Markdown is a plain text file format that uses symbols to add formatting to the text. For example, if you want to make a word bold you would put two asterisks on either side of the word.

```
**bold**
```

If you want to make a word italic you would put one asterisk on either side of the word.

```
*italic*
```

If you want to make a list you would put a dash in front of each item.

```
- item 1
- item 2
- item 3
```

If you want to make a heading you would put a hashtag in front of the heading.

```
# heading 1
## heading 2
### heading 3
```

These types of file formats are incredibly popular in DH for a few reasons. First, they are free to use and are more sustainable long term since they do not require specialized software to open. Second, this interoperability makes them easier to share and collaborate on, as well as use in a variety of DH Tools. Finally, the use of such file formats also preserves this data for future use. For example, if you have a `.docx` file and Microsoft Word goes out of business, you will no longer be able to open that file. However, if you have a `.txt` file you will always be able to open it in any text editor. 

The key thing to understand is that every file format has a history and is the product of multiple decisions and communities. In the case of Markdown, it was created by John Gruber with help from Aaron Swartz in 2004. The goal was to create a file format that was easy to read and write, and could be converted into HTML. They also wanted to create a file format that was easy to use and could be used by anyone. You can read more about the history of Markdown, in Bednarski, Dawid. “The History of Markdown: A Prelude to the No-Code Movement.” Taskade Blog, March 25, 2022. [https://www.taskade.com/blog/markdown-history/](https://www.taskade.com/blog/markdown-history/).

It's important to understand that Markdown has this history because many flavors of Markdown exist, and standardization of Markdown has been an ongoing project. For example, GitHub Flavored Markdown (GFM) is a flavor of Markdown that was created by GitHub in 2009. It is a superset of Markdown, meaning it adds additional features to Markdown. For example, GFM allows you to create tables in Markdown, which is not possible in regular Markdown. You can read more about GFM in “GitHub Flavored Markdown Spec.” GitHub, 2022. [https://github.github.com/gfm/](https://github.github.com/gfm/).

![markdown flavors](https://d11a6trkgmumsb.cloudfront.net/original/3X/c/b/cb7374a606a66c5b8e489afed76d93ed49dc7836.png)

This figure shows some examples of how Markdown is written depending on the Platform and standards. You can also see some of the discussions that go on to help shape these standards through the various repositories on GitHub that host the standards. For example, CommonMark is another popular Markdown style and improvements to it are discussed in this repository [https://github.com/commonmark/commonmark-spec/issues](https://github.com/commonmark/commonmark-spec/issues).

## Popular File Formats in DH

Understanding some of the tradeoffs and histories of file formats helps us consider increasingly popular file formats in DH. We have already discussed Markdown, but we will also be looking at two others: `JSON` and `CSV`.

### JSON

![json example](https://www.softwaretestinghelp.com/wp-content/qa/uploads/2017/12/Including-Car-in-Employee-JSON.jpg)

JSON stands for JavaScript Object Notation and is a file format that stores data in a key-value pair. For example, if you wanted to store our data from assignments this week you might write it like this:

```
{
  "DH Tool": "GitHub",
  "Found by": "Zoe LeBlanc"
}
```

This file format is popular in DH because it is easy to read and write, and can be used in a variety of programming languages. It is also a popular file format for sharing data across the web. You can read more about JSON in “JSON: JavaScript Object Notation.” MDN Web Docs, 2022. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON).

We won't be using this file format much in this course, but it's important to know it exists since many datasets are available as JSON files. These files will have the file ending of `.json` and will always have the curly brackets, and values separated by colons and listed with commas.

### CSV

![csv example](https://static.tildacdn.com/tild3262-3665-4232-b835-303031616463/Screenshot_2022-04-2.png)

The other incredibly popular file format that you likely have already used before and that we will use a lot in this course is CSV. CSV stands for Comma Separated Values and is a file format that stores data in a table. For example, if you wanted to store our data from assignments this week you might write it like this:

```
DH Tool, Found by
GitHub, Zoe LeBlanc
```
CSVs are a usually read by spreadsheet software, like Excel or Google Sheets and have the file ending of `.csv`. Unlike `.xlsx` files, which are proprietary to Microsoft Excel, CSVs are open source and can be opened by any spreadsheet software. 

![excel vs csv](https://miro.medium.com/v2/resize:fit:1400/1*eGVQ8M6mgERo8WFMUjYjZA.jpeg)

CSVs have a long history as well and the file format was first created in the 1970s. But as we we will discuss more next week, the act of putting data into tables has an even longer history.

![punch card](https://imgur.com/V5mfB2w.jpg)

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



### Resources

1. Ian Milligan and James Baker, "Introduction to the Bash Command Line," *The Programming Historian* 3 (2014), [https://programminghistorian.org/en/lessons/intro-to-bash]. This is an introduction to the Bash shell, which will serve well enough as an introduction to other shells like Zsh as well.
2. [Bash Basics Part 1 of 8 | Access and Navigation](https://youtu.be/eH8Z9zeywq0?t=885)
3. [Beginner's Guide to the Bash Terminal](https://www.youtube.com/watch?v=oxuRxtrO2Ag)
4. [The Most Important Thing You'll Learn in the Command Line](https://www.youtube.com/watch?v=q7-aEspwwEI)
5. Go through the CodeAcademy [command line course](https://www.codecademy.com/learn/learn-the-command-line).
6. [Shell Scripting Tutorial](https://www.youtube.com/watch?v=hwrnmQumtPw)

- Command Line might sounds a bit intimidating
- But ask yourself, how do you find files and manipulate files on your computer? Probably using Windows Explorer or Mac Finder, right?
- Command Line is a text-based way of doing the same thing you do with your files
- Command Line is used a lot in coding because we manipulate our code files and run them all in the terminal
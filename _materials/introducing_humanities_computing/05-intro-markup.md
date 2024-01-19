---
title: "Introduction to Markup and Documents"
permalink: /materials/introducing-humanities-computing/05-intro-markup
excerpt: "An introduction to markup languages and documents."
toc: true
---

- Intro to Markdown
- Intro to HTML

### Introducing Markdown

While `.txt` files are useful, in digital humanities we often use a file format called Markdown. Like txt, Markdown is a plain text file format that uses symbols to add formatting to the text, and has the file extension `.md`. 

Let's try creating a Markdown file in our folder. We can do this by using the `touch` command and adding `.md` to the end of the file name.

```sh
touch is310-computing-humanities.md
```

Now we can open this file in VS Code and add some text to it. We can also add some formatting to it using Markdown.

First, let's add some text to the file. We can do this by typing in the file in VS Code. Then we can save the file by pressing `command + s` on a Mac or `control + s` on a PC. Now we can see the text we added to the file in VS Code.

```md
Computing in the Humanities is defined as the application of computational methods and tools to the study of humanistic questions.
```

Now if we wanted too, we could add some formatting to this text using Markdown.

Maybe we want to highlight the word "Computing in the Humanities" in bold. To do this we would put two asterisks on either side of the word.

```md
**Computing in the Humanities** is defined as the application of computational methods and tools to the study of humanistic questions.
```

We could also put `defined` into italics by putting one asterisk on either side of the word.

```md
**Computing in the Humanities** is *defined* as the application of computational methods and tools to the study of humanistic questions.
```

Finally, we could add a heading to this text by putting a hashtag in front of the heading.

```md
# Welcome to Computing in the Humanities
```

These types of file formats are incredibly popular for a few reasons. First, they are free to use and are more sustainable long term since they do not require specialized software to open. Second, this interoperability makes them easier to share and collaborate with. Finally, the use of such file formats also preserves this data for future use. For example, if you have a `.docx` file and Microsoft Word goes out of business, you will no longer be able to open that file. However, if you have a `.txt` file you will always be able to open it in any text editor.

The key thing to understand is that every file format has a history and is the product of multiple decisions and communities. In the case of Markdown, it was created by John Gruber with help from Aaron Swartz in 2004. The goal was to create a file format that was easy to read and write, and could be converted into HTML. They also wanted to create a file format that was easy to use and could be used by anyone. You can read more about the history of Markdown, in Bednarski, Dawid. “The History of Markdown: A Prelude to the No-Code Movement.” *Taskade Blog*, March 25, 2022. [https://www.taskade.com/blog/markdown-history/](https://www.taskade.com/blog/markdown-history/).

It's important to understand that Markdown has this history because many flavors of Markdown exist, and standardization of Markdown has been an ongoing project. For example, GitHub Flavored Markdown (GFM) is a flavor of Markdown that was created by GitHub in 2009. It is a superset of Markdown, meaning it adds additional features to Markdown. For example, GFM allows you to create tables in Markdown, which is not possible in regular Markdown. You can read more about GFM in “GitHub Flavored Markdown Spec.” GitHub, 2022. [https://github.github.com/gfm/](https://github.github.com/gfm/).

<figure>
  <a href="https://d11a6trkgmumsb.cloudfront.net/original/3X/c/b/cb7374a606a66c5b8e489afed76d93ed49dc7836.png">
    <img src="https://d11a6trkgmumsb.cloudfront.net/original/3X/c/b/cb7374a606a66c5b8e489afed76d93ed49dc7836.png" alt="Markdown Flavors" class="image-popup">
  </a>
</figure>

This figure shows some examples of how Markdown is written depending on the platform and standards. You can also see some of the discussions that go on to help shape these standards through the various repositories on GitHub that host the standards. For example, CommonMark is another popular Markdown style and improvements to it are discussed in this repository [https://github.com/commonmark/commonmark-spec/issues](https://github.com/commonmark/commonmark-spec/issues).


Usually when we create files, we notice that they have a few characters after a `.`, like `.doc` or `.csv` or `.txt.`. That's what is known as a file extension and it tells computers the file format, as well as which applications and programs can interact with that file. To see a full list of file formats, visit <https://en.wikipedia.org/wiki/List_of_file_formats>.

Under the Document heading <https://en.wikipedia.org/wiki/List_of_file_formats#Document>, you'll find many of the different standards that exist for working with documents specifically and also the usage of different file formats (so GDOC is a Google Drive Document for example).

The one we'll be using for writing documents in this course is called Markdown or MD. Markdown files end with `.md` extension and can be written in your text editor of choice. Also there are specific writing tools that can be used to write Markdown files, like [Ulysses](https://ulysses.app/) for Macs or [Ghostwriter](https://wereturtle.github.io/ghostwriter/) for Windows. Also if you use the popular tool, Notion.so it also exports to Markdown.

As some background for what Markdown is exactly,
> Markdown is a lightweight markup language for creating formatted text using a plain-text editor. John Gruber and Aaron Swartz created Markdown in 2004 as a markup language that is appealing to human readers in its source code form. From Wikipedia page <https://en.wikipedia.org/wiki/Markdown>

The big difference from writing in something like Word or Google Docs is that Markdown is a plain text format and that you don't use buttons to format your text. Instead, you directly format it with Markdown.

For example, if you wanted to write a header with a paragraph, you would write it like this:

```markdown
### This is a subheading

Here is a paragraph with a bolded word: **bolded**
```

Which renders in our browser like this:

---
### This is a subheading

Here is a paragraph with a bolded word: **bolded**

---

This may seem like a lot of extra work, but the advantages of Markdown are numerous.

1. It is much more sustainable than Word or Google Docs. This is because the text is saved as plain text and not in a format that is optimized for editing. This makes it future-proof so that you don't require a license or access to an application to see your files.
2. It can also be rendered by any text editor. This is because Markdown is a plain text format and not a rich text format. This makes it platform agnostic.
3. Finally, Markdown plays nicely with Github, which renders it directly in your browser. This makes it easy to push up your files into your repositories.

If you are new to using Markdown or have some questions about some syntax we have been using, I highly recommend you take a look at the following resources.

1. Sarah Simpkin, "Getting Started with Markdown," *Programming Historian* 4 (2015), <https://doi.org/10.46430/phen0046>.
2. Then for more depth, you could also check out the Markdown Guide's Getting Started page <https://www.markdownguide.org/getting-started/>
3. The Markdown Guide also has a series of helpful cheatsheets if you are looking for a quick reference:
    - Cheatsheet for Markdown Basics <https://www.markdownguide.org/cheat-sheet/>
    - Basic Syntax <https://www.markdownguide.org/basic-syntax/>
    - Extended Syntax <https://www.markdownguide.org/extended-syntax/>
4. And finally for Github-flavored Markdown (that is Markdown that is compatible with Github's Markdown syntax), you can check out <https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet>.

*Have any additional questions? Either ask them in our Discord or message the instructor*
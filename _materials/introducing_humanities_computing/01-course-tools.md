---
title: "Course Software & Tools"
permalink: /materials/introducing-humanities-computing/01-course-tools/
excerpt: "Instructions for setting up your computer for the course"
toc: true
---

In this course, we will be utilizing a number of different software platforms and tools. Some of the tools are optional, but are highly recommended. Setting up some of these tools will be easy, but others will expose you to some of the more frustrating aspects of working with computers. The best representation of what I'm talking about is this [xkcd comic, entitled Dependency](https://xkcd.com/2347/).

<figure>
   <img src="https://imgs.xkcd.com/comics/dependency.png" alt="Dependency" style="width:100%" class="image-popup">
   <figcaption>Dependency by Randall Munroe</figcaption>
</figure>

Essentially, modern software is a bit of a house of cards, and it's not uncommon to spend hours trying to get something to work, only to find out that you were missing a single character in a configuration file or have some conflicting dependency. The key thing to know is that this is not a reflection of your ability to work with computers, but rather a reflection of the state of modern software. In fact, an HCI professor wrote an excellent post about how this type of configuration errors can deter students (you can read a bit about that here [https://www.kevinbrowne.ca/command-line-bullshittery-and-other-realities-of-computing/](https://www.kevinbrowne.ca/command-line-bullshittery-and-other-realities-of-computing/)).

So, the key thing here to know is that you should try your best to follow these instructions, but if you get stuck, please reach out to the instructor (especially if you've been trying for more than ~20 minutes). 

The following are the tools/software/programming languages we will be using in this course, listed in order of complexity of installation:

## Slack

<figure>
   <img src="{{site.baseurl}}/assets/images/dh_slack.png" alt="Our Slack Channel on DH@UIUC Slack Team" style="width:100%" class="image-popup">
   <figcaption>Our Slack Channel on DH@UIUC Slack Team</figcaption>
</figure>

Slack is a communication tool that we will use for this course. You can download the app for your computer or use the web version. You can also download the app for your phone. You will need to create an account and join the course channel `is310-2024` on `DH@UIUC` team. The link to join Slack is available on Canvas and in the syllabus, and you can add yourself to our channel or ask the Instructors for assistance. 

I realize that Slack is less popular than a platform like Discord, but it is a very popular platform for Digital Humanities. In fact, the primary `DH Slack` Team is a great place to ask questions and get help from other DHers. You can read more about it and how this field uses Slack in this writeup by Amanda Visconti [https://literaturegeek.com/2016/07/06/digital-humanities-slack-community-design](https://literaturegeek.com/2016/07/06/digital-humanities-slack-community-design).

You are welcome to make any username you want, but please be sure to share who you are in the course channel so we can all get to know each other.

## Hypothesis

For our collective annotations, we will be using the Hypothesis platform. You can sign up for Hypothesis here [hypothes.is/signup]( hypothes.is/signup) and join our collective group at the link in our syllabus or via Canvas. You will need to install the Hypothesis Browser Extension for your preferred browser as well. You should follow the instructions available in this Quick Start Guide [https://web.hypothes.is/help/quick-start-guide/](https://web.hypothes.is/help/quick-start-guide/).

You are welcome to make your username whatever you choose, but please share your username with the instructor. And please be sure to make your annotations in our hypothes.is group `is310-2024` and that these annotations are public. For more about using Hypothesis groups, see this guide [https://web.hypothes.is/help/annotating-with-groups/](https://web.hypothes.is/help/annotating-with-groups/).

<figure>
   <img src="https://d242fdlp0qlcia.cloudfront.net/uploads/2018/03/21135305/scopeselector-groupname-1024x585.png" alt="Hypothesis Annotation" style="width:100%" class="image-popup">
   <figcaption>Hypothesis Annotation</figcaption>
</figure>

## GitHub

If you do not already have a GitHub account, you will need to sign up for an account for this course. For those unfamiliar, GitHub is a a collaborative version control platform that was first founded in 2007 and since then has begun the defacto platform for writing and sharing code; though other platforms do exist, like [GitLab](https://about.gitlab.com/) or [Bitbucket](https://bitbucket.org/product). Nonetheless, we will be using GitHub in this course, in part because it is also very popular for digital humanities research. As a perhaps crude search option, I would actually recommend searching for `digital humanities` on the platform [https://github.com/search?q=digital%20humanities&type=repositories](https://github.com/search?q=digital%20humanities&type=repositories) or taking a look at the number of repositories on Github tagged as `digital-humanities` [https://github.com/topics/digital-humanities](https://github.com/topics/digital-humanities). 

<figure>
   <img src="{{site.baseurl}}/assets/images/dh_github.png" alt="Digital Humanities Repositories on GitHub" style="width:100%" class="image-popup">
   <figcaption>Digital Humanities Repositories on GitHub</figcaption>
</figure>

GitHub is free to use (part of its popularity) and once you have an account you can store code and related materials (like datasets, for example) remotely, while also working collaboratively on these materials. The platform primarily consists of users, organizations (which users can join), and repositories (often called “repos” that are akin to folders or directories) for storing materials. In many ways, GitHub is similar to Google Drive, allowing users to both upload, organize, and keep versioned histories of their files. However, unlike Google Drive or other research management platforms, GitHub is also a platform for social coding, where users can publicly work on projects together, follow one another, comment on each other’s work, and view each other’s activity (somewhat like Twitter, Mastodon, Bluesky, etc…). 

We will be delving into GitHub's functionality in the next few weeks, but first you will need to sign up for an account. You can sign up for an account here [https://github.com/join](https://github.com/join). GitHub provides additional documentation on [signing up for an account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account). In terms of selecting a username, I would recommend choosing something that you plan to use professionally.

Once you have an account, you will also need to sign up for the GitHub Education Global Campus account [https://education.github.com/benefits](https://education.github.com/benefits). You can find step-by-step instructions on how to sign up here [https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-global-campus-for-students/apply-to-github-global-campus-as-a-student](https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/github-global-campus-for-students/apply-to-github-global-campus-as-a-student), but you will need to use your `@illinois.edu` email and show proof of your student status (either ID or academic record).

Getting approved might take a few days, but once you are approved, you will be able to not only create private repositories for free (we will get into what repositories are soon), but also use GitHub's AI coding tool called Co-Pilot. Both GitHub and Co-Pilot are owned by Microsoft, which acquired the platform in 2018 for 7.5 Billion dollars. While these platforms and tools are useful, they are also political and you can read more about the politics of GitHub here [https://www.theverge.com/2020/6/12/21288971/github-black-lives-matter-police-abuse-regrets-hubert-palmer](https://www.theverge.com/2020/6/12/21288971/github-black-lives-matter-police-abuse-regrets-hubert-palmer).

Mackenzie, Adrian. “48 Million Configurations and Counting: Platform Numbers and Their Capitalization.” Journal of Cultural Economy 11, no. 1 (January 2, 2018): 36–53. https://doi.org/10.1080/17530350.2017.1393443. p. 37

## AI Coding with GitHub Co-Pilot

As part of our course, we will be using GitHub's new AI coding tool called Co-Pilot. Co-Pilot is a tool that uses machine learning to suggest code as you write. It is a bit like the auto-complete feature in Google Docs, but instead of just suggesting words, it suggests entire lines of code. You can read more about it here [https://copilot.github.com/](https://copilot.github.com/).

As a student on GitHub, you should be able to get free access to Co-Pilot. You can read more about how to get access here [https://docs.github.com/en/github/copilot/getting-started-with-github-copilot](https://docs.github.com/en/github/copilot/getting-started-with-github-copilot). 

If for whatever reason you cannot get access, please let the instructor know and we can try and find a solution. Other tools that may be of use include ChatGPT (the free 3.5 version) or gpt4all (which is a bit more complicated to set up).

## VS Code

We will be using Visual Studio Code (VS Code) as our primary code editor for this course. You can download VS Code here [https://code.visualstudio.com/](https://code.visualstudio.com/), though I would highly recommend you download the `Insiders Edition` [https://code.visualstudio.com/insiders/](https://code.visualstudio.com/insiders/). You should be able to use the link above to download VS Code for Windows, Mac, and Linux.

Like GitHub and Co-Pilot, VS Code is also owned by Microsoft, which is why all three work relatively well together. VS Code is something called a Integrated Development Environment (IDE), which is a fancy way of saying it is a program for writing code. You can read more about IDEs here [https://en.wikipedia.org/wiki/Integrated_development_environment](https://en.wikipedia.org/wiki/Integrated_development_environment). Other popular IDEs include Atom, Sublime Text, and PyCharm. While you are welcome to use any IDE you want, I will be using VS Code in this course and I'm not sure that Co-Pilot works with other IDEs, so would highly encourage you to at least test it out.


<figure>
   <img src="https://i.stack.imgur.com/2xI4w.png" alt="Visual Studio Code" style="width:100%" class="image-popup">
   <figcaption>Visual Studio Code</figcaption>
</figure>

Another benefit of getting used to VS Code is that you can use it in the browser for any Github repository by changing `.com` to `.dev`. So for example if you took the link to our reposition, `https://github.com/ZoeLeBlanc/is310-computing-humanities-2024` and switched it to `https://github.dev/ZoeLeBlanc/is310-computing-humanities-2024`, you would see the VS Code version of our repository in the browser.

### Installation for Mac Users

For Macs, you will need to check if you have an `Intel Chip` or an `Apple Silicon`. You can check this by going to the Apple menu  > About This Mac.

![Mac chip](https://cdsassets.apple.com/live/7WUAS350/images/mac/macos-ventura-mac-mini-m2-pro-2023-apple-menu-about-this-mac.png)

You can see in this example the Chip says `Apple M2 Pro`, which means this is an `Apple Silicon`. If you see `Intel` then you have an `Intel Chip`. Download the appropriate version for your computer through selecting the `zip` option and then opening and installing the program.

### Installation for Windows Users

For Windows, you will need to check if you have a `64-bit` or `Arm64` operating system. You can check this by going to `Settings > System > About` and looking at the `System type` field.

![Windows chip](https://www.tenforums.com/attachments/tutorials/325540d1617307951-how-check-if-processor-32-bit-64-bit-arm-windows-10-a-arm_processor_settings.png)

Once identified, you should select the User Installer option and then open and install the program.

## Terminal & Oh-My-Zsh (Optional)

We will discuss more in-depth what terminals are in our Command Line session, but for now, you should know that a terminal is a bit like an app for working with files, but instead of clicking on icons, you write commands. You can read more about terminals here [https://en.wikipedia.org/wiki/Command-line_interface](https://en.wikipedia.org/wiki/Command-line_interface).

Installing a separate terminal is completely optional since VS Code has a built in terminal, but in case you would like to try it out, I recommend iTerm2 [https://iterm2.com/](https://iterm2.com/) for Mac and the new Windows Terminal [https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701) for Windows (for more info about Windows Terminal see [this blog post](https://towardsdatascience.com/new-windows-terminal-the-best-you-can-have-9945294707e7)). You should be able to use both these links to download the appropriate version for your operating system, but **please let the instructor know if you are having problems**.

Once you have installed your terminal, you can customize it to be a little more human readable through using Oh-My-Zsh [https://ohmyz.sh/](https://ohmyz.sh/). [Zsh is a unix shell](https://en.wikipedia.org/wiki/Z_shell) and should be already installed on your Mac. If not though you can install with the following:

```bash
sudo apt install zsh
```

Then you install oh-my-zsh with the following:

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```


## Python

In this course, you'll be writing code in a few different programming languages, but we'll primarily be using Python. Given that's the case, you have the option of primarily working in the cloud, through Google Colab [https://research.google.com/colaboratory/](https://research.google.com/colaboratory/).

You can read more about Colab here [https://research.google.com/colaboratory/faq.html](https://research.google.com/colaboratory/faq.html) and it is a popular platform for those needing GPU resources. However, that's likely to be a fairly exceptional likelihood for this class. Nonetheless, you could complete a lot of the homework assignments through this platform, *so I'm letting you choose how you would prefer to work*.

As an alternative, I am hoping that I can help everyone get setup to write code locally (as in on your computer). Setting up a computer to write code can be tedious and frustrating, but it is usually useful and will hopefully help with other courses as well. Also you can still use Colab if you want, even after we get everything running locally!

To work locally, I recommend that you download two things: a code editor and a terminal or console. A code editor is a bit like word processing software specifically for writing code (though you can also just write text in it), and a terminal is a bit like an app for working with files, but instead of clicking on icons, you write commands.




##### Code Editors

![VS Code](https://code.visualstudio.com/assets/docs/editor/whyvscode/macwinlinux2.png)

For the code editor, I highly recommend that you download and use Visual Studio Code (VS Code) [https://code.visualstudio.com/](https://code.visualstudio.com/). You should be able to use the link above to download VS Code for Windows, Mac, and Linux.



##### Terminals



<h3 id="selecting-programming-language">Installing our programming languages</h3>

In the following sections, we'll go through how to get your computer set up so that you are ready for the course. Follow the instructions for your computer type (`Windows` = any computer running windows, `Mac` = any apple computer) Most of the instructions involve clicking on links to follow instructions and pasting text into your computer. If you get stuck or have any problems, please message on Discord or email the instructor.

<h4 id="windows-installation">Windows</h4>

##### Installing WSL

We'll be following the instructions for using Python for web development on Windows [https://docs.microsoft.com/en-us/windows/python/web-frameworks](https://docs.microsoft.com/en-us/windows/python/web-frameworks).

First step is to install the Windows Subsystem for Linux following these steps [https://docs.microsoft.com/en-us/windows/python/web-frameworks#install-windows-subsystem-for-linux](https://docs.microsoft.com/en-us/windows/python/web-frameworks#install-windows-subsystem-for-linux).

In either PowerShell or Command Prompt, run the following command:

```PowerShell
wsl --install
```

According to the instructions:
> This command will enable the required optional components, download the latest Linux kernel, set WSL 2 as your default, and install a Linux distribution for you (Ubuntu by default, see below to change this).

> The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for files to de-compress and be stored on your machine. All future launches should take less than a second.

FYI: You will need to restart your machine during this installation process.

After this you'll need to setup your WSL environment following these instructions [https://docs.microsoft.com/en-us/windows/wsl/setup/environment](https://docs.microsoft.com/en-us/windows/wsl/setup/environment).

Specifically you'll need to set up your Linux username and password [https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password).

![WSL Setup](https://docs.microsoft.com/en-us/windows/wsl/media/ubuntuinstall.png)

Once setup I would recommend first checking which version of WSL you are running and upgrading to WSL 2 if you are not already using it [https://docs.microsoft.com/en-us/windows/wsl/install#check-which-version-of-wsl-you-are-running](https://docs.microsoft.com/en-us/windows/wsl/install#check-which-version-of-wsl-you-are-running). And then I would recommend updating your packages for Ubuntu [https://docs.microsoft.com/en-us/windows/wsl/setup/environment#update-and-upgrade-packages](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#update-and-upgrade-packages).

##### Customizing Windows Terminal and VS Code

Now that you have WSL installed, you can customize your Windows Terminal. I recommend using the [https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-windows-terminal](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-windows-terminal) guide to customize your terminal.

You should also familiarize yourself with working with files in WSL [https://docs.microsoft.com/en-us/windows/wsl/setup/environment#file-storage](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#file-storage).

Now you can get VS Code working with WSL by following these installation instructions for working with the Remote WSL Extension [https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode#install-vs-code-and-the-remote-wsl-extension](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode#install-vs-code-and-the-remote-wsl-extension).

According to the docs:
> In order to install the Remote-WSL extension, you will need the 1.35 May release version or later of VS Code. We do not recommend using WSL in VS Code without the Remote-WSL extension as you will lose support for auto-complete, debugging, linting, etc. Fun fact: this WSL extension is installed in $HOME/.vscode/extensions (enter the command ls $HOME\.vscode\extensions\ in PowerShell).

Now you can open Windows Terminal and type:

```bash
code .
```

And that should start your VS Code Server
![VS Code Server](https://docs.microsoft.com/en-us/windows/wsl/media/wsl-open-vs-code.gif)

OR you can open VS Code and follow these instructions:
> You can also access more VS Code Remote options by using the shortcut: CTRL+SHIFT+P in VS Code to bring up the command palette. If you then type Remote-WSL you will see a list of the VS Code Remote options available, allowing you to reopen the folder in a remote session, specify which distribution you want to open in, and more.

![VS Code Remote Options](https://docs.microsoft.com/en-us/windows/wsl/media/vscode-remote-command-palette.png)

Finally, we can customize our Windows Terminal to be a little more human readable through using Oh-My-Zsh [https://ohmyz.sh/](https://ohmyz.sh/).

[Zsh is a unix shell](https://en.wikipedia.org/wiki/Z_shell) and should be already installed on your WSL system. If not though you can install with the following:

```bash
sudo apt install zsh
```

Then you install oh-my-zsh with the following:

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![install zsh](https://res.cloudinary.com/practicaldev/image/fetch/s--HnDFRLC1--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5qpu02quwb9iwo6gguxg.png)

You can find more in depth instructions here [https://dev.to/contactsunny/installing-zsh-and-oh-my-zsh-on-windows-11-with-wsl2-1p5i](https://dev.to/contactsunny/installing-zsh-and-oh-my-zsh-on-windows-11-with-wsl2-1p5i)

To learn more about zsh and terminals, check out this in-depth guide from The Missing Semester of Your CS Education [https://missing.csail.mit.edu/2020/course-shell/](https://missing.csail.mit.edu/2020/course-shell/) and [https://missing.csail.mit.edu/2020/command-line/](https://missing.csail.mit.edu/2020/command-line/).

##### Installing Python and Git

Now we're finally ready to install Python and Git 🥳! Luckily Python is already installed on Windows Subsystem for Linux, so this is relatively easy.

Just follow the three steps in these instructions [https://docs.microsoft.com/en-us/windows/python/web-frameworks#install-python-pip-and-venv](https://docs.microsoft.com/en-us/windows/python/web-frameworks#install-python-pip-and-venv) and you should be set to go.

Installing git is a little more complex and something we'll be working through primarily on Thursday. However for those that are ready to continue, please follow these instructions [https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git). Specifically, you'll need to install git into your WSL environment, configure git to work with your **Github account** username and email, and then set up the Git Credential Manager [https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git#git-credential-manager-setup](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git#git-credential-manager-setup).

<h4 id="mac-installation">Mac</h4>

##### Installing Python and Oh-My-Zsh

The instructions for installing Python are a little less convoluted on a Mac since it is already running a Unix OS (though we might hit some issues if anyone has a new M1 chip macbook). We'll largely be following the instructions from [https://docs.python-guide.org/starting/install3/osx/](https://docs.python-guide.org/starting/install3/osx/).

First step is to open iTerm2 and run the following command:

```bash
python --version
```

That should show you the version of Python you have installed, and it is likely going to be 2.7 since that ships with Mac. Unfortunately, that version is now officially retired and so will you might come across a library or two using it, you'll end with a lot of errors if we don't upgrade (also you can check the old countdown clock for the migration from Python 2 to 3 [https://pythonclock.org/](https://pythonclock.org/)).

To upgrade our version of Python, first we'll need to install X-Code and [Homebrew](https://brew.sh/).

In our iTerm2 window, run the following command:
  
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once that's complete install Xcode Command Line Tools, by typing into the terminal:

```sh
xcode-select --install
```

Now we'll tell our computer to use Homebrew by adding a line to our ~/.zshrc file:

```sh
open ~/.zshrc
```

This should open your file in a text editor. Add the following line to the bottom of the file, and then press save and exit:

```sh
export PATH="/usr/local/opt/python/libexec/bin:$PATH"
```

Finally back in iTerm2, run the following command:

```sh
source ~/.zshrc
```

Now you can install Python with brew:

```sh
brew install python
```

Finally, we can customize our iTerm2 to be a little more human readable through using Oh-My-Zsh [https://ohmyz.sh/](https://ohmyz.sh/).

[Zsh is a unix shell](https://en.wikipedia.org/wiki/Z_shell) and should be already installed on your Mac.

Install oh-my-zsh with the following:

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![install zsh](https://res.cloudinary.com/practicaldev/image/fetch/s--HnDFRLC1--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5qpu02quwb9iwo6gguxg.png)

You can find more in depth instructions here [https://dev.to/hannahgooding/how-i-customise-my-terminal-with-oh-my-zsh-macos-427i](https://dev.to/hannahgooding/how-i-customise-my-terminal-with-oh-my-zsh-macos-427i)

To learn more about zsh and terminals, check out this in-depth guide from The Missing Semester of Your CS Education [https://missing.csail.mit.edu/2020/course-shell/](https://missing.csail.mit.edu/2020/course-shell/) and [https://missing.csail.mit.edu/2020/command-line/](https://missing.csail.mit.edu/2020/command-line/).

**CONGRATS YOU'VE SETUP YOUR COMPUTER 🎉**

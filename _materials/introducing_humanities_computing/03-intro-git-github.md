---
title: "Introduction to GitHub"
permalink: /materials/intro-github-git/01-intro-github
excerpt: "An introduction to GitHub"
toc: true
---

## What is GitHub?

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

GitHub is a web-based platform that allows you to host and version code-related projects, while also working collaboratively. The best analogy is to imagine a blend of a data management and collaborative work platform like Google Drive with a social media platform like Twitter. It uses Git, a version control system, which is confusingly different from GitHub (more about git available in the [next lesson]({{site.baseurl}}/materials/intro-github-git/02-intro-git)), to manage the history of a project. The platform was created in late 2007 and acquired by Microsoft in 2018[^1],and has become the largest global platform for hosting code, with the platform recently announcing that they had over 100 million of users.[^2]

![100 million users](https://github.blog/wp-content/uploads/2023/01/100million-header.png?resize=1200%2C627)

### Considerations and Criticisms

These numbers sound impressive, but should also be concerning. The consolidation of code and data on a single platform raises questions about the centralization of knowledge and the power of a single company to control the future of software development, if not all technology writ large. 

While alternatives to GitHub exist (primarily [GitLab](https://about.gitlab.com/) or [Bitbucket](https://bitbucket.org/product)), it is hard to overstate how much in the last decade GitHub has become the de facto platform for this type of work. Such a centralization is truly a double-edged sword. For example, GitHub has created what amounts to the largest code archive in the world through their GitHub Arctic Code Vault, an initiative to take a snapshot of all code hosted on their platform on February 2, 2020 and store it in the Svalbard Global Seed Vault. Such an initiative is impressive and was done in partnership with some academic institutions (the exact partners were the Long Now Foundation, the Internet Archive, the Software Heritage Foundation, Arctic World Archive, Microsoft Research, the Bodleian Library, and Stanford Libraries). But it also raises a number of ethical, archival, and political questions.

![arctic code vault]({{site.baseurl}}/assets/images/artic_code_vault.png)

For example, this Arctic Code Vault has been criticized for its erasure of the indigenous Sami people who live on Svalbard and its performative approach to archives.[^3] GitHub also has contracts with U.S. Immigrations and Customs Enforcement (ICE) led to protests and boycotts from some sectors of the developer community.[^4] While we plan to use this platform, it's important to do so with these issues in mind.

## Why Use GitHub for Digital Humanities?

While primarily marketed towards software developers, GitHub is also incredibly popular for digital humanities. It is widely used for hosting data sets, text corpora, and other scholarly research assets. It provides a central place to publish, discover, and collaborate on such resources. 

For instance, academic journals like the *Programming Historian* use GitHub for the entire publishing life cycle (you can explore for yourself [https://github.com/programminghistorian/jekyll](https://github.com/programminghistorian/jekyll)). You can get a sense of how popular GitHub is for digital humanities through searching for `digital-humanities` on the platform. 

![dh popularity]({{site.baseurl}}/assets/images/dh_github_popularity.png)

You'll notice that there's a number of categories on the left-hand side. Under `Filter By`, we have code, repositories, issues, pull requests, discussions, users, commits, packages, wikis, topics, marketplace. Then underneath, we have `Languages` which lists a series of programming languages. And finally we have `Advanced` which is a set of advanced filters that lets you search by date, owner, topic, etc...

We won't cover each of these in detail today, but there's a few you should become familiar with.

### Repositories

Repositories are the core of GitHub, and are essentially like folders in Google Drive. They are where all the files, code, and data for a project is stored, along with version histories of them. Repositories can be public or private. Public repositories are visible to anyone, while private repositories are only visible to the owner and collaborators.

You can view the activity on a repository by clicking on the `Insights` tab. This will show you a graph of the activity on the repository, including activity by contributors, under the `Contributors` tab.

[![contributors jekyll]({{site.baseurl}}/assets/images/contributors_jekyll.png)](https://github.com/programminghistorian/jekyll/graphs/contributors)

### Issues

Issues are a way to track bugs, feature requests, or other tasks related to a project. They are a way to track the development of a project and can be used to coordinate work between collaborators. Issues can be assigned to specific users, labeled, and commented on. They can also be closed when the issue is resolved.

![issue](https://docs.github.com/assets/cb-119863/mw-1440/images/help/issues/issue-assignees.webp)

### Discussions

You have all tried out discussions already! Discussions are a way to have threaded conversations about a project. They are similar to issues, but are more open-ended and can be used for general questions or conversations. They are a way to build community around a project.

![discussions](https://github.githubassets.com/images/modules/site/discussions/overview.png)

### Topics

While GitHub's search engine is powerful, one way to make your projects for findable is to add topics, which allows you to tag a repository with keywords.  For example, if you search for `digital-humanities` and then click on the `Topics` tab, you'll see a list of topics that are associated with repositories that have been tagged with `digital-humanities`. You can also see how many repositories have been tagged with each topic.

![dh topics]({{site.baseurl}}/assets/images/dh_topics.png)

### Users

You are all also familiar now with users, since you all have accounts on GitHub. While user profiles are somewhat self-explanatory, there's a number of features for users that are worth highlighting.

#### Profile

User profiles are where you can see all of a user's repositories, issues, and discussions. It's also where you can see their followers and who they are following. You can also see their activity on GitHub, including their contributions to repositories, issues, and discussions.

We can explore some of these features through my profile as an example.

[![leblanc profile]({{site.baseurl}}/assets/images/leblanc_github_profile.png)](https://github.com/ZoeLeBlanc)

#### Followers and Following

You can follow other users on GitHub, which allows you to see their activity on the platform. You can also see who is following you. This is a way to build community and find other users who are working on similar projects.

## In Class Lab Activity

### Creating Your First Repository

Now that we've explored some of the features of GitHub, let's create a repository. Again, remember repository is essentially a term for folder.

The folder or repository we are going to create today is going to be a place where you can store your work for this course. We'll be using this repository throughout the course, so it's important that you create it now.

To do this, click on the `New` button in the top right-hand corner of the screen. This will take you to a page where you can create a new repository.

![new repo](https://docs.github.com/assets/cb-31554/images/help/repository/repo-create.png)

Now you'll be asked to give it a name. Let's do our course name `is578-introduction-to-dh`. You can also add a description, choose whether it's public or private, and add a license (we'll discuss licenses later in the semester). 

![create repo](https://cdn-media-1.freecodecamp.org/images/mxGU5eGEki7FsedthUt8Vyi3uqAhL02FbmXF)

You can also initialize the repository with a README, which is a file that provides information about the project. You can also add a `.gitignore` file, which is a file that tells Git to ignore certain files in the repository. We'll talk more about this in the next lesson.

![first commit](https://material.bits.vib.be/topics/git-introduction/images/02-3-create-readme-repository.PNG)

Once you create your repository it should like the photo above. If you do not select the `Initialize this repository with a README` option, you will see a blank repository that looks like the photo below.

![empty repo](https://www.dataquest.io/wp-content/uploads/2019/01/repo_options.png)


*Any questions or problems?*

----

So far what we have is pretty basic, but we can quickly start editing. Let's click on the little pencil icon to edit the README file. This will take us to a text editor where we can edit the file. Let's add some text to the file. For example, let's add the following text:

```
# Introduction to Digital Humanities

This is my repository for IS 578: Introduction to Digital Humanities.
```

Now let's scroll down to the bottom of the page and click on the `Commit changes` button. This will save our changes to the repository. You'll notice that we have to add a commit message. This is a message that describes the changes we made to the repository. For example, we could write `Added text to README file`.

But what exactly did we just do? We just made our first commit and worked with git, so time for the next lesson!



[^1]: For more about this acquistion see Warren, Tom. “Microsoft Confirms It Will Acquire GitHub for $7.5 Billion.” *The Verge*, June 4, 2018. [https://www.theverge.com/2018/6/4/17422788/microsoft-github-acquisition-official-deal](https://www.theverge.com/2018/6/4/17422788/microsoft-github-acquisition-official-deal).
[^2]: Dohmke, Thomas. “100 Million Developers and Counting.” The GitHub Blog (blog), January 25, 2023. [https://github.blog/2023-01-25-100-million-developers-and-counting/](https://github.blog/2023-01-25-100-million-developers-and-counting/).
[^3]: David., “Seeds Or Code?,” accessed April 5, 2023, [https://blog.dshr.org/2019/11/seeds-or-code.html](https://blog.dshr.org/2019/11/seeds-or-code.html).
[^4]: For more information on this topic, you can read ["The Schism at the Heart of the Open-Source Movement"](https://www.theatlantic.com/technology/archive/2020/01/ice-contract-github-sparks-developer-protests/604339/) and [Dear GitHub](https://github.com/drop-ice/dear-github-2.0/blob/master/README.md).


We just created our first repository and updated our file. But how exactly did we do that and what were we even doing exactly? This is where git comes in!

## What is Git? 

Git is a third-generation version control system designed to keep track of changes in your projects. Created in 2005 by Linus Torvalds, the creator of the Linux kernel, Git is a decentralized version control system that requires changes to be saved (committed) before they can be combined (merged) with the main project. What that means in lay terms is that Git is the software that allows you to track changes in your project and collaborate with others. You are already familiar with this concept if you've ever used Google Docs or Microsoft Word's "Track Changes" feature, but in those you get the version history automatically. With git, we have to tell it what to track and when to track it.

A very important thing to understand is that while git and GitHub sound the same, they are two separate technologies. Git is a version control system, while GitHub is a platform for hosting git repositories. We'll be using both in this course, but it's important to realize they are not identical.

<div class="notice--info">KEY POINT: GitHub is a <em>remote</em> platform for hosting materials, git is a version control system that can work both on GitHub and <em>locally</em> on your computer.</div>

### A Brief History of Version Control (Optional read)

Before Git, there were several generations of version control systems that evolved to meet the changing demands of software development. The first generation, represented by tools like Source Code Control System (SCCS) developed in 1972 by Marc Rochkind at Bell Labs, was centralized and relied on simple single-file locking-based concurrency. The Revision Control System (RCS), developed a decade later in 1982, followed the same lines but became widely popular due to its open-source nature.

The second generation included the Concurrent Versions System (CVS), which allowed for more networked, collaborative work by introducing a merging-based approach instead of a file-locking approach. However, CVS had limitations that were addressed by its successor, Subversion, released in 2000, which allowed for more robust fileset operations with atomic commits.

Git represents the third generation of version control, combining lessons from these previous systems with new features suited for modern, large-scale software development.

### Why is Git Useful in Humanities?

Although Git and version control systems are predominantly used in software development, they offer several advantages for scholars in the digital humanities. Similar to how you might handle versions of a paper, essay, or data set, Git allows you to:

- Keep track of changes in plain text files 
- Collaborate in real-time with other researchers
- Easily revert to earlier versions
- Create different branches to explore new ideas without disturbing the main project


## Working with Git and GitHub

In this course, we will be using GitHub extensively, which requires some understanding of git and version control. However, you are not required to install git or use it in your terminal (though both things may prove easier down the road). Instead, we will be using GitHub's web interface to work with git.

### Installing Git (Optional step)

If you decide to install Git on your local computer, I highly recommend following these instructions [here](https://github.com/git-guides/install-git) and also reaching out to the instructor if you have issues. For Windows users, you will also need to install Git for Windows, which includes Git Bash. Step-by-step instructions can be also found [here](https://github.com/DHRI-Curriculum/install/blob/master/sections/git.md#windows).

### Editing Files in GitHub

So far, we have already tried to edit a file in GitHub. This is a great way to make quick changes to a file, but it's limiting to working with one file at a time. For more complex projects, we will need to use either the command line with git or GitHub in the broswer.

Let's try adding using the GitHub interface in the browser and making more changes to our README.md file.

### GitHub Dev

GitHub Dev is a new feature that allows you to edit files in the browser and commit them to your repository. To access it, all you have to do is change `github.com` in your URL to `github.dev`. 

So for us, we would change `https://github.com/[USER NAME]/is578-introduction-dh` to `https://github.dev/[USER NAME]/is578-introduction-dh`.

![github dev](https://user-images.githubusercontent.com/856858/130119109-4769f2d7-9027-4bc4-a38c-10f297499e8f.gif)

You can also just hit the `.` key on your keyboard when you're in a repository to open GitHub Dev.

Now you should see a new interface that looks like this:

![github dev]({{site.baseurl}}/assets/images/github_dev.png)


This interface let's us interact with our repository and files in a program called Visual Studio Code (VS Code). VS Code is a text editor that is very popular with programmers and digital humanists. It is also owned by Microsoft, which gives you a taste of how much they are centralizing the (DH) tools ecosystem.

Now we can update our README.md file with some new text. Let's add a new section called "In Class Lab Activity" and add some text to it.

![github edit]({{site.baseurl}}/assets/images/dev_edit.png)

You'll notice after you click on the file and update it, that there's a small blue circle with a number in it. This is the number of changes you've made to the file. If you click on it, you'll see a new Side Panel with the name `SOURCE CONTROL`. This interface is where we need to save our changes.

![github commit]({{site.baseurl}}/assets/images/dev_commit.png)

First, we need to once again write a message for our `commit` in the white box that says `Message` (if you don't you'll see an angry red message). Once we have done that we can press the big blue button that says `Commit & Push`.

Initially it will seem like nothing happened, but if we navigate back to our `github.com` version of our repository, you'll see that the updated changes are live. 

### Git Branching and Merging

So far we have been working with git, but not really talking about it. Every time we `commit` a change that is git.

But what is a commit exactly?

A commit is a snapshot of your project at a particular point in time. It's like a save point in a video game. You can go back to it at any time and see what your project looked like at that point in time.

But what if you want to try something new? You don't want to mess up your project, but you want to try something new. This is where `branching` comes in.

A branch is a copy of your project that you can make changes to without affecting the main project. You can create as many branches as you want and then merge them back into the main project when you're ready.

![git branch](https://www.nobledesktop.com/image/gitresources/git-branches-merge.png)

While we won't use much branching in this course, it's important to know it exists. For example, in our repository we have been *committing* to the `main` branch. But we could create new branches if we wanted to try something new.

#### Git Commands and AI Tools

While we will use git more extensively towards the end of the semester, I want to flag that so far we haven't really explained how to use git beyond pressing buttons on GitHub. This is only scratching the surface, but can also be overwhelming when starting off.

Eventually diagrams like the one below will make sense:

![git diagram](https://www.edureka.co/blog/wp-content/uploads/2016/11/Git-Architechture-Git-Tutorial-Edureka-2.png)

But for now, I would suggest that if you have any errors when using GitHub and git that you both reach out to the instructor, explore the resources below, and also try to using your preferred AI tool for fixing errors. The results may not be perfect, but this type of technical syntax is difficult to learn so it's important both to practice and utilize the resources available to you.

## In Class Lab Activity

### Updating Repositories

So far, we have only updated our README.md file, but we can also add other files in our repository. Let's try adding our command line maze to our repository.

*Any suggestions or questions for how we could do this?*


## Assignment

- [ ] Find one DH tool using whatever digital workflow you prefer. This tool may be one that you've used before, read about, or just found through searching. 
- [ ] Once you’ve located your tool, try to find it in the Index of DH conferences interface [https://dh-abstracts.library.virginia.edu/](https://dh-abstracts.library.virginia.edu/) and "download" at least one of the abstracts (how you do this will depend on your workflow and preference). If you cannot find your tool, then either try to find an alternative tool OR find an example of its usage in a DH project.
- [ ] Create a new file in your GitHub repository using the `github.dev` interface and the new file button. Save this file as `DH-Tool.md` (remember the `.md` to indicate the file type) and add the following information:
  - [ ] Name of the tool
  - [ ] Link to the tool
  - [ ] Link to the abstract or DH project
  - [ ] A short description of why you consider this to be a “DH tool” and whether you have previous experience using it.
- [ ] Commit and save the file to your repository. Then, finally, share a link to your file in our GitHub discussion forum for the assignment [here](https://github.com/ZoeLeBlanc/is578-intro-dh/discussions/2#discussion-5604130). 


## Additional Resources

- [Shane Lin's *Git for Humanists*](https://shane-et-al.github.io/git_slab/), a great introduction to Git for humanists
- Melanie Walsh's Introduction to Git and Github in *Introduction to Cultural Analytics* [https://melaniewalsh.github.io/Intro-Cultural-Analytics/04-Data-Collection/04-Git-GitHub.html](https://melaniewalsh.github.io/Intro-Cultural-Analytics/04-Data-Collection/04-Git-GitHub.html)
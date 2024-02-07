---
title: "Web Scraping & Complex Python"
permalink: /materials/creating-curating-humanities-data/03-web-scraping
excerpt: "An introduction to web scraping with Python."
toc: true
---

Now that we have refreshed our knowledge of Python and learned how to create virtual environments, it's time to start getting more advanced in how we use Python to get data. In this lesson, we'll learn how to use Python to scrape the web and get data from web pages. 

## Complex Python

### Classes

So far we've learned how to store data in different data types (integers, strings, floats, etc...) and structures (lists and dictionaries). We've also learned how to use for loops to manipulate our data, conditionals to change the data flow, and functions to encapsulate our code and make it reusable and generalizable.

Now that we've started to learn the range of Python syntax, we can start putting it all together. One of the main ways we can do that is with `Classes`.

Let's take a look at code from the Advance Python Part 1.

```python
def make_tool_dict(tool_name, value_2015):
    return {
        "name":tool_name,
        "2015":value_2015 ,
    }

dh_tools= {
    "tool": make_tool_dict("Python",9),
    "creator": "Guido van Rossum"
}
```

This code snippet contains a **function** called make_tool_dict that returns a **dictionary** with the name and value from 2015 for a DH tool. We call this function inside of the dh_tools **variable**. 

If we added a print statement in our script, this would be the output in the terminal:

```python
{
    'tool': 
        {
            'name': 'Python', 
            '2015': 9
        }, 
    'creator': 'Guido van Rossum'
}
```

Right now this code works well if we just have our existing spreadsheet about these tools, but what if we wanted to build upon this initial research to add more fields and information about the tools, and also maybe even reuse this code in multiple scripts? Then we might want to consider rewriting the code into a **class**.

While dictionaries are great for describing complex data within a single object, a class is really useful to encapsulate both data and functions in a single cohesive unit.

A class is a particular type of **object**. We can create ("instantiate") an object of a class and store it as a variable. A variable therefore contains (technically, contains a reference to) an *instance* of a class.

Sounds complex but let's break it down...

We've already used a lot of built-in classes. Strings, lists, dictionaries are all classes. We can have Python tell us what kind of class it is using the built-in function `type()`.

```sh
>>> a = [1,2,3]
>>> type(a)
<class 'list'>
>>> b = "123"
>>> type(b)
<class 'str'>
```

Python classes are great for storing complex data structures, but they can also be simple.

Here's how you define a simple class that does nothing.

```python
# Define a class
class Blank:
    pass  # Pass means "Move along, please. Nothing to see here."

# Create an instance of the class and invoke it
Blank()
```

To first define a class, we need to use the keyword `class` followed by the name of the class (which can be anything!) and then a semi colon. All the logic of the class is indented (just like with functions, loops, and conditionals) and then we call the class similar to a function, using its name and parentheses to pass arguments to the class.

In this case, since the class has no actual logic in it, just the keyword `pass`, nothing actually happens. For any class, when you invoke it, it executes the `__init__` method, which is another built in method from Python (this one is called a **constructor** method). Thus, since our example above didn't define any logic for the built-in `__init__` method, nothing happened.

## Simple Class

Let's define a class that actually does something when it's initialized.

```python
class DHTool:
    def __init__(self, name):
        self.tool_name = name

a_tool = DHTool("Python")
a_tool.tool_name
```

So similar to our initial `make_dh_tool` function, we are creating a way to store data about DH tools. However, in this example we've created a class that has an initial method (which is really just a function!) that takes the argument we pass and assigns it to something called `self`.

Self references the class **instance** that is created when you call a class, which is why `self` is the first argument to ***any*** function defined in a class. You can read more about [class scope here](https://docs.python.org/3/tutorial/classes.html#python-scopes-and-namespaces).

Let's try making a more complex version of our DH tool class.

```python
class DHTool:
    """Contains methods for maintaining data related to a dh tool

    Methods:
    --------
    add_authors
    add_year_popularity
    calculate_total_popularity
    """
    def __init__(self, name):
        self.tool_name = name
        self.authors = list()
        self.year_values = dict()
        self.total_value = 0


    def add_authors(self, authors):
        """Adds a list of authors of the DH Tool

        Method argument:
        -----------------
        authors(list) -- A list of people who built the dh tool
        """
        if isinstance(authors, list) is False:
            authors = [authors]

        self.authors.extend(authors)


    def add_year_popularity(self, year, value):
        """Adds the popularity value for each year of the DH tool

        Method argument:
        -----------------
        year(integer or string) -- A year 
        value(integer) - Popularity value
        """

        self.year_values[str(year)] = value


    def calculate_total_popularity(self):
        """Calculate the total popularity for a tool
        """

        self.total_popularity = sum(self.year_values.values())
        print(self.total_popularity)


a_tool = DHTool("Python")
a_tool.add_authors("Guido van Rossum")
a_tool.add_year_popularity(2015, 9)
a_tool.calculate_total_popularity()
print(a_tool.total_popularity)

print(a_tool.add_year_popularity.__doc__) # To view the docstring for the method
```

So what's going in this code block?

First we're taking our `DHTool` class and expanding it so that it can contain more information about each tool. We still only initially create the class with one argument - the tool's name. But we've also added additional attributes to the `__init__` function. First, we have `authors`, which holds a list; then year_values, which is a dictionary holding years as keys for the tool's popularity value, and finally total_value, which is an integer that we store the total popularity of the tool.

Do you notice that the syntax here looks like a dictionary? That's because we can use a similar pattern to dictionaries for creating our attributes.

To make it even more clear this is what the `__init__` method would look like as a function that return a dictionary:

```python

def make_dh_tool(name):
    dh_tool = dict() #Could also write {}
    dh_tool.tool_name = name
    dh_tool.authors = alist()
    dh_tool.year_values = dict()
    dh_tool.total_value = 0
```

While this function is somewhat similar to our `DHTool` class, we've also added a number of functions, which we call **methods** to the class.

The first method `add_authors` takes two arguments, `self` and `authors`. Just like in the `__init__` method, `self` represents the class instance and authors is a list of authors. In the `__init__` method, we define the authors attribute on `self` as an empty list. Then in our `add_authors` method we extend this initial empty list, adding the new authors to the list.

What would happen if we decided to add an additional author of Python from the [list of core contributors](https://devguide.python.org/developers/)?

```python
a_tool.add_authors("Joannah Nanjekye")
print(a_tool.authors)
```

We can check by printing out the authors attribute, and we'll see that the list now contains both Guido and Joannah.

Our `DHTool` class also has methods for add popularity values for each year, and also for calculating the total popularity for the tool.

What if we wanted to add a method for printing out an entire tool's information? We could try looping through the class object and print out each attribute. Or we could use the built-in `__dict__` functionality that prints out the values for a class.

```python
def get_tool_info(self):
    print(a_tool.__dict__)

```

### Quick Assignment

1. Try adding the `get_tool_info` to our `DHTool` class and then call it in your script.
2. Try adding a second tool with all the relevant information, and then calculate it's total popularity and print out it's full information.

#### Additional Reading

1. [An Introduction to Python Classes and Inheritance](http://www.jesshamrick.com/2011/05/18/an-introduction-to-classes-and-inheritance-in-python/)
2. [Here is a very helpful video series on class inheritance](https://www.youtube.com/playlist?list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc)
3. [Python Documentation on Classes](https://docs.python.org/3/tutorial/classes.html)


#### Commenting and Documentation

##### Inline Commenting

Comments are especially useful--necessary!--for collaboration. Python is open source and its community of millions of coders often share in its permissive approach to intellectual property. Python as a whole is a giant collaborative project of which you are now members.

When you write particularly complicated logic or whenever you write new classes or functions (more on this later!), you should write a comment to explain yourself.

```python
edited_definition_of_dh = definition_of_dh.replace('tools', 'people') 
print(edited_definition_of_dh)
```

##### Documentation

Python, as with virtually all other languages and complex codes, contains extensive documentation that covers all aspects of its use. This documentation is [easily accessible via the Internet](assets/MissionImpossible.m4v?raw=true).

[Python 3 Documentation](https://docs.python.org/3/)

Let's take a look at the specific documentation for strings:

[Python 3 Docs: Built-in Types: Strings](https://docs.python.org/3/library/stdtypes.html#string-methods)

Learning to read documentation is a critical skill for succeeding as a programmer. Happily, most of you, as graduate students, should already be literate.


### Libraries


#### Imports

#### File Input and Output

##### Reading Files

##### Writing Files



## Classes


## Python Libraries

So you're probably wondering when to use classes? Mostly we won't be delving into code complicated enough to require to write your own classes, but you will be using lots of code that is based on this pattern. That's because the class is the primary way that Python organizes its standard library and the wider ecosystem of external libraries.

Let's dig into the Python documentation to understand more! [Here's the Python Standard Library](https://docs.python.org/3/library/). We've already been using this documentation, but let's scroll down to the [Pathlib module](https://docs.python.org/3/library/pathlib.html).

First take a look at the [source code!](https://github.com/python/cpython/blob/3.8/Lib/pathlib.py) Notice how it's organized, and try and find the documentation for the `class Path` (*hint* use control F)

Let's take a look at the methods in the `class Path` [https://docs.python.org/3/library/pathlib.html#methods](https://docs.python.org/3/library/pathlib.html#methods). How would we would print out the current working directory using pathlib? 

Let's try importing in `Pathlib` into our script.

## Imports are Important

We can easily bring classes into other code using the `import` keyword, which does some magic to allow us to use classes defined in other files. This is how we can use parts of the Python Standard Library that aren't directly built into the base language. It's also how we use modules written by other programmers from the larger Python community. 

We can also use `import` to import our own classes. It gets complicated if we have to specify the path, so for now it's easier to open the Python interpreter inside the same directory to import.

## File Input and Output

To use pathlib, we needed to import the `pathlib` module. Pathlib is useful not just for printing out working directories, it can also let us load in files. 

Up to know you've had to hand enter data but in Python you can use various libraries to manipulate and read in data.

Let's try it out with Pathlib by passing in our DH tools csv path to the `Path` class.

Because of how my site is organized the file path for `tools_dh_proceedings.csv` is in my assets and then files folder. You'll need to change the path to your version so that your computer knows what exact file you mean.

```python
from pathlib import Path

file = Path('../assets/files/tools_dh_proceedings.csv')
print(file, type(file))
```

If you run this code you should see the exact file path of your spreadsheet and then the type of the object, either `<class 'pathlib.PosixPath'>` or `<class 'pathlib.WindowsPath'>`. Not to get too complicated but this is because the `Path` class is a subclass of the `PosixPath` class (not really going to get into subclassing but think of it as building classes on top of one another - like lego or jenga). 

We can also look at the methods built-in to the `Path` class. One in particular is useful for us `read_text` which reads in the contents of a file and returns it as a string. Read more about it here [https://docs.python.org/3/library/pathlib.html#pathlib.Path.read_text](https://docs.python.org/3/library/pathlib.html#pathlib.Path.read_text) and test it out in your script.

```python
from pathlib import Path

file = Path('../assets/files/tools_dh_proceedings.csv')
print(file, type(file))

print(file.read_text())
```

You should now see the entirety of our csv file in your terminal. If you try saving that to a variable and checking the type you should see that it's a string.

So now we can simply manipulate that string so that we don't have to hand enter the data.

### Quick Assignment

Try seeing if you can use the `read_text` method to read in the contents of the csv file and store it in a variable. And then use that data in your existing DH tools code.

----

So far we've been using Pathlib to work with files, but there are number of libraries and even some methods built into Python for reading in and writing files.

For example we could use the [`open` built-in function in Python](https://docs.python.org/3/library/functions.html#open).

To open a file for reading (input), we just do:

```python
input_file = open("tools_dh_proceedings.csv","r")
text = input_file.read()
print(text)
input_file.close()
```

Here, we use the `open` function to open a file in mode "r" (read). `open` returns a [File Object](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files) that provides methods for reading and writing. In this case, the `read` method reads in data from the `input_file` file object and stores it as a string in `text`.

At the end, we can close the file to save some memory, but even if we don't do it explicitly, Python will eventually catch on to the fact that it isn't being used anymore and do it for us. This isn't a huge concern unless you're opening thousands of files or the files you're opening are very, very large.

Often, you'll see file handling used with the `with` keyword:

```python
with open("tools_dh_proceedings.csv","r") as input_file:
    print(input_file.read())
```

This is functionally the same as our last example. The only difference is that the file is automatically closed at the end of the block. You can use whichever convention you like, but keep both in mind because they're both pretty common in the wild.

### File Output

File output is very similar. We just use mode `w`, which overwrites the file specified. We can also use `x` (which only works for new files) or `a` (which appends data at the end of the file). Read the [`open` docs](https://docs.python.org/3/library/functions.html#open) for all the details and also take a look at this table.

|Character| Mode |Description|
|-|-|-|
|`r`|Read (default)| Open a file for read only|
|`w` |Write |Open a file for write only (overwrite) and will also create a new file if it doesn't exist|
|`a` |Append |Open a file for write only (append)|
|`r+` |Read+ |Write open a file for both reading and writing|
|`x` |Create |Create a new file|


To understand file output, let's try working with a file that doesn't exist. Try pasting this code in your script.

```python
f = open("new_text.txt","w")
for i in range(0,100):
    f.write(str(i**2)+"\n")
```

Once you run it, you should see a new file in your directory called `new_text.txt`, which should be a text file, containing a list of numbers. We created those numbers using the built-in `range` function and the `write` method.

Here, there's something just a little tricky. `i` and `i**2` are  integers, but the file object in this case expects a string. If we try to use `f.write(i**2)` instead, we'll get an error: `TypeError: write() argument must be str, not int`.

To get around this, we can convert from int to string using the built-in `str` class constructor `str()` to create a new string that's the *string representation* of the integer we pass in. So even though the integer 4 and the string "4" look the same, they're different objects and different ways to represent data.

For the same reason that we can't do `f.write(4)`, we also can't do `"4"+4` (or, for that matter, `4+"4"`). We have to explicitly tell python whether we want it to treat each value as an integer or a string. `"4"+str(4)` produces "44" while `int("4")+4` returns 8.

The second new thing here is the newline character "\n", which is technically called a LF or Line Feed. This inserts a line break between characters in a string.

### Reading CSVs

While we can use the `open` method or Pathlib for working with text files, but usually for CSVs (aka spreadsheets), we need a Python library with a little more functionality. One of the most common ones is the [`csv` module](https://docs.python.org/3/library/csv.html). Just like with Pathlib, we first to import `csv` and then we can still use `open` to open our spreadsheet.

But now we use the built-in methods of `csv` library to manipulate our file.

```python
import csv

with open("tools_dh_proceedings.csv","r") as input_file:
    csv_reader = csv.reader(input_file)
    for row in csv_reader:
        print(row)
```

Try out this code and see what the difference is between the `csv.reader` and `read_text` methods we've tried out.


## Quick Assignment: Putting it Together

Here's part of what you did in the command line assignment earlier, but now in Python.

```python
jane = 'The Project Gutenberg EBook of Pride and Prejudice, by Jane Austen This eBook is for the use of anyone anywhere at no cost and with almost no restrictions whatsoever. You may copy it, give it away or re-use it under the terms of the Project Gutenberg License included with this eBook or online at www.gutenberg.org Title: Pride and Prejudice Author: Jane Austen Posting Date: August 26, 2008 Release Date: June, 1998 Last Updated: March 10, 2018 Language: English Character set encoding: UTF-8 *** START OF THIS PROJECT GUTENBERG EBOOK PRIDE AND PREJUDICE *** Produced by Anonymous Volunteers PRIDE AND PREJUDICE By Jane Austen Chapter 1 It is a truth universally acknowledged, that a single man in possession of a good fortune, must be in want of a wife.'
jane = jane.replace("man","person").replace("wife","partner")
print(jane)
```

Let's say that we want to "modernize" every classic book on Project Gutenberg. The first step is to write a program to read a single book in, replace the words, and then write it back out to a file.

I've pushed the Gutenberg version of Pride and Prejudice to this directory [here]({{site.baseurl}}/assets/files/PrideandPrejudice.txt) and the skeleton of the code needed to convert the text:

```python
filename = "PrideandPrejudice.txt"

### input code to read file goes here

jane = jane.replace("man","person").replace("wife","partner")

### output code to print file changes goes here
```


## Web Scraping

### What is Web Scraping?

#### Why Web Scraping?

#### Is Web Scraping Legal?

### Web Scraping with Python

#### Requests

#### Beautiful Soup

Let's install our required packages. If you haven't already, check out the instructions for installing a [virtual environment]({{site.baseurl}}/materials/advance-python/05-virtual-environment).

We previously discussed Python libraries when we talked about classes and file input and outputs, but let's dig in a bit deeper. 

- Library: There's a lot of different definitions for this term, but most generally you can think of this as a collection of software that's directly used by other software. Most often, this will be a generalizable piece of logic that is useful to bundle separately so that other, unrelated pieces of software can use it. Because it's an informal term in Python and not a specific, technical one, it's more useful to think about libraries in terms of how code is organized. Used in this way, the concept of "software libraries" spans many different programing languages and development contexts: we have Python libraries, C++ libraries, Javascript libraries, operating system libraries, etc.
- Let's consider libraries that we've used. The [Python Standard Library](https://docs.python.org/3/library/) is the most obvious example which encompasses many different purposes and packages (more on that later), but is unified in that it is included in all Python installations so that Python code that's written using the Standard Library will run on any compatible Python environment of the expected version. Parts of the Standard Library that we've used before include packages like [pathlib](https://docs.python.org/3/library/pathlib.html).
- There are also third-party libraries that people build in Python, which can be found on The Python Package Index (PyPI) <https://pypi.org/>. These are usually less expansive than the Standard Library, but can be useful because they are written for specialized tasks. This week, we'll take a look at [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/), which is analogous in scope to packages like pathlib. In fact, third party libraries are often organized into a single package. A library like Beautiful Soup can best be thought of in terms of purpose: you want to accomplish the a particular, common task like scraping a website and Beautiful Soup helps accomplish it.
- Package: A package is a formal term in the Python context. It's a specific organization of code which all lives in a single directory. Libraries sometimes (often) consist of a single package (e.g. PathLib or BS4), so the term is sometimes (often) used interchangeably. Packages are the basic unit by which we install and use libraries. So when we type `pip3 install beautifulsoup4` into the terminal, we're installing the beautifulsoup4 package.

Here, confusingly, the name of the package on PyPI (beautifulsoup4) doesn't match the actual Python code package (bs4). Always [read the docs](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)!

We use Beautiful Soup in our Python code with code that looks like this:

```python
import bs4
soup = bs4.BeautifulSoup(html_doc, 'html.parser')
# 'bs4' is the package, 'BeautifulSoup' is a class defined inside the package definition
```

or

```python
from bs4 import BeautifulSoup
soup = BeautifulSoup(html_doc, 'html.parser')
# this code is equivalent
```

We can also use the star symbol, which often means "all" or "any", to import all the modules in the package:

```python
from bs4 import *
soup = BeautifulSoup(html_doc, 'html.parser')
# imports * imports all modules in a package
```

In these examples, we can either the `bs4` *package* directly or, using the `from` keyword, import *modules* from with that package.

Incidentally, it's almost always considered poor practice to use the `from x import *` form. We see in the example immediately above that, for people just reading through our code, there's no obvious connection between the bs4 package and the BeautifulSoup class. It would take some deeper understanding of BeautifulSoup or at least chasing down some its documentation

### What is Web Scraping?

Web scraping is extracting data from web pages, using the syntax of a web page. It's great for compiling datasets when you don't already have them in a database somewhere. A good supplemental resource for web scraping is [Intro to Beautiful Soup by Jeri Wieringa](https://programminghistorian.org/en/lessons/intro-to-beautiful-soup) at The Programming Historian or Melanie Walsh's [Chapter on Web Scraping](https://melaniewalsh.github.io/Intro-Cultural-Analytics/04-Data-Collection/02-Web-Scraping-Part1.html#)

### So how do we scrape the web?

In Python, there's more than a few different libraries we could use, but let's continue to focus on Beautiful Soup. We've already installed our required packages, so let's check that we did it correctly.

```python
import bs4
print(bs4.__version__)
```

Looks good so now let's take a look at the page we'll be scraping, <https://humanist.kdl.kcl.ac.uk/>. This is a web archive of a Digital Humanities Listserv that was started in the 1980s and continues to today. Save that page to a file called `humanist_homepage.html` in the same directory as this notebook.

Now we can try scraping that page!

```python
from bs4 import BeautifulSoup
soup = BeautifulSoup(open("humanist_homepage.html"), features="html.parser")

print(soup.prettify())
```

You can see we now have the full html page in all it's weirdly organized HTML glory.

Now let's figure out how to use BeautifulSoup by going to the [documentation for the library](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

We can see here that `soup` is an instance of a [bs4.BeautifulSoup class](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#beautifulsoup). This is an object that represents the whole of the document. The other important class we will use is the [Tag class](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#tag), which represents an html tag. These two classes actually share many of the same methods: we can use `get_text()` on either a BeautifulSoup or a Tag to extract just the text that they contain.

We can also use the `find_all()` method that they share to search with either the whole document or within the tag. Remember that tags can be nested within each other.

Let's try and get all the links on our webpage.

```python
links = soup.find_all('a')

for link in links:
    print(link)
```

We can see that we are getting lots of different links here. Everything from the Home link (which is usually just a `/` on most websites) to links to all the volumes.

So now we need to decide what we want to keep and what we don't 🤔. Let's take a look at the basic structure of the html file. We can do this easily using the development console built into most popular browsers. In Chrome or Firefox, right clicking (or control-clicking) and choosing "Inspect" or "Inspect Element". We can see that the html is pretty basic, but it does seem like there's some patterns for the links.

### Quick Assignment

How could we get just the Volume links? We can use the `find_all()` method to get all the links in the document and then use `get_text()` to get the text of each link.

```python
links = soup.find_all('a')

for link in links:
    print(link)
    ## Code goes here
```

## Requests and the Web

We are now scraping a web page 🥳!! But what if we wanted to scrape more than one? Saving each manually would get tiring really quickly!

Instead we can use another Python library called `requests` to programmatically get each web page. Try installing and then importing requests.

```python
import requests
response = requests.get("https://humanist.kdl.kcl.ac.uk/")

print(response.status_code)
print(response.headers)
```
So what is this information exactly?

Well the first line is the status code of our request and the second line is the headers that are returned with the request. This information is important because this is how we might know if we get an error when we try to request a web page. However, to understand what this means we need a quick introduction into how the web and HTTP works.

If you already know how the Web works then feel free to skip this next section. Otherwise read on!

### What is the Web?

[**From Wikipedia:**](https://en.wikipedia.org/wiki/World_Wide_Web)
"The World Wide Web (WWW), commonly known as the Web, is an information system where documents and other web resources are identified by Uniform Resource Locators (URLs, such as <https://www.example.com/>), which may be interlinked by hypertext, and are accessible over the Internet.[1][2] The resources of the WWW are transferred via the Hypertext Transfer Protocol (HTTP) and may be accessed by users by a software application called a web browser and are published by a software application called a web server."

![http](https://2.bp.blogspot.com/_4l9wMe5bbSk/TMpvwVcMT3I/AAAAAAAAAK4/sCEjRQCkF1o/s1600/Client+Server+communication.GIF)

*What does this mean exactly?*

When we type a url for a webpage (say google.com), we're actually sending an **HTTP request** to a **server** that hosts the actual HTML files and data. If the server decides that our request is ok (200), then it will give us access to the webpage.

![404 page](https://user-images.githubusercontent.com/2938045/56276896-af93b580-6103-11e9-9885-74981a49a5ae.png)

If you've ever seen an error message when you go to a webpage saying the page doesn't exist, that means that you received a 404 error, which is a type of status code you get back from an HTTP request.

## What is HTTP?

**Courtesy of [Julia Evans' Zine](https://jvns.ca/blog/2019/09/12/new-zine-on-http/)**

![What is HTTP?](https://pbs.twimg.com/media/EAiEGSgXsAELERE?format=jpg&name=large)

This comic explains a bit more in depth what is comprised of an HTTP request. We also want to have a sense of what types of status codes we can get back from a request.

![HTTP Status Codes](https://pbs.twimg.com/media/D-bI-xyWkAAY0Qb?format=jpg&name=large)

Finally, in our example we used the `GET` method when calling a webpage (using `request.get()`), but there's multiple methods that we can use to send data across the web.

![HTTP Request Methods](https://pbs.twimg.com/media/EB8dt0CWsAAET4b?format=jpg&name=large)

![How to learn more](https://pbs.twimg.com/media/ECvlQX1W4AE9EgP?format=jpg&name=large)

[More information about HTTP from Mozilla Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)

If you're interested in the longer history of the internet checkout this timeline from the Computer History Museum, covering the history from the 1960s to the 1990s [https://www.computerhistory.org/internethistory/](https://www.computerhistory.org/internethistory/).

### Requesting and Souping Humanist

Alright so now we know how the web works in a broad sense, but let's jump back into our example and into [this section of the Cultural Analytics textbook](https://melaniewalsh.github.io/Intro-Cultural-Analytics/04-Data-Collection/02-Web-Scraping-Part1.html#beautifulsoup).

Prior to this section, Melanie has this code block that fetches the text of a webpage:

```python
def scrape_screenplay(url):
    response = requests.get(url)
    html_string = response.text
    return html_string
```

Let's try out `response.text` with our code block.

```python
print(response.text)
```
Notice that this looks familiar 🤔! It's our HTML from the webpage that we had previously downloaded and we can double check by passing it into BeautifulSoup.

```python
soup = BeautifulSoup(response.text, "html.parser")
print(soup.prettify())
```

Wonderful! Now we could for example loop through and scrape the text of each of the Volumes on the Humanist Listserv site.

*Have any questions or issues? Either post it to Discord or message the instructor.*

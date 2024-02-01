---
title: "Python Refresher"
permalink: /materials/creating-curating-humanities-data/01-python-refresher
excerpt: "A refresher and overview of how to code with Python."
toc: true
---

So far in this course, we have either been using the command line or markup languages, but now it's time to get back into some programming. As a reminder, this course assumes you have either taken a programming course or have some experience with programming. If you don't have any experience with programming, you should contact the instructor immediately.

## Python Basics

The easiest way to work with Python is through the command line. You can open the command line and type `python` to start the Python interpreter. You can also use a text editor to write Python code and then run the code in the command line.

Let's start by first checking our Python version. Open the command line and type `python --version` or `python3 --version`. You should see something like the following:

<figure>
    <a href="{{site.baseurl}}/assets/images/python_version.png">
    <img src="{{site.baseurl}}/assets/images/python_version.png" alt="Python Version" class="image-popup">
    </a>
</figure>

If you don't see these messages, then you might not have Python installed, so return to our [setup instructions]({{site.baseurl}}/materials/introducing-humanities-computing/01-course-tools/#python) and reach out to the instructors for assistance.

Once you have Python working, you can type `python` and this will open the interactive Python interpreter where you can write your python code and have the computer execute it. The python interpreter is an excellent way to sandbox your ideas or check your syntax. You can exit using `exit()`.

Type `'Hello world'` in the interpreter and press enter.

<figure>
    <a href="{{site.baseurl}}/assets/images/python_hw.png">
    <img src="{{site.baseurl}}/assets/images/python_hw.png" alt="Hello World" class="image-popup">
    </a>
</figure>

Congrats you've just typed your first bit of Python and had the computer execute it 🎉!

Let's breakdown what just happened.

1. You entered data into the interpreter.
2. That data had a certain format, in this case a variable, and the interpreter automatically showed that data again.

We can also use the interpreter as a calculator. Try out these examples.

```python
1+1
2**3
```

You'll notice that though the interpreter *prints* out when you press enter, the results of our calculations aren't saved any where. What if we wanted to save our data?

### Variables

We can save our hello world data into a *variable* and keep using it again and again.

```python
var = 'Hello world'
```

Now try typing `var` again. What happens?

The `var` variable now has 'Hello world' stored inside. Python understands that our variable contains a *string*. You can type any string and store it into a variable.

```python
one = 'one'
two = 'two'
three = 'three'
```

Python knows that these variables contain strings because of the use of either single('') or double quotes("").

### Data Types

Strings are just one of many data types accepted in Python.

There's also numbers, called *integers*. We can take our variables that we assigned before and assign them their actual numbers.

```python
one = 1
two = 2
```

Once we do this though, our strings that were stored in these variables will be **erased!**

What happens if you try and use a number for your variable?

```python
1 = 1
```

You'll get a syntax error! That's because Python has rules for how to name variables.

- A variable can have a short name (like `x` and `y`) or a more descriptive name (`age`, `carname`, `total_volume`)
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)

*So what makes a good variable name?*

As a general rule of thumb, I would recommend choosing names that are short and descriptive. In Python, we also tend to use underscores for naming (versus Javascript where you use camelCase). For some more examples, see Melanie Walsh's note on ["Striving for Good Variable Names"](https://melaniewalsh.github.io/Intro-Cultural-Analytics/02-Python/04-Variables.html#striving-for-good-variable-names).

So our previous example could work if we changed the variable name to:

```python
one_1 = 1
```

Python also has a special name for floating point numbers, called *floats*.

```python
one = 1.0
```

Integers are simple and easy to use. Floats are mostly easy, but sometimes really weird!

*Weird Numbers*

What does this return?

```python
0.1+0.2
```

Huh, weird.

All data in a computer is represented as binary (base 2) numbers, comprising only 1s and 0s. The text you're reading now is represented by individual characters that, under the hood, are stored as binary numbers. The method of translating these information between different forms and contexts (such as between binary numbers and text or numbers) is called **encoding**.

Integers are easy enough to represent in binary: 0 is 0, 1 is 1, 2 is 10, 3 is 11, 4 is 100, and so on.

But floats are trickier and require a special system to represent. Don't worry about it for now, but consider for a moment that it's impossible to represent exactly 1/3 in finite decimal notation (0.3333...). It's similarly impossible to represent some simple decimal numbers in a binary notation. Which is why you get the weird results above.

For more information check out [Float to Binary Converter](https://www.h-schmidt.net/FloatConverter/IEEE754.html) and [IEEE 754 Standard](https://en.wikipedia.org/wiki/IEEE_754-1985).

### Built-In Methods

What if we decided that we wanted to combine variable `one` and `two`? We could use a **built-in Python method** for manipulating variables and data.

1. To join variables together use the `+` symbol, this is called concatenation.

```python
one + two
```

You should see `3.0` as your answer. We just added the data in variable `one` and `two` together.

What would happen if we added variables `var` and `three` together?

```python
var + three
```

Python strings are "immutable" which means they cannot be changed after they are created (Java strings also use this immutable style). Since strings can't be changed, we construct *new* strings as we go to represent computed values. So in this example we concatenate `var` and `three`, which builds a new string 'Hello Worldthree'.

Other methods that you can use on integers and floats:

- division:

```python
one / two
```

- multiplication:

```python
one * two
```

- We can also assign a truth value to a variable, called a *boolean*.

```python
var_true = True
var_false = False
```

We can then check if these two variables contain the same truth value.

```python
var_true == var_false
```

In Python `=` is used to assign values to a variable, and `==` is used to check if two variables contain the same value. `True` in Python is interchangeable with the number `1` and `False` with `0`.

### Data Structures

All this typing can get tedious, so Python has a way to store multiple variables in one variable with more complex data types. These are called *data structures*.

**1. Lists**

If we wanted to take the names of some popular DH tools, we could store them in a data structure called a *list*.

```python
tools = ['Twitter', 'Gephi', 'HathiTrust']
```

A list is an unordered, comma-separated collection of any values. So we can store any combination of values in our list.

```python
tools = ['Twitter', 'Gephi', 'HathiTrust', 2019]
```

We can also store a list inside of another list.

```python
tools = ['Twitter', 'Gephi', 'HathiTrust', 2019, ['MALLET']]
```

What if you want to just print out 'Twitter' from the list? We can do that by *indexing* the list.

```python
tools[0]
```

Each list in Python is a sequence, and we can access the position of an item in that sequence through indexing. **In Python, indexes always start at zero!**

We can use indexing in all sorts of ways.

1. We can take the final item by using negative one, which tells Python to get the last item from the list

```python
tools[-1]
```

2. We can take a range of items by using a colon to specify when we want to start and stop

```python
tools[1:3]
```

3. If we try to index longer than the list, we'll get an error that tells us we're out of range of the list

```python
tools[8]
```

Now what if we wanted to add DH projects to our list? We could create a new list that contained the projects and then use concatenation to join them.

```python
projects = ['Prof Gender', 'Ngram Viewer']
tools + projects
```

We can see in the interpreter that we now have a list containing both lists, but what happens if you type tools again?

Remember to store values, we need to *assign* them to variables.

```python
projects = ['Prof Gender', 'Ngram Viewer']
new_list = tools + projects
```

We can also add items and remove them from the list. Let's take a look at some of these methods [https://www.w3schools.com/python/python_ref_list.asp](https://www.w3schools.com/python/python_ref_list.asp). You can read more about them in the python documentation [https://docs.python.org/3/tutorial/datastructures.html](https://docs.python.org/3/tutorial/datastructures.html) and in Melanie Walsh's textbook [https://melaniewalsh.github.io/Intro-Cultural-Analytics/02-Python/06-String-Methods.html#id1](https://melaniewalsh.github.io/Intro-Cultural-Analytics/02-Python/06-String-Methods.html#id1).

**2. Dictionaries**

We can use a *dictionary*, which is a collection of key/value pairs to store this information. Keys and values are always separated by a colon.

```python
tool = { 'name': 'Gephi', 'founded_year': 2008}
```

To access our values in dictionaries, we don't use indexing. Instead, we use the keys of dictionary. Keys are always the values that come before the colon.

```python
tool['name']
```

We write the key inside of brackets and quotations, called *bracket notation*.

What happens if we add another tool to the dictionary?

```python
tool = { 'name': 'Gephi', 'founded_year': 2008, 'name': 'HathiTrust'}
```

Where's Gephi??

Gephi was overwritten in our dictionary because our new value shared the same key. In a dictionary, keys must be unique!

Just like lists though we can store a dictionary inside of a dictionary

```python
tools = {
    'tool_1': {
        'name':'HathiTrust'
    },
    'tool_2': {
        'name': 'Gephi', 
        'founded_year': 2008
    },
}
```

Now we can get Gephi's name if we type `tools['tool_2']['name']`. What's happening here is that we're using the keys to find our value that's nested inside a dictionary within a dictionary.

We can add Gephi's release year by using a similar notation:

```python
tools['tool_2']['founded_year'] = 2008
```

You can also get even crazier and store lists in dictionaries:

```python
tools = {
    'tool_1': {
        'name':'HathiTrust',
        'projects': ['Bookworm', 'Google Ngram Viewer']
    },
    'tool_2': {
        'name': 'Gephi',
        'founded_year': 2008
    },
}
```

Notice that the list is a value of a key, in this case `projects`. You can only insert a list into a dictionary as a value.

You can also put dictionaries inside of lists:

```python
tools = [
    {
        'name':'HathiTrust',
        'projects': ['Bookworm', 'Google Ngram Viewer']
    },{
        'name': 'Gephi',
        'founded_year': 2008
    }
]
```

Notice that we now don't have keys for our top-most dictionaries. In lists, items don't have keys, so each of your dictionaries is without an explicit key.

Python defaults to indexing each dictionary with numbers, just like in our list of strings. So to get the first value, you would type:

```python
tools[0]
```

Just like lists there are many ways to manipulate dictionaries
[https://www.w3schools.com/python/python_ref_dictionary.asp](https://www.w3schools.com/python/python_ref_dictionary.asp)

## Advanced Python

Python interpreter is great, but why might we not want to write all our code in the interpreter? What happens every time you quit?

Open your terminal directory in Visual Studio Code or your favorite code editor, and create a new file:

```sh
touch first_script.py
```

You should see this file in Visual Studio Code. We're going to write your first code script! Feel free to enter some of what you wrote for the exercise, or copy this below:

```python
tools = [
    {
        'name':'HathiTrust',
        'projects': ['Bookworm', 'Google Ngram Viewer']
    },{
        'name': 'Gephi',
        'founded_year': 2008
    }
]
```

1. Now try running the file from your terminal
Make sure you are not in the python interpreter. Type:

```sh
python3 first_script.py
```

What happens?

<figure>
    <a href="https://media.giphy.com/media/3KCOFfdqmptLi/giphy.gif">
    <img src="https://media.giphy.com/media/3KCOFfdqmptLi/giphy.gif" alt="First Script" class="image-popup">
    </a>
</figure>

Because we aren't in the interpreter any more, unless we tell the computer to output a value it won't show us any message (unless there's an error.)

One solution is the **print** method.

In first_script.py, add the line to the bottom of the script:

```python
print(tools)
```

This time you should see the list of tools.

Now try moving that line to the top of first_script.py and running the script again.

<figure>
    <a href="https://media.giphy.com/media/qQI16x8tgp7nW/giphy.gif">
    <img src="https://media.giphy.com/media/qQI16x8tgp7nW/giphy.gif" alt="First Script" class="image-popup">
    </a>
</figure>

We've hit a problem. Let's break down what happened here. If the print statement was at the bottom of the script it worked, but if it was at the top it didn't.

That's because the print statement within it's parentheses references the variable `tools`, but we haven't defined that variable yet.

**Computers read code from top to bottom**

So what's the print statement?

Print is another *built-in Python method*, which means it comes installed with Python and we can use it whenever we are writing Python.

Print is used to literally print out values to the terminal, and it's one of many ways to find out the output of a Python script.

Print is one of many methods. Let's take a look at a few more.

1. `Len()`
In first_script.py, move the print statement back to the bottom of the script. Then above the print statement type:

```python
tools_numbers = len(tools)
print('how many DH tools do we have?', tools_numbers)
```

Then try running the code. You should first see our question followed by a number and then the list of projects.

The **len** method can return the length of any list, dictionary, or string in Python.

2. `Type()`
You might also want to know the **type** of your variable, whether it's a data type or a data structure. In first_script.py, add to the bottom of the script:

```python
print(type(tools), type(tools[0]))
```

Once you run the script you should see that we have both a list and a dictionary. With print statements you can add multiple items as long as they are separated by commas, and you can use built-in methods inside the print statement, instead of assigning them to a variable first.

3. `Input()`
You can also get input from the terminal using the **input** method. In first_script.py, type the following at the bottom of the script:

```python
print('Enter your name:')
name = input()
print('Hello, ' + name)
```

<figure>
    <a href="https://media.giphy.com/media/3o7buirYcmV5nSwIRW/giphy.gif">
    <img src="https://media.giphy.com/media/3o7buirYcmV5nSwIRW/giphy.gif" alt="First Script" class="image-popup">
    </a>
</figure>

*What did we just do?*
First we printed out a prompt. Then we assigned the input method to a variable, and then we printed out hello concatenated with the value of name.

You've now used built-in methods before for both dictionaries and lists. But they exist for data types too.

### Built-In Methods for Strings

1. `Split()`
The **split** method lets us split up a string and turn it into a list. In first_script.py, add the following:

```python
definition_of_dh = 'DH is 1) using new digital tools to do humanistic research and 2) using humanistic methods to analyze new digital tools.'
print(definition_of_dh)
print(definition_of_dh.split(''))
```

<figure>
    <a href="{{site.baseurl}}/assets/images/def_dh.png">
    <img src="{{site.baseurl}}/assets/images/def_dh.png" alt="DH Definition" class="image-popup">
    </a>
</figure>

1. `Join()`
The **join** method lets us take a list and join all the values together.

```python
split_definition = definition_of_dh.split(' ')
joined_definition = '_'.join(split_definition)
print(joined_definition)
```

1. `Replace()`
The **replace** method lets us find a string and replace it with another string. You can also specify how many times you want to replace a string.

```python
edited_definition_of_dh = definition_of_dh.replace('tools', 'people') 
print(edited_definition_of_dh)
```

1. `Upper()` and `Lower()`
The **upper** and **lower** methods return the entire string capitalized or lowercased respectively.

```python
print(definition_of_dh.upper(), definition_of_dh.lower())
```

You can find more information about string methods here
[https://www.w3schools.com/python/python_ref_string.asp](https://www.w3schools.com/python/python_ref_string.asp)

### Commenting and Documentation

#### Inline Commenting

Comments are especially useful--necessary!--for collaboration. Python is open source and its community of millions of coders often share in its permissive approach to intellectual property. Python as a whole is a giant collaborative project of which you are now members.

When you write particularly complicated logic or whenever you write new classes or functions (more on this later!), you should write a comment to explain yourself.

```python
edited_definition_of_dh = definition_of_dh.replace('tools', 'people') 
print(edited_definition_of_dh)
```

#### Documentation

Python, as with virtually all other languages and complex codes, contains extensive documentation that covers all aspects of its use. This documentation is [easily accessible via the Internet](assets/MissionImpossible.m4v?raw=true).

[Python 3 Documentation](https://docs.python.org/3/)

Let's take a look at the specific documentation for strings:

[Python 3 Docs: Built-in Types: Strings](https://docs.python.org/3/library/stdtypes.html#string-methods)

Learning to read documentation is a critical skill for succeeding as a programmer. Happily, most of you, as graduate students, should already be literate.

### Control Flow

Computers read code line by line, top to bottom of a script. But what if you want to have code run not in sequential order, or you want your code to do something depending on a value, or you want to reuse your code and run it multiple times?

We can solve all those problems with data flow structures.

#### Looping

Earlier you had to print out multiple values from the tools dictionary. While typing each value out is tedious, it was still possible to do. However, what would happen if you had hundreds or thousands of values?

There's a much faster way to traverse data structures and types in Python, called `Looping`. With various types of loops in Python, you can travel through a sequence (i.e. a list, dictionary, string, etc...) to be able to manipulate items within the sequence.

**For Loops** are one of the most common ways in python to loop over a sequence. But what does looping mean exactly?

Let's go back to our script from our script, and find our list of names. Add these lines to the script:

```python
tools=["Gephi", "R", "Python", "HathiTrust"]
for tool in tools:
    print(tool)
```

<figure>
    <a href="https://www.learnbyexample.org/wp-content/uploads/python/Python-for-Loop-Syntax.png">
    <img src="https://www.learnbyexample.org/wp-content/uploads/python/Python-for-Loop-Syntax.png" class="image-popup">
    </a>
</figure>

We can also use For Loops on dictionaries. The syntax is slightly different because dictionaries are not one long sequence, but rather a sequence of key/value pairs.

```python
tools = {"Python":{"2015":9, "2016":22, "2017":27, "2018":32, "2019":35}, "Javascript":{"2015":8, "2016":18, "2017":12, "2018":6, "2019":15}, "Twitter":{"2015":10, "2016":18, "2017":26, "2018":16, "2019":12}, "Github":{"2015":2, "2016":6, "2017":17, "2018":5, "2019":10}, "Gephi":{"2015":11, "2016":16, "2017":14, "2018":10, "2019":9}, "Geonames":{"2015":2, "2016":4, "2017":3, "2018":1, "2019":8}, "Transkribus":{"2015":0, "2016":1, "2017":2, "2018":1, "2019":8}, "Excel":{"2015":5, "2016":9, "2017":3, "2018":6, "2019":7}, "MySQL":{"2015":0, "2016":6, "2017":9, "2018":5, "2019":7}}

for key, value in tools.items():
    print('key', key)
    print('value', value)
```

Or even strings.

```python
for letter in 'Digital Humanities':
    print(letter)
```

For more about looping in Python checkout [https://wiki.python.org/moin/ForLoop](https://wiki.python.org/moin/ForLoop) and [https://www.learnpython.org/en/Loops](https://www.learnpython.org/en/Loops).

#### Functions

Looping is very powerful, but if we want to loop through a second list of names or a different variable, we would have to repeat our code later in the script. An alternative is to create a function.

A function is a way to organize code by packaging many lines of code together into a single bundle. At the most basic level, this makes it easy to reuse code: it's easier to write out and read a single line rather than many lines and easier to change code in one place rather than in many places.

**Function Syntax**

<figure>
    <a href="https://www.askpython.com/wp-content/uploads/2019/06/python-functions.png">
    <img src="https://www.askpython.com/wp-content/uploads/2019/06/python-functions.png" class="image-popup">
    </a>
</figure>

To create a function, we define using `def` and a unique name and finally parentheses, followed by colon. Then we can pass *arguments* (also called parameters) in the parentheses, that we can that use *inside* of the functions. Those arguments will be *variables* and so we can do anything you would normally do to a value. Finally we can *return* the result of our manipulation.

For example try:

```python
def get_fundamentals():
    fundamentals = 'Having fun'
    print(fundamentals)
    return fundamentals

get_fundamentals()
```

What would happen if you try to access the variable `fundamentals` after the line `get_fundamentals()`?

Spoiler alert you'll get this message:

```sh
NameError: name 'fundamentals' is not defined
```

We get that error because `fundamentals` is only defined in the **local scope** of the function. That is the variable `fundamentals` only exists within the function and can only be accessed within it. This is why when writing functions we either use two or four spaces (or tabs) to indent our code.

This is called "white space", and indicates to Python that everything that's indented is part of the function definition. As soon as we stop indenting, the function definition is over. We can use any number of spaces or tabs, but they have to be consistent. Notice we also used white space in the For Loops. Similar to in our function, variables defined within the for loop are only available within the local scope of the loop.

We also use something called a **return statement**.

```python
def get_fundamentals():
    fundamentals = 'Having fun'
    print(fundamentals)
    return fundamentals

new_fundamentals = get_fundamentals()
```

If you printed out `new_fundamentals` what would this variable contain? You might expect it to print out the function, but it will actually print out the local variable `fundamentals`.

Return is used to pass data back from the function, which can then be assigned to a new variable that's accessible in the rest of the script, also known as the **global scope**.

```python
def get_fundamentals(code_concept):
    fundamentals = 'Having fun, ' + code_concept
    return fundamentals

new_fundamentals = get_fundamentals('for loops')
```

We can also pass in data to our functions through the parentheses when we call and define our functions. This is called passing **arguments** into our functions. In this example, what does `new_fundamentals` contain?

Arguments can have any name (so our example above could have named `code_concept` as `data` or `x`) and can contain any data type or structure.

Using functions and for loops we can reuse our code whenever we want within our script.

For example, try and understand this code from our assignment exercise:

```python
def make_tool_dict(name, value_2015 , value_2016, value_2017,value_2018, value_2019):
    return {
        "2015":value_2015 ,
        "2016":value_2016,
        "2017":value_2017,
        "2018":value_2018,
        "2019":value_2019,
        "name":name,
        "total":value_2015+value_2016+value_2017+value_2018+value_2019
    }

dh_tools=[make_tool_dict("Python",9,22,27,32,35),
          make_tool_dict("JavaScript",8,18,12,6,15),
          make_tool_dict("Twitter",10,18,26,16,12),
          make_tool_dict("GitHub",2,6,17,5,10),
          make_tool_dict("Gephi",11,16,14,10,9),
          make_tool_dict("GeoNames",2,4,3,1,8),
          make_tool_dict("Transkribus",0,1,2,1,8),
          make_tool_dict("Excel",5,9,3,6,7),
          make_tool_dict("MySQL",0,6,9,5,7)]

print("\nPrinting tools...\n")
for tool in dh_tools:
    for prop in ["name","2015","2019","total"]:
        print(prop+": "+str(tool[prop]))
    print("")
```

What arguments does the `make_tool_dict` function take and what value does it return?

What does `dh_tools` variable contain?

What is the for loop iterating through? What does `str(tool[prop])` do?

For more on functions, checkout this tutorial [https://www.datacamp.com/community/tutorials/functions-python-tutorial](https://www.datacamp.com/community/tutorials/functions-python-tutorial)

#### Conditional Statements

Earlier we learned about *booleans* (`True or False`). In Python, we can test the truth value of code to decide how we want our code to run.

<figure>
    <a href="https://automatetheboringstuff.com/images/000019.jpg">
    <img src="https://automatetheboringstuff.com/images/000019.jpg" class="image-popup">
    </a>
</figure>

A conditional is a way for a computer program to make a choice. The basic syntax of the conditional in many programming languages is the `if` statement. In Python, it looks like this:

```python
x = 5
if x>0:
    print("Positive")
```

If statements are essentially expressions that follow `if` and end with a `:`. We indent whatever code we want to run if that expression is successful within that code block, just like with functions or for loops. In this case, when whatever value we assign to `x` is *greater than* zero our script will run the print statement. What happens if we assign `x` to `-1`?

```python
x = 5
if x>0:
    print("Positive")
elif x<0:
    print("Negative")
else:
    print("Zero")
```

We an also use additional conditional keywords `elif` (else if) and `else` to add more complexity to our code. Each of the conditional blocks (the three `print()` statements) are only run if the associated conditional statement is `True` (in the boolean logic sense). We can have multiple `elif` blocks if we want. We can also omit `elif` and `else` blocks altogether.

We can also test more complicated comparisons using various comparison operators:

<figure>
    <a href="https://introcs.cs.princeton.edu/python/appendix_cheatsheet/images/ComparisonOperators.png">
    <img src="https://introcs.cs.princeton.edu/python/appendix_cheatsheet/images/ComparisonOperators.png" class="image-popup">
    </a>
</figure>

For numbers, we can use `>`, `>=`, `==`, `<`, and `<=` to make numeric comparisons. If we want to modify or chain together boolean statements, we can use `and`, `or`, and `not`:

```python
x = 5
y = -1
if x>0 and y<0:
    print("both expressions true")
```

For strings, we can use use `==` for comparison and some special operators like `in` to see if one string exists inside of another.

```python
if 'I' in 'TEAM':
    print('at least one')
else:
    print('no')
```

If a variable is the special `None` object, an empty string (""), or the numeric value zero, it evaluates as boolean `False`. Otherwise, it is `True`.

```python
fundamentals = ''
if fundamentals:
    print('Yay!')
else:
    print('Nooo...')
```

We can also test the equality of two variables in an if statement:

```python
top_tool2015 = 'Gephi'
top_tool2019 = 'Python'
if top_tool2015 != top_tool2019:
    print('Change over time')
else:
    print('More they stay the same')
```

For more information about control flow, read the [Python documentation on the topic](https://docs.python.org/3/tutorial/controlflow.html).
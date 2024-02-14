---
title: "Getting Data From APIs"
permalink: /materials/creating-curating-humanities-data/06-getting-data-apis
excerpt: "An introduction to using APIs to get data from the web."
toc: true
---

So far in class we have briefly mentioned APIs (for example, the Genius and Spotify API), but haven't yet discussed what they are or how to use them. This week we will start to work through the basics of using APIs to get data from the web.

## What is an API?

API stands for Application Programming Interface.What does that mean exactly? 

While according to Wikipedia,

> An application programming interface is a connection between computers or between computer programs. It is a type of software interface, offering a service to other pieces of software. A document or standard that describes how to build or use such a connection or interface is called an API specification.

But that probably leaves you with more questions than answers.

Let's try looking at specific API to figure out what this means. We'll be working with the DPLA API (the same one that is our reading of Yanni Alexander Loukissas, *All Data Are Local*).

If you pull up their documentation for their API [https://pro.dp.la/developers/api-basics/](https://pro.dp.la/developers/api-basics/), you'll notice they begin with a helpful explanation for what is an API.

<figure>
    <a href="{{site.baseurl}}/assets/images/dpla_api_basics.png">
        <img src="{{site.baseurl}}/assets/images/dpla_api_basics.png" alt="DPLA API Basics" class="image-popup">
    </a>
</figure>

In this documentation, the talk about APIs as a type of language similar to HTTP. To help us understand this connection, let's also take a look at this figure:

<figure>
    <a href="https://assets-global.website-files.com/5f3c19f18169b62a0d0bf387/609b09fb261ba04c095064cb_https-lh6-googleusercontent-com-_nyclktg8po_wx5-.png">
    <img src="https://assets-global.website-files.com/5f3c19f18169b62a0d0bf387/609b09fb261ba04c095064cb_https-lh6-googleusercontent-com-_nyclktg8po_wx5-.png" alt="API Workflow" class="image-popup">
    </a>
</figure>

You'll notice that we have a web browser that is using the "internet cloud" to make requests and get responses from an API that is connected to a web server and a database. This might seem complex, but we've seen a similar relationship when we talked about how the web works. We talked previously about how web browsers use HTTP to make requests and get responses from web servers, this is the same idea. APIs are just a way to get data from a server, similar to how we get web pages from a server, but instead of storing the data in a webpage (aka an HTML document), the data is stored in a database. For example, when you use a weather app, or really any app on your phone, that app is using an API to get the weather data from a server.

Databases might also sound intimidating, but they are just a way to store data, similar to csvs or excel files. The difference is that databases are designed to store large amounts of data and to allow that data to be accessed and manipulated quickly, usually using something called SQL (Structured Query Language).

Rather than going to a URL in your browser, an API lets us send a similar request to a server, and then we can get the data we want. If you want a bit more in-depth introduction you might check out this medium post <https://medium.com/epfl-extension-school/an-illustrated-introduction-to-apis-10f8000313b9>.

**Big takeaway is to realize that so far we have been getting data by either downloading CSVs or scraping from the web. APIs let us get usually larger amounts of data that would be either difficult to download or difficult to scrape.**

So let's try this out with the DPLA API.

## Working with DPLA API

There's a few ways we can work with the DPLA API. First we are going to be working with the `requests` library we used in the Intro to Web Scraping lesson. But if you are having issues authenticating with the API, you can jump ahead and use the `DPyLA` library, which is a Python library to work the DPLA API.

### Request(ing) Data

Our first step when working with an API is to authenticate. This sound intimidating but you do it all the time whenever you login to your email, DUO, social media, etc...; it's just usually this is handled automatically by your browser. Because we aren't using a browser with APIs, we need to do this explicitly by making a request to the API to get an authentication key and token.

For DPLA we will follow these instructions [https://pro.dp.la/developers/policies#get-a-key](https://pro.dp.la/developers/policies#get-a-key), but it's worth noting that many APIs have different ways of authenticating so you should be sure to read their documentation (usually available under developer documentation, like this one from the Spotify API [https://developer.spotify.com/documentation/general/guides/authorization/](https://developer.spotify.com/documentation/general/guides/authorization/)).

First, let's get our DPLA token!

On Macs/WSL, open your VS Code terminal and type:

```sh
curl -v -XPOST http://api.dp.la/v2/api_key/YOUR_EMAIL@example.com
```

On Windows, open your VS Code PowerShell terminal and type:

```sh
Invoke-WebRequest -Uri ("http://api.dp.la/v2/api_key/YOUR_EMAIL@example.com") -Method POST -Verbose
```

In both examples, replace `YOUR_Email@example.com` with your email (can be any email address). If you run into issues, again feel free to jump ahead and authenticate with DPyLA.

Once you've completed that step, go to your inbox and you should see an email from the DPLA with your API key, which is a long list of alphanumeric characters.

Copy that key and we are going to store in a new Python script. Create a new folder in `is310-coding-assignments` called `api-getting-data` and then create a new script called `first_api_script.py` and import requests into the script. Then save your key into a new variable called api_key.

```python
import requests

api_key = "YOUR_API_KEY_HERE"
```

Now we can look at the DPLA API documentation to see how we can start getting data from their databases [https://pro.dp.la/developers/requests](https://pro.dp.la/developers/requests).

Let's start with the simple search example [https://pro.dp.la/developers/requests#simple](https://pro.dp.la/developers/requests#simple).

Copy their example url into your script and save it as the variable `url`. Then try to get the data from the API using the `requests.get` method we've used previously.

```python
url = 'https://api.dp.la/v2/items?q=kittens&api_key='

response = requests.get(url + api_key)
```

Notice that the end of the `url` variable is `api_key=` and that in the requests.get, we are concatenating url and api_key. That's how we pass our key to the DPLA API so that it knows who we are and that we are allowed to use their API. While we have discussed HTTP in our Intro to Web Scraping class, we haven't really broken down what a url is exactly.

#### What is a URL? 

URL actually stands for Uniform Resource Locator. It's a way to identify a specific document (remember document is what we call web pages) on the internet and also includes instructions on how to access the document (remember HTTP headers -- yes, they are confusing but they do help browsers understand how to load data and web pages). The [Mozilla docs has a great introduction to URLs](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL) and helps see that the basic structure of a URL is the following:

![url structure](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL/mdn-url-all.png)

What we are using in our example is a URL is first a scheme `https`, then a domain `api.dp.la`, then a path `/v2/items`, then a query `q=kittens`, and then a key `api_key=` and then the actual key. Everything after the `?` is called a query string and it's where we set [the parameters](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL#parameters) (or arguments --- yes exactly like a function in Python!) that we want to pass to the API.

#### What is a response?

So now we have a sense of how we are composing our API request URL, let's take a look at the response. We've used the `get` method from requests, which if we go to the documentation <https://docs.python-requests.org/en/master/api/#requests.get>, tells us that this method or function returns a `requests.Response`. Now since we know that requests is the library, what we are really interested in is this `Response` class <https://docs.python-requests.org/en/master/api/#requests.Response>.

According to the documentation, this class contains:
> The Response object, which contains a server’s response to an HTTP request.

The first few bolded options underneath the Response object are the methods we can use with this class. We've already tried one of them in class on Tuesday <https://docs.python-requests.org/en/master/api/#requests.Response.status_code>.

Let's try to print out the status code.

```python
response.status_code
```

What does `200` mean again? 

How could we see what data got returned from the API? We could use two methods, either `.text` or `.json()` Let's try to print out the response, using the json one.

```python
response.json()
```

You should see something like the following:
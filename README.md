
# An End to End Data Cleaning Example


## Introduction
In "week 0", we installed the key tools required to do data capture and cleaning with Python and to complete this course (git, GitHub and Anaconda). In week 1, we introduced the basics of Python programming - variables, some simple data types (String, Integer, Floating Point, Boolean and Date Time), some of the more complex data types (List, Tuple, Set and Dictionary), and control flow using if statements and (for looping over collections), "for-in" loops and (for extra credit) list comprehensions. *Don't worry if you're still a little confused by list comprehensions - you don't have to master them to be able to clean up data!*

A lot of the tasks last week were "small motion" lessons. You got to practice little bits of a project, but didn't really pull it together into a more realistic end-to-end experience. Today, we're going to build on the knowledge you gained last week to do an end to end data cleaning example. We're going to import some company data, clean it up and then save it to a new file.

To keep things easy, we'll just focus on cleaning up the capitalization of text from a csv file filled with company information. In a real world example you'd probably want to do more complicated clean up, but once you've seen how to do the basics, it'll be quite easy to add a little more sophistication or complexity to the data clean up in future lessons.

We're also going to have to introduce a few new concepts along the way. We're going to introduce the concept of libraries (pre-written software that you can use to write your code more quickly), Pandas (one of the most popular libraries for working with data in Python) and the Pandas Series and DataFrame (the standard ways to store information within Pandas). It might seem like a lot of theory, but in practice you'll be using Pandas DataFrames for most of your data import, cleanup and export operations, so it's important to take the time to introduce them now.


## Objectives
You will be able to:
* Explain what a library is and why you might want to use one
* Explain what a Series and DataFrame is and why you would use them
* Import data from a csv file into a DataFrame
* Transform data within a DataFrame to clean it up
* Export data from a DataFrame into a csv

## Review
Lets start with a quick review from last week with a few quick questions . . .
* **Which two of the simple data types above are generally best for working with numbers?**
* **What's the difference between those two types?**
* **How would you take a string containing whole numbers (no fractions or decimals) and turn it into a numeric data type?**
* **If you have an unchanging list (e.g. a list of US states) that should not have any duplicates, what would be the best (complex) data type to store that?**
* **If you have a list of companies with company name, address and website for 50 companies, what two complex data types would you combine to store that information in Python?**

## Introducing Libraries
Libraries are pre-written pieces of software that you can use to write software more quickly. There are lots of pre-written libraries in Python for doing everything from storing and manipulating data to plotting graphs to creating Neural Networks. 

## Introducing Pandas
[Pandas](https://pandas.pydata.org/) is one of the most popular Python libraries for anyone working with data. It is a library providing high-performance, easy-to-use data structures and data analysis tools.

## Introducing the Pandas Series and DataFrame
At the heart of the Pandas library are two special data types - the Series and the DataFrame. A Series is used for storing and operating on a single dimensional data set - something that you might have previously put into a List or a Tuple. An example of the kind of data you'd put into a Series would be a list of US states or a list of company names.

A DataFrame is used for storing and operating on two dimensional data - anything you might put into a spreadsheet that has more than one row and more than one column. It could hold a list of companies with the name, address and phone number for each company or a list of people with the first name, last name, email address and date of birth for each person.

In practice we're going to use a DataFrame most of the time as we'll often be importing two dimensional data from csv files or creating it by pulling information from an API or a website.

## An Overview of the Data Cleaning Process
In practice, the overall process of data cleaning that we're going to run through today is pretty straightforward:
* **Import data** - from a csv file into Python (specifically saving it in a Pandas DataFrame)
* **"Look" at the data** - perhaps running some summary statistics 
* **Clean up the data** - iterating over the data in any given column to clean it up
* **Export the data** - typically to a csv file so you can import it into another application for further analysis or processing

Alright, let's give it a try!

## "Importing" the Library
Before we can use a library in Python, we have to tell Python that we want to include that library in our code. That is called "importing" the library. Here's the code. Make sure to run it, otherwise the rest of this notebook isn't going to work.


```python
import pandas as pd
```

Let's have a look at the code:
* **import** is a Python key word telling Python that we're just about to give it the name of a library that we want to be able to use
* **pandas** is the name of the library - we generally capitalize the P when referring to the library in writing, but when we want to import it into Python, it has to be written using lower case. *If you capitalize the P and run the code you;'ll get a "library not found" error - feel free to try it out in the cell above!*
* **as** is another Python keyword. This is optional, but it allows us to declare a shorter *alias* for the library so for the rest of the notebook instead of having to type `pandas` every time we want to refer to the library, we can type something else (typically something shorter to save us some typing)
* **pd** is the common shortening of `pandas` that most Python programmers will use. It's a good idea to follow common conventions like this so that other programmers looking at your code can understand it more easily.

## Summary



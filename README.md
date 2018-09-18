(Below is transcript from lessons on Code Institute)

## Core Python - Introduction

Since development began and the language in the mid to late 80s Python has undergone several major releases. Since then the first released in the early 90s which was version 1 and subsequently version 2 and the most
recent version which is version 3. Hi my name is Aaron Sinnott, a senior product developer here at Code Institute. So python has a number of uses and a number of different ways that we can execute Python code and there are also different tools and libraries available to us that we can use to enhance and also to add to our project so we don't have to develop logic ourselves so throughout this we're going to learn how we're going to look at executing simple Python statements in the interpreter which is an environment similar to the repl.it environment. It allows us to test code pretty handy and pretty quickly and find out if our logic is going to work or not. We'll be looking at executing code that exists within a .py file so a Python file uses the .py extension and we look at how we can execute code that lives inside a .py file and installing additional dependencies using
pip which is a tool that allows us to install additional packages that have been developed by third-party vendors. So the learning outcomes for this section are going to be we're going to learn how to use the Python interpreter we're going to learn how to execute Python files and we're going learn how to use pip to install additional libraries and frameworks.
End of transcript. Skip to the start.

## Getting started with Python in Cloud9

# Making sure that we're using Python 3

The first thing that we're going to do to get up and running with Python is we're going to create a brand new workspace and call it core python. This is going to be a blank workspace and then I'm going to click on create workspace. So what we're going to do in this video is we're just going to go through some of the different versions and some of the kind of discrepancies that exist in Python. So for example Cloud9 comes with several versions of Python pre-installed and the version that we are going to be using for the duration of this course is going to be Python 3. The reason that we're going to be using Python 3 is because it is the latest version and also there are certain differences between Python 2 and python 3. So when python tree was being created backwards compatibility was not a concern so certain things have changed or have been broken between the two versions. So in order to ensure that we're using the right version we're just going to take a look at some of the Python versions that we have here. So the first thing that I'm going to do - once my workspace is created - is I'm going to open up the terminal. There is something strange happening here so I'm going to close my terminal down at the bottom of the screen and then open up a new one. And what I can do then is I can say which python. Python is an executable file which is installed in a directory so if I use the which command then it'll tell me where this file is installed. So this file is currently installed in the bin directory which is contained in the usr directory. So we can do an ls /usr/bin/ | grep python and this will allow us So when we run this command we can see all of the different versions of Python that have been installed. Here we have Python 2, Python 2.7, Python 3, Python 3.4 so on and so forth. What we want to do is we just want to clear up some of this so what I'm going to do is I'm going to run Python -v here. This didn't give me the output I was wanting. What I wanted was version so let's run Python - - version which will print out the version. We can see that the version of this Python is 2.7.6 What we actually want to be using is Python 3. If I go ahead and run the python command it will open up the Python interpreter for us and we can execute inline code. So if I run the Python command here I can do print "Hello world" and this will print out Hello world. This is an artifact of Python 2 that doesn't exist in python 3. One of the biggest changes in python 3 was that print was changed from a statement to a function. So we have to use parentheses in order to use a print function. So if I type in Python 3 - -version we get to Python 3.4.3. If I run a python3 command it will open up Python 3 in an interpreter. As we can see when I try to run the print statement it gives me a syntax error saying I'm missing parentheses. The print parentheses indicate this is a function taking an argument so when we modify this accordingly we get the term Hello world printed out. End of transcript. Skip to the start.

# Executing Python Code

What is it?

The different ways that we can execute Python code

What does it do?

Allows us to execute code from a file or an inline interpreter similar to repl.it

How do you use it?

By using the python3 command

LESSON:
    So now we know that we're using the correct version of Python we can go ahead and quit our interpreter. We can go ahead and I'm going to right click on the core Python directory here and create a new File. I'm going to create this file called python.py for now. I'm going to pop in some Python code. I'm going to say def print_message. We'll give this a parameter of message. Next we're going to call the print function inside of
    there and pass through message as an argument. Underneath that we're going to invoke our print message function and pass through a message that says hello world. I'm going to save that by pressing CTRL+S on Windows (CMD+S on Mac). In order to execute that file then I have to run python3 python.py and this will output Hello world. If I open the interpreter and run python3, I can do the same thing. I can say def print_message(message): print(message) and hit return. (I have to do four spaces). Then I can put print_message("Hello world") and then I hit enter twice to exit out of the
    print message function. Then I just called that in the same way that I did previously. So this will print that message - it says Hello world. We can also create, say for example, a list. So my_list is equal to [1, 2, 3, 4, 5] all separated by commas. Then we can do a for loop to iterate over those. I can say for item in my_list: and hit return and then I just press space four times and say print(item) and hit enter twice. We can see that 1 2 3 4 5 has been printed out. I can do the same thing by putting this code into a file. I'm now saying my_list = [1, 2, 3, 4, 5]. Below that I will just say for item in my_list: print.
    I'm back in my terminal I'll quit out of the interpreter by using the quit
    function. Then I will say python3 python.py and I'll get those numbers
    printed out again
    End of transcript. Skip to the start.
    
# PIP3

What is it?

pip3 is a Python tool

What does it do?

It helps us to manage project dependencies

How do you use it?

By using the pip3 command

LESSON:
    So now that we've seen how we can use the Python 3 executable to run code.
    What we want to look at now is another Python tool called pip and pip is the means of handling and managing dependencies. So for example we have the standard library in Python which contains modules such as OS and math modules and stuff like that but it doesn't contain everything that we would always ever need. For example here's one - from flask import flask. Flask is a Python framework that we'll be looking at later on in this module. So we don't need to know anything about it now we just need to know that it is a module that needs to be installed so if I run my Python3 python.py command I'll get an error saying no module named flask. So what I need to do is I need to install flask so I say sudo pip3 and pip3 is the tool that we use to install and manage dependencies so I'm going to say sudo pip3 install Flask. We're going to install it globally - we need root privileges to install it so once that's done then if I run python3 python.py I won't get any output at all. The reason I won't get any output is because we're not actually
    expecting any output. We're not doing any print statements we're literally just trying to see if we can import the module. If we weren't able to import the module we would get a reference error like we did previously whereas now we're not getting any error   shows that it works. The next thing we can do is pip3 freeze - - local. This will tell us all
    of the packages that we've installed as we can see we've installed flask and we also have jinja2, MarkupSafe, Werkzeug and these are all packages that flask installed as it relies on them. So if I do what I can actually do then as well instead of just outputting this to the console I can say pip3 freeze --local and redirect our output to a file called requirements.txt. This is a really common way of persisting the dependencies in a project for example I would include this in a repository and then another developer would clone this repository and they'd be able to install the dependencies without me telling him what dependencies to install. So I'm just gonna go ahead here just to illustrate this I'm going to uninstall flask and I forgot to use sudo so I got a permission denied error so I'm gonna run sudo without space !! which will run the previous command as sudo which was pip3 uninstall Flask. I'm then going to use Python3 to run the python.py file and since we have uninstalled flask now we're getting our import error again so if I do sudo pip3 install and then - r (to say install recursively) from the requirements.txt file this will install all the requirements in our requirements.txt file. So I run my python3 python.py command again and we will see that this code runs fine. Don't worry too much about things like requirements.txt and freeze and flask for now we'll be taking a much more detailed look at these later on. For now we just want to make sure that we've looked at the command. End of transcript. Skip to the start.


   
   
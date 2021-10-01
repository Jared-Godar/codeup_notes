# Python Overview

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than right now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!

    -- The Zen of Python

General purpose programming language
Start with the basics

### Goals

- Understand how to use Python in it's various forms
- Understand the different data types in Python and how to manipulate them
- Understand the flow of control in Python programs (conditionals, loops, and functions)
- Understand how imports work and how to use them
- Understand the purpose of, and have a basic working knowledge of the following libraries:
    - `matplotlib`
    - `numpy`
    - `pandas`
    - `seaborn`
    - `sklearn`
    - `scipy`
    - `stats`

## Introduction To Python

Python is a high-level, dynamic, interpreted programming language that has gained a lot of popularity in the data science community.

### Python 2 vs 3

Python version 2 has been around for a long time, but is reaching it's end of life in 2020. Going forward the recommendation is to use Python version 3 for any new projects. Because of this, we will solely be using Python 3 for this course.

When you are searching the internet for Python-related questions, it is always wise to check and see which version of Python is being referenced, or to check the date on the information provided.

## Setting Up a Python Environment

For this course, we'll be using [anaconda](https://www.anaconda.com/) for our Python environment. Python has a very large ecosystem and there are many different libraries we'll want to use with it. Anaconda is a distribution of Python that has the "batteries included" for data science. This means that it has almost everything we'll need to do data science work and we won't have to spend a lot of time installing packages or downloading libraries ourselves.

    # Run these commands from your terminal. It does not matter what directory you are in.
    # install anaconda (this might take a minute)
    brew install --cask anaconda

    # add anaconda's tools to your PATH (this tells your shell how to find all of the anaconda programs)
    echo 'export PATH=/usr/local/anaconda3/bin:$PATH' >> ~/.zshrc

    # reload your configuration
    source ~/.zshrc
    If you did everything above correctly, you should be able to run the command below in order to see what version of Python you have installed:

If you did everything above correctly, you should be able to run the command below in order to see what version of Python you have installed:

    python --version

**High-level:** Closer to English
**Dynamic** Data types - can change and modify as needed
**Interprative** reads and runs as soon as you type it

Human-friendly language

**Curriculum update** Use

    echo 'export PATH=/opt/homebrew/anaconda3/bin:$PATH' >> ~/.zshrc

    # reload your configuration
    source ~/.zshrc

**REPL**

**READ**
**EVALUATE**
****
**LOOP**

Python by itself runs the REPL like a scratchpad

**ipython** Interactive python REPL in anaconda

Keep an ipython repl up all the time - use as a calculator
Line numbers and colors.

!ls from inside python repl -- `!` in front talks to terminal shell

Can keep open to do quick, little calculations or test things. Nice because able to interact with term as well as doing python stuff

To make a python file, `code hello.py`

Opens VS Code editor

run python from terminal - gold standard of how to run python- not from jupyter notebook or editor

`python filename.py`

highlight then shift + enter in VS code executes the highlighted portion of code

### Jupyter notebook

- Interactive environment
- Composed of elements called cells
    - Code cells
    - Markdown 
- Useful for making reports
    - Markdown formatting and images
    - Code
    - Comments
    - Data visualization embedded
    - Directly caption

Need a specific tool to run jupyter notebooks
`.ipynb` is jupyter notebook file extension
`.py` is python script

`python file.ipynb`

Can you use a jupyter notebook to open another file? Yes

File - new Python3 notebook

Python scripts are plain text. Sytactically correct python will run from the terminal. 

---
01OCT21

Now that environment is set up, we are getting into coding in Python.
Systematic approach to learning python good, but never ends. Always exposed to something new and learning more. Always huge sections out there to explore.

General programming language that it is, can make whole career in Python building software in that language.

[Youtube COrey Schaeffer](https://www.youtube.com/c/Coreyms): egood coding tutorials. Mostly python

Dictionaries of dictionaries - pain in the ass. Need to be comfortable with dictionaries for building and using data structures. 

https://codingbat.com/python

https://www.hackerrank.com/domains/python
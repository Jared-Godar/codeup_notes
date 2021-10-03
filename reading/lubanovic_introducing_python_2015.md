# Introducing Python
## Modern Computing in Simple Packages
### Bill Lubanovich 2015

---
**About Author** UNIX developer since 1977, GUIs since 81
**Target Audience** Ideal for beginning programmers as well as those new to the language

End of chapter exercises
- Strong foundation and best practices
    - Testing
    - Debugging
    - Code reuse
- Applications
    - Business
    - Science
    - Arths
- Tools and open-source packages

Learn:
- Data types
- Basic math and text operation
- Data wrangling with built-in data structires
- Code structure
- Functions
- Large programs
    - Modules
    - Packages
- Objects, classes, other object-orientated features
- Storage - relational database, NoSQL
- Build web clients, servers, APIs, and services
- Manage programs, processes, and threads
- Basics of network programming

---

## Preface

*Version 3.3* 

### Conventions Used in This Book

The following typographical conventions are used in this book:

*Italic*
Indicates new terms, URLs, email addresses, filenames, and file extensions.

`Constant width`
Used for program listings, as well as within paragraphs to refer to program elements such as variables, functions, and data types.

**`Constant width bold`**
Shows commands or other text that should be typed literally by the user.

*`Constant width italic`*
Shows text that should be replaced with user-supplied values or by values determined by context.

[Code Examples Online](https://github.com/madscheme/introducing-python) 

Cloned into /codeup-data-science/introducing-python/

An attribution usually includes the title, author, publisher, and ISBN. 

*Introducing Python* by Bill Lubanovic (O’Reilly). Copyright 2015 Bill Lubanovic, 978-1-449-35936-2.

-----

# 1: A Taste of Py

Special words and symbols `for`, `in`, `print`, `,`, `:`, `()`, etc **syntax**

Python has a nicer syntax which is easier to remember than many other programming languages.

**List**
Use `[]`

    cliches = [
        "At the end of the day",
        "Having said that",
        "The fact of the matter is",
        "Be that as it may",
        "The bottom line is",
        "If you will",
        ]
    print(cliches[3])

**Zero Indexing** By definition, the first item in a list is 0 and increases by increments of one.

**Dictonary**
Collection of *keys* and *values*, ise `{}`

    quotes = {
        "Moe": "A wise guy, huh?",
        "Larry": "Ow!",
        "Curly": "Nyuk nyuk!",
        }
    stooge = "Curly"
    print(stooge, "says:", quotes[stooge])

## Python in the real world

- Language has been around since 1991 (older than Java)
- Consistently top 10 programming languages
- Reputation of productivity that appeals to fast-moving organizations
- Ranges from one off *scripts* to million-line programs
- Found in many computing environments
    - Command line
    - GUIS
    - Web
        - Client
        - Server
    - Backend
    - *Cloud*
    - Mobile devices
    - Embedded devices

## Python vs. Language X

- C C++, low-level languages 
    - Used when speed is more important
    - Harder to learn
    - Track many details
- Java & C#
    - Successors to C
    - Somewhat verbose and restrictive

Static languages make you declare the *type* of each *variable*. Used to *compile* program into *machine languate* Language designers must make tradeoffs for making things easier for people or computers. 

In comparison, *dynamic languages* (anso called *scripting languages*) do not force you to declare variable types before using them.

*Interpreted* instead of *compiled* by *interpreters*. Slower than static languages

*Perl* was the all-purpose dynamic language for many years. Powerful and extensive libraries, but suntax can be awkward.

*Ruby* is more revent language. Borrows from *Perl*. *Ryuby on Rails* is a common web development framework. 

*PHP* is popular for web development. Easy to combine HTML and code. 

## So, why Python?

- Good general-purpose, high-level language
- Very *readable*
- Easier to learn and remember, more *writable*
- Gentle learning curve compared to other languages
    - More productive sooner
    - But still has immense depth to explore further
- Can write smaller programs than equivalent in static language
    - Programmers typically write same number of lines of code / day, regardless of language
    - So, writing half the lines of code doubles productivity
- Most popular intro CS language
- Most popular for evaluating programmin skills by many employers
- Free
- People generally like the language

## Python 2 v 3

- 2 has been around forever
    - Preinstalled on Lnux and Apple
- Hard fixes bundled together into Python 3
    - Python 3 is the future

## Running Python

- Built-in *interactive interpreter* (*shell*) is the easy way to experiment with small programs
    - Type line by line and see results immediately
    - Experiment faster
- Store as text files with `.py` extension and run from terminal by typing `python *filename*`

## Using the Interactive Interpreter

- Type `python` or `ipython` from terminal
- Works almost the same as Python works on files
    - One exception: when you type something that has a value, the interactive interpreter prints the value automatically

*Integrated development envireonments* IDEs GUIs with advance text editing and help. Go over in Chapter 12

`import this`

    The Zen of Python, by Tim Peters

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
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!

---

# Appendix D: Install Python 3

- Find out version
- Install Python 3
- Install Anaconda
- Install `pip` and `virtualenv`
- Install `conda` as an alternative to `pip`

---

# 2. Py Ingredients: Numbers, Strings, and Variables

- Look at built-in data types
    - *booleans* `True` or `False`
    - *integers* whole numbers
    - *floats* numbers with dicimal or exponenets
    - *strings* sequences of text characters

## Variables, Names, and Objects

- In python, *evertyhing* -- booleans, integers, floats, strings, even large data structures, functions, and programs -- are implemented as an *object*. 
- Object is like a clear plastic box containing a piece of data
    - Object has a *type* (boolean, integer) that determies what can be done with it
    - *Type* determines if the *value* can be changed (*mutable*) or is constant (*immutable*)
- Python *strongly typed* which means that the type of an object does not change, even if the value is mutable
- Can define *variables*
    - Names that refer to values in teh computer's memory that you can define or use in your program
    - use `=` to *assign* a value to a variable
    - *variables are just names* assignment **does not copy** a value it just **attaches a name** to the object that contains the date
        - The neme is a *reference* to a thing rather than the thing itself


- A *class* is the definition of an object. In python "class" and "type" mean pretty much the same thing
- Variable names can only contain
    - lowercase (a-z)
    - uppercase (A-Z)
    - Digits (0-9)
    - `_`
    - Cannot begin with a digit
    - Variables with underscore are treated in a special way
    - Do not use *reserved words* in variable names:
        - False, class, finally, i, return, None, continue, for, lambda, try, True, def, from, nonlocal, while, and, del, global, not, with, as, elif, if, or, yield, break, except, in, raise

## Numbers

- Built-in support for *integers* and *floating point* numbers
- Can calculate combinations of numbers with math *operators*
    - `+` addition
    - `-` subtraction
    - `*` multiplaication
    - `/` floating point division
    - `//` integer division
    - `%` modulus (remainder)
    - `**` exponentiation

- Style note: not required to have spaves `5+9` but inclusion increases readaility `5 + 9`

- Can reassign variables with mathematical operators
    a = 95
    a -= 3
a becomes 92
    a +=8
Becomes 100
    a *=2
Becomes 200
    a /= 3
Becomes 66.66666667
    a = 13
    a //= 4
Becomes 3

To get both quotient and remainder
    divmod(9,5)
    returns (1,4)
    9 // 5 #1
    9 % 5 #4
`divmod()` is a *function* that returns a *tuple*

## Precedence

    2 + 3 * 4 #14

Uses orders of operation, higher *precendnce* for multiplication

Always best to explicitly use parentheses

    2 + (3 * 4)

This way, anyone reading code doesn't have to guess precedence or lookup rules

## Bases

- Integers are assumed to be decimal (base 10) unles a prefix is used to specify another *base*
- Base is how many digits you can use until you need to "carry the one"
    - Base 2 (`binary`) only digits are 0 and 1. 1 + 1 = 10
    - `0b` or `0B` for *binary* base 2
    - `0o` or `0)` for *octal* base 8
    - `0x` or `0X` for *hex* base 16

## Type conversions

- To change other python types into an integer, use the `int()` function
    - Keeps the whole number and discards any fractional art
    - `int(True)` 1
    - `int(False)` 0
    - `int(98.6)` 98
    - `int(1.0e4)` 1000
    - `int('99')` 99
    - `int(1234)` 1234

- If you mix numeric types, Python will somtimes automatically convert them for you
    4 + 7.0 #11.0
    True + 2 #3
    False + 5.0 #5.0

## How big is an int?

Python 2:

- `int` limited to 32 bits
    - Store -2,147,483,648 to 2,147,483,647
- `long` has 64 bits

Python 3 `int` can be *any size* and there isn't a `long` anymore

## Floats

- *Floating-point* numbers have decimal points
    - `float(True)` #1.0
    - `float(False)` #0.0
    - `float(98)` 98.0
    - `float('99')` 99.0
    - `float('98.6')` 98.6
    - `float('-1.5')` -1.5
    - `float('1.0e4')` 10000.0

## Math Functions

Square roots, cosines, etc. Appendix C

## Strings

- Supports Unicode standard
    - Can contain characters from any written language in the world
    - Plus a lot of symbols
- Strings are an example of a python *sequence*
- Strings are *immutable*
    - Can't change a string in omace, but you can copy parts of stings to other strings to get the same effect

## Create with Quotes

- Make strings by enclosing characrers in either single or double quotes
- Why have both?
    - So you can create strings containing quote characters
    - Single quote in double quote or other way around

    >>> "'Nay,' said the naysayer."
    "'Nay,' said the naysayer."
    >>> 'The rare double quote in captivity: ".'
    'The rare double quote in captivity: ".'
    >>> 'A "two by four" is actually 1 1⁄2" × 3 1⁄2".'
    'A "two by four is" actually 1 1⁄2" × 3 1⁄2".'
    >>> "'There's the man that shot my paw!' cried the limping hound."
    "'There's the man that shot my paw!' cried the limping hound."

You can also use three single quotes (''') or three double quotes ("""):
    >>> '''Boom!'''
    'Boom'

Triple quotes aren’t very useful for short strings like these. Their most common use is to create *multiline strings*, like this classic poem from Edward Lear:

    >>> poem = '''There was a Young Lady of Norway,
    ... Who casually sat in a doorway;
    ... When the door squeezed her flat,
    ... She exclaimed, "What of that?"
    ... This courageous Young Lady of Norway.'''
    >>>

### Convert data types by using str()

- You can convert other Python data types to strings by using the `str() `function:

    >>> str(98.6)
    '98.6'
    >>> str(1.0e4)
    '10000.0'
    >>> str(True)
    'True'

- Python uses the `str()` function internally when you call `print()` with objects that are not strings and when doing *string interpolation*

## Escape with \

- Python lets you *escape* the meaning of some characters within strings to achieve effects that would otherwise be hard to express. 
- By preceding a character with a backslash `(\)`, you give it a special meaning
- The most common escape sequence is `\n` which means to begin a new line.

    >>> palindrome = 'A man,\nA plan,\nA canal:\nPanama.'
    >>> print(palindrome)
    A man,
    A plan,
    A canal:
    Panama.

- You will see the escape sequence `\t `(tab) used to align text:

    >>> print('a\tbc')
    a bc

- You might also need `\'` or `\" `to specify a literal single or double quote inside a string that’s quoted by the same character:

    >>> testimony = "\"I did nothing!\" he said. \"Not that either! Or the other
    thing.\""
    >>> print(testimony)
    "I did nothing!" he said. "Not that either! Or the other thing."
    >>> fact = "The world's largest rubber duck was 54'2\" by 65'7\" by 105'"
    >>> print(fact)
    The world's largest rubber duck was 54'2" by 65'7" by 105'

- And if you need a literal backslash, just type two of them:

    >>> speech = 'Today we honor our friend, the backslash: \\.'
    >>> print(speech)
    Today we honor our friend, the backslash: \.

## Combine with +

- You can combine literal strings or string variables in Python by using the + operator, 

    >>> 'Release the kraken! ' + 'No, wait!'
    'Release the kraken! No, wait!'

## Duplicate with *

- You use the * operator to duplicate a string. Tr

    >>> start = 'Na ' * 4 + '\n'
    >>> middle = 'Hey ' * 3 + '\n'
    >>> end = 'Goodbye.'
    >>> print(start + start + middle + end)

## Extract a character with []

- To get a single character from a string, specify its offset inside square brackets after the string’s name. The first (leftmost) offset is 0, the next is 1, and so on. The last (rightmost) offset can be specified with –1 so you don’t have to count; going to the left
are –2, –3, and so on.

    >>> letters = 'abcdefghijklmnopqrstuvwxyz'
    >>> letters[0]
    'a'
    >>> letters[1]
    'b'
    >>> letters[-1]
    'z'
    >>> letters[-2]
    'y'
    >>> letters[25]
    'z'
    >>> letters[5]
    'f'

- If you specify an offset that is the length of the string or longer, you'll get an exception

- Because strings are immutable, you can’t insert a character directly into one or change the character at a specific index.
- Let’s try to change 'Henny' to 'Penny' and see what
happens:

    >>> name = 'Henny'
    >>> name[0] = 'P'
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    TypeError: 'str' object does not support item assignment

Instead you need to use some combination of string functions such as `replace()` or a slice (which you’ll see in a moment):

    >>> name = 'Henny'
    >>> name.replace('H', 'P')
    'Penny'
    >>> 'P' + name[1:]
    'Penny'

## SLICE WITH [*start: end: step*]

- Can extract a *substring* using a *slice*
- Define using square brackets `start` offset, `end` offset, and an optional `step` size
    - `[:]` Extracts entire sequence start to end
    - `[*start*:]` Specifies start and goes to end
    - `[:*end*]` beginning to end offset -1
    - `[start:end:step]` extracts from start to end skipping characters

## Get length with `len()`

- `len()` funtion counts characters in a string

## Split with `split()`

- To use a string function, type the name of the string, a dot, the name of the function and any *arguments* that hte function needs: 

    `*string.function(arguments)*`

- `split()` breaks a string into a list of smaller strings

    >>> todos = 'get gloves,get mask,give cat vitamins,call ambulance'
    >>> todos.split(',')
    ['get gloves', 'get mask', 'give cat vitamins', 'call ambulance']

- You still need the parentheses when calling split with no arguments—that’s howPython knows you’re calling a function.

## Combine with `join()`

- `join()` function is the opposite of `split()`
- Collapses a list of strings into a single string. 
- It looks a bit backward because you specify the string that glues everything together first, and then the list of strings to glue: 
    - `string .join( list )`

    >>> crypto_list = ['Yeti', 'Bigfoot', 'Loch Ness Monster']
    >>> crypto_string = ', '.join(crypto_list)
    >>> print('Found and signing book deals:', crypto_string)
    Found and signing book deals: Yeti, Bigfoot, Loch Ness Monster

## Playing with strings

    >>> setup = 'a duck goes into a bar...'

    Remove . sequences from both ends:
    >>> setup.strip('.')
    'a duck goes into a bar'

    Capitalize the first word:
    >>> setup.capitalize()
    'A duck goes into a bar...'

    Capitalize all the words:
    >>> setup.title()
    'A Duck Goes Into A Bar...'

    Convert all characters to uppercase:
    >>> setup.upper()
    'A DUCK GOES INTO A BAR...'

    Convert all characters to lowercase:
    >>> setup.lower()
    'a duck goes into a bar...'

    Swap upper- and lowercase:
    >>> setup.swapcase()
    'A DUCK GOES INTO A BAR...'

## Substitute with `replace()`

- Use `replace()` for simple substring substitutions

    >>> setup.replace('duck', 'marmoset')
    'a marmoset goes into a bar...'

---
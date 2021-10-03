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

- Triple quotes aren’t very useful for short strings like these. Their most common use is to create *multiline strings*, like this classic poem from Edward Lear:

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

- To get a single character from a string, specify its offset inside square brackets after the string’s name. The first (leftmost) offset is 0, the next is 1, and so on. The last (rightmost) offset can be specified with –1 so you don’t have to count; going to the left are –2, –3, and so on. 

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
- Let’s try to change 'Henny' to 'Penny' and see what happens:

    >>> name = 'Henny'
    >>> name[0] = 'P'
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    TypeError: 'str' object does not support item assignment

- Instead you need to use some combination of string functions such as `replace()` or a slice (which you’ll see in a moment):

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

- Examples

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

# 3. Py Filling: Lists, Tuples, Dictionaries, and Sets

## Lists and Tuples

- Most languages can represent a sequence if items indexed by their integer position
- String is a list of characters
- *Tuples* and *lists* 
    - Contain zero or more elements
    - Unlike strings, elements can be of different types
    - In fact, each element can be *any* phtyon element
    - *tuples* are *immutable*
        - when assigned baked in and cannot change
    - *lists* are *mutable*
        - Can insert and delete elements
    
> Guido van Rossum, the creator of Python, tweeted “I pronounce tuple too-pull on Mon/Wed/Fri and tub-pull on Tue/Thu/Sat. On Sunday I don’t talk about them. :)”

## Lists

- Keeping track of things by their order
    - Especially when order and content might change

## Create with `[]` or `list()`

- A list is made from zero or more elements, separated by commas, and surrounded by square brackets:

    >>> empty_list = [ ]
    >>> weekdays = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']
    >>> big_birds = ['emu', 'ostrich', 'cassowary']
    >>> first_names = ['Graham', 'John', 'Terry', 'Terry', 'Michael']

- You can also make an empty list with the list() function:

    >>> another_empty_list = list()
    >>> another_empty_list
    []

- The weekdays list is the only one that actually takes advantage of list order. 
- The `first_names` list shows that values do not need to be unique.
- If you only want to keep track of unique values and don’t care
about order, a Python *set* might be a better choice than a list. 
    - `big_birds` could have been a set. 
    
## Conbert other data types to lists with `list()`

- Python’s `list()` function converts other data types to lists. 
- The following example converts a string to a list of one-character strings:

    >>> list('cat')
    ['c', 'a', 't']

- This example converts a tuple (coming up after lists in this chapter) to a list:

    >>> a_tuple = ('ready', 'fire', 'aim')
    >>> list(a_tuple)
    ['ready', 'fire', 'aim']

## Get an Item by Using `[*offset*']`

- As with strings, you can extract a single value from a list by specifying its offset:

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> marxes[0]
    'Groucho'
    >>> marxes[1]
    'Chico'
    >>> marxes[2]
    'Harpo'

- Again, as with strings, negative indexes count backward from the end:

    >>> marxes[-1]
    'Harpo'
    >>> marxes[-2]
    'Chico'
    >>> marxes[-3]
    'Groucho'

## Lists of lists

- Lists can contain elements of different types, including other lists, as illustrated here:

    >>> small_birds = ['hummingbird', 'finch']
    >>> extinct_birds = ['dodo', 'passenger pigeon', 'Norwegian Blue']
    >>> carol_birds = [3, 'French hens', 2, 'turtledoves']
    >>> all_birds = [small_birds, extinct_birds, 'macaw', carol_birds]

- So what does all_birds, a list of lists, look like?

    >>> all_birds
    [['hummingbird', 'finch'], ['dodo', 'passenger pigeon', 'Norwegian Blue'], 'macaw',
    [3, 'French hens', 2, 'turtledoves']]

- Let’s look at the first item in it:

    >>> all_birds[0]
    ['hummingbird', 'finch']

- If we want the first item of extinct_birds, we can extract it from all_birds by specifying two indexes:

    >>> all_birds[1][0]
    'dodo'

- The [1] refers to the list that’s the second item in all_birds, whereas the [0] refers to the first item in that inner list.

## Change an item by `[*offset*]`

- Just as you can get the value of a list item by its offset, you can change it:

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> marxes[2] = 'Wanda'
    >>> marxes
    ['Groucho', 'Chico', 'Wanda']

- Again, the list offset needs to be a valid one for this list.
You can’t change a character in a string in this way, because strings are immutable.
- Lists are mutable. You can change how many items a list contains, and the items themselves.

## Get a slice to extract items by offset range

- You can extract a subsequence of a list by using a slice:

    >>> marxes = ['Groucho', 'Chico,' 'Harpo']
    >>> marxes[0:2]
    ['Groucho', 'Chico']

- A slice of a list is also a list.

- As with strings, slices can step by values other than one. The next example starts at the beginning and goes right by 2:

    >>> marxes[::2]
    ['Groucho', 'Harpo']

- Here, we start at the end and go left by 2:

    >>> marxes[::-2]
    ['Harpo', 'Groucho']

- And finally, the trick to reverse a list:

    >>> marxes[::-1]
    ['Harpo', 'Chico', 'Groucho']


## Add an item to the end with `append()`

- The traditional way of adding items to a list is to append() them one by one to the end. In the previous examples, we forgot Zeppo, but  hat’s all right because the list is
mutable, so we can add him now:

    >>> marxes.append('Zeppo')
    >>> marxes
    ['Groucho', 'Chico', 'Harpo', 'Zeppo']

## Combine lists bu using `extend()` or `+=`

- You can merge one list into another by using `extend()`. Suppose that a well-meaning person gave us a new list of Marxes called others, and we’d like to merge them into the main marxes list:

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> others = ['Gummo', 'Karl']
    >>> marxes.extend(others)
    >>> marxes
    ['Groucho', 'Chico', 'Harpo', 'Zeppo', 'Gummo', 'Karl']

- Alternatively, you can use +=:

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> others = ['Gummo', 'Karl']
    >>> marxes += others
    >>> marxes
    ['Groucho', 'Chico', 'Harpo', 'Zeppo', 'Gummo', 'Karl']

- If we had used `append()`, others would have been added as a single list item rather than merging its items:

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> others = ['Gummo', 'Karl']
    >>> marxes.append(others)
    >>> marxes
    ['Groucho', 'Chico', 'Harpo', 'Zeppo', ['Gummo', 'Karl']]

## Add an item by offset with `insert()`

- The `append()` function adds items only to the end of the list.
- To add an item before any offset, use `insert()`
    - Offset `0` inserts at the beginning
    - If offset is beyond end of list, adds to end

## Delete an item by Offset with `del[]`

- Deletes item by position
- `del list[*offset*]`

## Delete an Item by Value with `remove()`

- Removes match to item passed

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Gummo', 'Zeppo']
    >>> marxes.remove('Gummo')
    >>> marxes
    ['Groucho', 'Chico', 'Harpo', 'Zeppo']

## Get an item by offset and delete it using `pop()`

- `pop()` or `pop(-1)` removes and returns last item
- `pop(0)` fives the start of the list

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> marxes.pop()
    'Zeppo'
    >>> marxes
    ['Groucho', 'Chico', 'Harpo']
    >>> marxes.pop(1)
    'Chico'
    >>> marxes
    ['Groucho', 'Harpo']

## Find an item's offset value with `index()`

- If you want to know the offset of an item in a list by its value, use `index()`:

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> marxes.index('Chico')
    1

## Test for a value within

- The Pythonic way to check for the existence of a value in a list is using in:

    >>> marxes = ['Groucho', 'Chico', 'Harpo', 'Zeppo']
    >>> 'Groucho' in marxes
    True
    >>> 'Bob' in marxes
    False

- The same value may be in more than one position in the list. As long as it’s in there at
least once, in will return True:

    >>> words = ['a', 'deer', 'a' 'female', 'deer']
    >>> 'deer' in words
    True

## Count Occurences of a value using `count()`

- To count how many times a particular value occurs in a list, use `count()`:

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> marxes.count('Harpo')
    1
    >>> marxes.count('Bob')
    0
    >>> snl_skit = ['cheeseburger', 'cheeseburger', 'cheeseburger']
    >>> snl_skit.count('cheeseburger')
    3


## Convert to a String with join()

- `join()` Example:

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> ', '.join(marxes)
    'Groucho, Chico, Harpo'

- The argument to `join()` is a string or any iterable sequence of strings (including a list), and its output is a string.
- If join() were just a list method, you couldn’t use it with other iterable objects such as tuples or strings.

## Reorder items with `sort()`

- Sorts by values rather than offsets
- The list function `sort()` sorts the list itself, *in place*.
- The general function `sorted()` returns a sorted *copy* of the list.
- Numbers sorted ascending by default
- Strings sorted alphabetically

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> sorted_marxes = sorted(marxes)
    >>> sorted_marxes
    ['Chico', 'Groucho', 'Harpo']

- `sorted_marxes` is a copy, and creating it did not change the original list:

    >>> marxes
    ['Groucho', 'Chico', 'Harpo']

- But, calling the list function `sort()` on the marxes list does change marxes:

    >>> marxes.sort()
    >>> marxes
    ['Chico', 'Groucho', 'Harpo']

- If the elements of your list are all of the same type (such as strings in marxes), `sort()`
will work correctly. 
- You can sometimes even mix types—for example, integers and floats—because they are automatically converted to one another by Python in expressions:

    >>> numbers = [2, 1, 4.0, 3]
    >>> numbers.sort()
    >>> numbers
    [1, 2, 3, 4.0]

- The default sort order is ascending, but you can add the argument `reverse=True` to set it to descending:

    >>> numbers = [2, 1, 4.0, 3]
    >>> numbers.sort(reverse=True)
    >>> numbers
    [4.0, 3, 2, 1]

## Get length with `len()`

- `len()` returns the number of items in a list:

    >>> marxes = ['Groucho', 'Chico', 'Harpo']
    >>> len(marxes)
    3

## Assign with `=` | Copy with `copy()`

 - Example

    >>> a = [1, 2, 3]
    >>> a
    [1, 2, 3]
    >>> b = a
    >>> b
    [1, 2, 3]
    >>> a[0] = 'surprise'
    >>> a
    ['surprise', 2, 3]

- Remember the sticky note analogy in Chapter 2? `b` just refers to the same list object as `a`; therefore, whether we change the list contents by using the name `a` or `b`, it’s reflected in both:

    >>> b
    ['surprise', 2, 3]
    >>> b[0] = 'I hate surprises'
    >>> b
    ['I hate surprises', 2, 3]
    >>> a
    ['I hate surprises', 2, 3]

- You can copy the values of a list to an independent, fresh list by using any of these methods:
    - The list `copy()` function
    - The `list()` conversion function
    - The list slice [:]

- Our original list will be `a` again. 
    - We’ll make `b` with the list `copy()` function
    - `c` with the `list()` conversion function
    - `d` with a list slice:

        >>> a = [1, 2, 3]
        >>> b = a.copy()
        >>> c = list(a)
        >>> d = a[:]
- Again, `b`, `c`, and `d` are copies of `a`: 
    - they are new objects with their own values and no
connection to the original list object `[1, 2, 3]` to which `a` refers. 
- Changing `a` does *not* affect the copies `b`, `c`, and `d`:

    >>> a[0] = 'integer lists are boring'
    >>> a
    ['integer lists are boring', 2, 3]
    >>> b
    [1, 2, 3]
    >>> c
    [1, 2, 3]
    >>> d
    [1, 2, 3]

## Create a tuple by using `()`

- The syntax to make tuples is a little inconsistent, 
- Let’s begin by making an empty tuple using `()`:

    >>> empty_tuple = ()
    >>> empty_tuple
    ()

- To make a tuple with one or more elements, follow each element with a comma. This works for one-element tuples:

    >>> one_marx = 'Groucho',
    >>> one_marx
    ('Groucho',)

- If you have more than one element, follow all but the last one with a comma:

    >>> marx_tuple = 'Groucho', 'Chico', 'Harpo'
    >>> marx_tuple
    ('Groucho', 'Chico', 'Harpo')

- Python includes parentheses when echoing a tuple. You don’t need them—it’s the trailing commas that really define a tuple—but using parentheses doesn’t hurt. 
- You can use them to enclose the values, which helps to make the tuple more visible:

    >>> marx_tuple = ('Groucho', 'Chico', 'Harpo')
    >>> marx_tuple
    ('Groucho', 'Chico', 'Harpo')

- Tuples let you assign multiple variables at once:

    >>> marx_tuple = ('Groucho', 'Chico', 'Harpo')
    >>> a, b, c = marx_tuple
    >>> a
    'Groucho'
    >>> b
    'Chico'
    >>> c
    'Harpo'

- This is sometimes called tuple unpacking.

- You can use tuples to exchange values in one statement without using a temporary variable:

    >>> password = 'swordfish'
    >>> icecream = 'tuttifrutti'
    >>> password, icecream = icecream, password
    >>> password
    'tuttifrutti'
    >>> icecream
    'swordfish'
    >>>

- The `tuple()` conversion function makes tuples from other things:

    >>> marx_list = ['Groucho', 'Chico', 'Harpo']
    >>> tuple(marx_list)
    ('Groucho', 'Chico', 'Harpo')

## Tuples vs. Lists

- You can often use tuples in place of lists, but they have many fewer functions
- There is no `append()`, `insert()`, and so on—because they can’t be modified after creation.
- Why not just use lists instead of tuples everywhere?
    - Tuples use less space.
    - You can’t clobber tuple items by mistake.
    - You can use tuples as dictionary keys (see the next section).
    - Named tuples can be a simple alternative to objects.
    - Function arguments are passed as tuples 
- In everyday programming, you’ll use lists and dictionaries more.

## Dictionaries

- *Dictionary* is similar to a list, but:
    - Order dosen't matter
    - Aren't selected by offser
    - Uses a unique *key* for each value
        - Often a string, but can be any immutable type (boolean, int float, tuple, string)
    - Mutable
        - Add
        - Delete
        - Change key-value elements

## Create with `{}`

- Curly brackets around comma-separated `key : value` pairs

    >>> empty_dict = {}
    >>> empty_dict
    {}

- Let’s make a small dictionary with quotes from Ambrose Bierce’s *The Devil’s Dictionary*:

    >>> bierce = {
    ... "day": "A period of twenty-four hours, mostly misspent",
    ... "positive": "Mistaken at the top of one's voice",
    ... "misfortune": "The kind of fortune that never misses",
    ... }
    >>>

- Typing the dictionary’s name in the interactive interpreter will print its keys and values:

    >>> bierce
    {'misfortune': 'The kind of fortune that never misses',
    'positive': "Mistaken at the top of one's voice",
    'day': 'A period of twenty-four hours, mostly misspent'}

- In Python, it’s okay to leave a comma after the last item of a list, tuple, or dictionary. 
- You don’t need to indent, when you’re typing keys and values within the curly braces. It just helps readability.

## Convert by using `dict()`

- You can use the `dict()` function to convert two-value sequences into a dictionary.
    - You might run into such key-value sequences at times
        -  “Strontium, 90, Carbon, 14”
        - “Vikings, 20, Packers, 7”.
- The first item in each sequence is used as the key and the second as the value.

- First, here’s a small example using lol (a list of two-item lists):

    >>> lol = [ ['a', 'b'], ['c', 'd'], ['e', 'f'] ]
    >>> dict(lol)
    {'c': 'd', 'a': 'b', 'e': 'f'}

## Add or Change an Item by `[ *key* ]`

- Adding an item to a dictionary is easy. Just refer to the item by its key and assign a value. 
    - If the key was already present in the dictionary, the existing value is replaced by the new one.
    - If the key is new, it’s added to the dictionary with its value. 
    - Unlike lists, you don’t need to worry about Python throwing an exception during assignment by specifying an index that’s out of range.

- Let’s make a dictionary of most of the members of Monty Python, using their last names as keys, and first names as values:

    >>> pythons = {
    ... 'Chapman': 'Graham',
    ... 'Cleese': 'John',
    ... 'Idle': 'Eric',
    ... 'Jones': 'Terry',
    ... 'Palin': 'Michael',
    ... }
    >>> pythons
    {'Cleese': 'John', 'Jones': 'Terry', 'Palin': 'Michael',
    'Chapman': 'Graham', 'Idle': 'Eric'}

- We’re missing one member: the one born in America, Terry Gilliam. Here’s an attempt by an anonymous programmer to add him, but he’s botched the first name:

    >>> pythons['Gilliam'] = 'Gerry'
    >>> pythons
    {'Cleese': 'John', 'Gilliam': 'Gerry', 'Palin': 'Michael',
    'Chapman': 'Graham', 'Idle': 'Eric', 'Jones': 'Terry'}

- And here’s some repair code by another programmer who is Pythonic in more than one way:

    >>> pythons['Gilliam'] = 'Terry'
    >>> pythons
    {'Cleese': 'John', 'Gilliam': 'Terry', 'Palin': 'Michael',
    'Chapman': 'Graham', 'Idle': 'Eric', 'Jones': 'Terry'}

- By using the same key ('Gilliam'), we replaced the original value 'Gerry' with 'Terry'.

- Remember that dictionary keys must be *unique*. 
- That’s why we used last names for keys instead of first names here—two members of Monty Python have the first name Terry! If you use a key more than once, the last value wins:

(p58 stop notes for now)

(p65 resume)

## Sets

- *Set* is like a dictionary with values thrown away, leaving only keys
    - Each key must be unique
    - Use set when you ony want to know that something exists and othing else about it
    - Dictionary if you want to attach some infrmation to a key as a value
- Unions of sets

## Create with set()

- To create a set, you use the `set()` function or enclose one or more comma-separated values in curly brackets, as shown here:

    >>> empty_set = set()
    >>> empty_set
    set()
    >>> even_numbers = {0, 2, 4, 6, 8}
    >>> even_numbers
    {0, 8, 2, 4, 6}
    >>> odd_numbers = {1, 3, 5, 7, 9}
    >>> odd_numbers
    {9, 3, 1, 5, 7}

- As with dictionary keys, sets are unordered.

- Because `[]` creates an empty list, you might expect `{} `to create an empty set. 
    - Instead, `{}` creates an empty dictionary. 
    - That’s also why the interpreter prints an empty set as `set() `instead of `{}`.
-  Why?
    - Dictionaries were in Python first and took possession of the curly brackets.

## Convert from other data types with `set()`

- You can create a set from a list, string, tuple, or dictionary, discarding any duplicate values.

- First, let’s take a look at a string with more than one occurrence of some letters:

    >>> set( 'letters' )
    {'l', 'e', 't', 'r', 's'}

- Now, let’s make a set from a list:

    >>> set( ['Dasher', 'Dancer', 'Prancer', 'Mason-Dixon'] )
    {'Dancer', 'Dasher', 'Prancer', 'Mason-Dixon'}

- This time, a set from a tuple:

    >>> set( ('Ummagumma', 'Echoes', 'Atom Heart Mother') )
    {'Ummagumma', 'Atom Heart Mother', 'Echoes'}

- When you give set() a dictionary, it uses only the keys:

    >>> set( {'apple': 'red', 'orange': 'orange', 'cherry': 'red'} )
    {'apple', 'cherry', 'orange'}

## Test for values by using `in`

- This is the most common use of a set. 
- We’ll make a dictionary called drinks. 
- Each key is the name of a mixed drink, and the corresponding value is a set of its ingredients:

    >>> drinks = {
    ... 'martini': {'vodka', 'vermouth'},
    ... 'black russian': {'vodka', 'kahlua'},
    ... 'white russian': {'cream', 'kahlua', 'vodka'},
    ... 'manhattan': {'rye', 'vermouth', 'bitters'},
    ... 'screwdriver': {'orange juice', 'vodka'}
    ... }

- Even though both are enclosed by curly braces ({ and }), a set is just a sequence of values, and a dictionary is one or more key : value pairs.

- Which drinks contain vodka? 

    >>> for name, contents in drinks.items():
    ... if 'vodka' in contents:
    ... print(name)
    ...
    screwdriver
    martini
    black russian
    white russian

- We want something with vodka but are lactose intolerant, and think vermouth tastes like kerosene:

    >>> for name, contents in drinks.items():
    ... if 'vodka' in contents and not ('vermouth' in contents or
    ... 'cream' in contents):
    ... print(name)
    ...
    screwdriver
    black russian

## Combinations and Operators

- hat if you want to check for combinations of set values? 
- Suppose that you want to find any drink that has orange juice or vermouth? 
    - We’ll use the set intersection operator, which is an ampersand (`&`):

    >>> for name, contents in drinks.items():
    ... if contents & {'vermouth', 'orange juice'}:
    ... print(name)
    ...
    screwdriver
    martini
    manhattan

- The result of the `&` operator is a set, which contains all the items that appear in both lists that you compare. 

- If neither of those ingredients were in contents, the `&` returns
an empty set, which is considered `False`.

- Now, let’s rewrite the example from the previous section, in which we wanted vodka but neither cream nor vermouth:

    >>> for name, contents in drinks.items():
    ... if 'vodka' in contents and not contents & {'vermouth', 'cream'}:
    ... print(name)
    ...
    screwdriver
    black russian

[skipping notes p66-70]

----

# 4. Crust: Code structures

- Now to structure *code* NOT JUST DATA
- Decided indentation was enough to define a program's structure

## Comment with `#`

- *Comment* is piece of text ignored by interpreter
- Clarify code
- Make notes to self
- You’ll usually see a comment on a line by itself, as shown here:

    >>> # 60 sec/min * 60 min/hr * 24 hr/day
    >>> seconds_per_day = 86400

- Or, on the same line as the code it’s commenting:

    >>> seconds_per_day = 86400 # 60 sec/min * 60 min/hr * 24 hr/day

- The `#` character has many names: hash, sharp, pound, or the sinister-sounding octothorpe.

- Whatever you call it, its effect lasts only to the end of the line on which it appears.
- Python does not have a multiline comment. You need to explicitly begin each comment line or section with a #.

    >>> # I can say anything here, even if Python doesn't like it,
    ... # because I'm protected by the awesome
    ... # octothorpe.
    ...
    >>>

However, if it’s in a text string, the all-powerful octothorpe reverts back to its role as a plain old # character:

    >>> print("No comment: quotes make the # harmless.")
    No comment: quotes make the # harmless.

## Continue Lines with \

- Programs are more readable when lines are reasonably short.
- The recommended (not required) maximum line length is 80 characters. 
- If you can’t say everything you want to say in that length, you can use the continuation character: \ (backslash). 
- Just put \ at the end of a line, and Python will suddenly act as though you’re still on the same line.

- For example, if I wanted to build a long string from smaller ones, I could do it in steps:

    >>> alphabet = ''
    >>> alphabet += 'abcdefg'
    >>> alphabet += 'hijklmnop'
    >>> alphabet += 'qrstuv'
    >>> alphabet += 'wxyz'

- Or, I could do it in one step, using the continuation character:

    >>> alphabet = 'abcdefg' + \
    ... 'hijklmnop' + \
    ... 'qrstuv' + \
    ... 'wxyz'

[Looking for intro to loops]

## Compare with if, elif, and else

## What Is True?

## Do Multiple Comparisons with in

## Repeat with while


- Testing with `if`, `elif`, and `else` runs from top to bottom. 
- Sometimes, we need to do something more than once. 
- We need a loop, and the simplest looping mechanism in Python is `while`.

    >>> count = 1
    >>> while count <= 5:
    ... print(count)
    ... count += 1
    ...
    1
    2
    3
    4
    5
    >>>

- We first assigned the value `1` to `count`. 
- The `while` loop compared the value of `count` to `5` and continued if count was less than or equal to `5`.
- Inside the loop, we printed the value of `count` and then incremented its value by one with the statement `count += 1`
- Python goes back to the top of the loop, and again compares `count` with `5`. The value of count is now `2`, so the contents of the while loop are again executed, and count is incremented to `3`.
- This continues until count is incremented from `5` to `6` at the bottom of the loop. 
- On the next trip to the top, count `<= 5` is now `False`, and the while loop ends. Python moves on to the next lines.

## Iterate with `for`

- Python makes frequent use of *iterators*, for good reason. 
- They make it possible for you to traverse data structures without knowing how large they are or how they are implemented. 
- You can even iterate over data that is created on the fly, allowing processing of data streams that would otherwise not fit in the computer’s memory all at once.

- It’s legal Python to step through a sequence like this:

    >>> rabbits = ['Flopsy', 'Mopsy', 'Cottontail', 'Peter']
    >>> current = 0
    >>> while current < len(rabbits):
    ... print(rabbits[current])
    ... current += 1
    ...
    Flopsy
    Mopsy
    Cottontail
    Peter

- But there’s a better, more Pythonic way:

    >>> for rabbit in rabbits:
    ... print(rabbit)
    ...
    Flopsy
    Mopsy
    Cottontail
    Peter
    80

- Lists such as rabbits are one of Python’s iterable objects, along with strings, tuples, dictionaries, sets, and some other elements. 
- Tuple or list iteration produces an item at a time. 
- String iteration produces a character at a time, as shown here:

    >>> word = 'cat'
    >>> for letter in word:
    ... print(letter)
    ...
    c
    a
    t


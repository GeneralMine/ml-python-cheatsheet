# Python-Cheatsheet
A simple cheatsheet for python and ml basics 

- [Python-Cheatsheet](#python-cheatsheet)
  - [The Philosophy of Python](#the-philosophy-of-python)
  - [Python Basics](#python-basics)
    - [Comments](#comments)
    - [Data Types](#data-types)
    - [Variables](#variables)
    - [Input/Output](#inputoutput)
    - [Math](#math)
    - [Boolean and Comparison Operators](#boolean-and-comparison-operators)
      - [Comparison Operators:](#comparison-operators)
      - [Boolean Operators:](#boolean-operators)
      - [Examples:](#examples)
    - [If, elif, else](#if-elif-else)
      - [if Statements](#if-statements)
      - [else Statements](#else-statements)
      - [elif Statements](#elif-statements)
      - [Example](#example)
    - [Loops: while and for](#loops-while-and-for)
      - [while Loop Statements](#while-loop-statements)
      - [break Statements](#break-statements)
      - [continue Statements](#continue-statements)
      - [for Loops and the range() Function](#for-loops-and-the-range-function)
      - [For else statement](#for-else-statement)
  - [Functions](#functions)
    - [Return Values and return Statements](#return-values-and-return-statements)
    - [The None Value](#the-none-value)
    - [Keyword Arguments and print()](#keyword-arguments-and-print)
    - [Local and Global Scope](#local-and-global-scope)
    - [The global Statement](#the-global-statement)
  - [Data Structures](#data-structures)
    - [Set](#set)
      - [Initializing a set](#initializing-a-set)
      - [sets: unordered collections of unique elements](#sets-unordered-collections-of-unique-elements)
      - [set add() and update()](#set-add-and-update)
      - [set remove() and discard()](#set-remove-and-discard)
      - [set union()](#set-union)
      - [set intersection](#set-intersection)
      - [set difference](#set-difference)
      - [set symetric_difference](#set-symetric_difference)
    - [Lists](#lists)
      - [Getting Individual Values in a List with Indexes](#getting-individual-values-in-a-list-with-indexes)
      - [Negative Indexes](#negative-indexes)
      - [Getting Sublists with Slices](#getting-sublists-with-slices)
      - [Getting a List’s Length with len()](#getting-a-lists-length-with-len)
      - [Changing Values in a List with Indexes](#changing-values-in-a-list-with-indexes)
      - [List Concatenation and List Replication](#list-concatenation-and-list-replication)
      - [Removing Values from Lists with del Statements](#removing-values-from-lists-with-del-statements)
      - [Using for Loops with Lists](#using-for-loops-with-lists)
      - [Looping Through Multiple Lists with zip()](#looping-through-multiple-lists-with-zip)
      - [The in and not in Operators](#the-in-and-not-in-operators)
      - [The Multiple Assignment Trick](#the-multiple-assignment-trick)
      - [Augmented Assignment Operators](#augmented-assignment-operators)
      - [Finding a Value in a List with the index() Method](#finding-a-value-in-a-list-with-the-index-method)
      - [Adding Values to Lists with the append() and insert() Methods](#adding-values-to-lists-with-the-append-and-insert-methods)
      - [Removing Values from Lists with remove()](#removing-values-from-lists-with-remove)
      - [Removing Values from Lists with pop()](#removing-values-from-lists-with-pop)
      - [Sorting the Values in a List with the sort() Method](#sorting-the-values-in-a-list-with-the-sort-method)
    - [Tuples](#tuples)
      - [Converting Types with the list() and tuple() Functions](#converting-types-with-the-list-and-tuple-functions)
    - [Dictionaries](#dictionaries)
      - [The keys(), values(), and items() Methods](#the-keys-values-and-items-methods)
      - [Checking Whether a Key or Value Exists in a Dictionary](#checking-whether-a-key-or-value-exists-in-a-dictionary)
      - [The get() Method](#the-get-method)
      - [The setdefault() Method](#the-setdefault-method)
      - [Pretty Printing](#pretty-printing)
      - [Merge two dictionaries](#merge-two-dictionaries)
  - [Google Colab](#google-colab)
    - [Editor](#editor)
    - [Kernel](#kernel)
    - [File upload and mount of Google Drive](#file-upload-and-mount-of-google-drive)
  - [Machine Learning](#machine-learning)
    - [pandas](#pandas)
      - [read csv](#read-csv)
    - [sklearn](#sklearn)
      - [Linear Regression](#linear-regression)


## The Philosophy of Python

`Beautiful is better than ugly.`  
`Explicit is better than implicit.`  
`Simple is better than complex.`  
`Complex is better than complicated.`  
`Flat is better than nested.`  
`Sparse is better than dense.`  
`Readability counts.`  
`Special cases aren't special enough to break the rules.`  
`Although practicality beats purity.`  
`Errors should never pass silently.`  
`Unless explicitly silenced.`  
`In the face of ambiguity, refuse the temptation to guess.`  
`There should be one-- and preferably only one --obvious way to do it.`  
`Although that way may not be obvious at first unless you're Dutch.`  
`Now is better than never.`  
`Although never is often better than *right* now.`  
`If the implementation is hard to explain, it's a bad idea.`  
`If the implementation is easy to explain, it may be a good idea.`  
`Namespaces are one honking great idea -- let's do more of those!`  

> The Zen of Python, by Tim Peters

## Python Basics

### Comments

Inline comment:

```python
# This is a comment
```

Multiline comment:

```Python
# This is a
# multiline comment
```

Code with a comment:

```python
a = 1  # initialization
```

Please note the two spaces in front of the comment.

Function docstring:

```python
def foo():
    """
    This is a function docstring
    You can also use:
    ''' Function Docstring '''
    """
```

### Data Types

| Data Type              | Examples                                  | Cast Method |
|:-----------------------|:------------------------------------------|:------------|
| Integers               | `-2, -1, 0, 1, 2, 3, 4, 5`                | `int()`     |
| Floating-point numbers | `-1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25` | `float()`   |
| Strings                | `'a', 'aa', 'I', 'love', '3 penguins!'`   | `str()`     |

String concatenation:

```python
>>> 'Alice' 'Bob'
'AliceBob'
```

Note: Avoid `+` operator for string concatenation. Prefer string formatting.

String Replication:

```python
>>> 'Alice' * 5
'AliceAliceAliceAliceAlice'
```

Evaluates to the integer value of the number of characters in a string:

```python
>>> len('hello')
5
```

Note: test of emptiness of strings, lists, dictionary, etc, should **not** use len, but prefer direct boolean evaluation.

```python
>>> a = [1, 2, 3]
>>> if a:
>>>     print("the list is not empty!")
```

### Variables

You can name a variable anything as long as it obeys the following rules:

1. It can be only one word.
1. It can use only letters, numbers, and the underscore (`_`) character.
1. It can’t begin with a number.
1. Variable name starting with an underscore (`_`) are considered as `unuseful` or `throwaway`.

Example:

```python
>>> message = 'Hello'
>>> message
'Hello'
```

```python
>>> _message = 'Hello'
```

`_message` should not be used again in the code.

### Input/Output

```python
>>> name = input()
>>> print('Nice to meet you ' + name + '!', 3)
Pingu
Nice to meet you Pingu! 3
```

### Math
| Operators | Operation         | Example         |
|-----------|-------------------|-----------------|
| +         | Addition          | `2 + 2 = 4`     |
| -         | Subtraction       | `5 - 2 = 3`     |
| \*        | Multiplication    | `3 * 3 = 9`     |
| /         | Division          | `22 / 8 = 2.75` |
| //        | Integer division  | `22 // 8 = 2`   |
| %         | Modulus/Remainder | `22 % 8 = 6`    |
| \*\*      | Exponent          | `2 ** 3 = 8`    |

Examples of expressions in the interactive shell:

```python
>>> 2 + 3 * 6
20
```

```python
>>> (2 + 3) * 6
30
```

```python
>>> 2 ** 8
256
```

```python
>>> 23 // 7
3
```

```python
>>> 23 % 7
2
```

```python
>>> (5 - 1) * ((7 + 1) / (3 - 1))
16.0
```

### Boolean and Comparison Operators
#### Comparison Operators:
| Operator | Meaning                  |
|----------|--------------------------|
| `==`     | Equal to                 |
| `is`     | Boolean Equal to         |
| `!=`     | Not equal to             |
| `is not` | Boolean Not Equal to     |
| `<`      | Less than                |
| `>`      | Greater Than             |
| `<=`     | Less than or Equal to    |
| `>=`     | Greater than or Equal to |

#### Boolean Operators:
| Operator | Meaning              |
|----------|----------------------|
| `not`    | Negation             |
| `is`     | Boolean Equal to     |
| `is not` | Boolean Not Equal to |
| `and`    | logical AND          |
| `or`     | logical OR           |

These operators evaluate to `True` or `False` depending on the values you give them.

#### Examples:

```python
>>> 42 == 42
True
```

```python
>>> 40 == 42
False
```

```python
>>> 'hello' == 'hello'
True
```

```python
>>> 'hello' == 'Hello'
False
```

```python
>>> 'dog' != 'cat'
True
```

```python
>>> 42 == 42.0
True
```

```python
>>> 42 == '42'
False
```

```python
>>> True is True
True
```

```python
>>> True is not False
True
```

```python
>>> (4 < 5) and (5 < 6)
True
```

```python
>>> (4 < 5) and (9 < 6)
False
```

```python
>>> (1 == 2) or (2 == 2)
True
```

You can also use multiple Boolean operators in an expression, along with the comparison operators:

```python
>>> 2 + 2 == 4 and not 2 + 2 == 5 and 2 * 2 == 2 + 2
True
```

These statements are equivalent:

```Python
>>> if a is True:
>>>    pass
>>> if a is not False:
>>>    pass
>>> if a:
>>>    pass
```

And these as well:

```Python
>>> if a is False:
>>>    pass
>>> if a is not True:
>>>    pass
>>> if not a:
>>>    pass
```

### If, elif, else

#### if Statements

```python
if name == 'Alice':
    print('Hi, Alice.')
```

#### else Statements

```python
name = 'Bob'
if name == 'Alice':
    print('Hi, Alice.')
else:
    print('Hello, stranger.')
```

#### elif Statements

```python
name = 'Bob'
age = 5
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
```
#### Example
```python
name = 'Bob'
age = 30
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
else:
    print('You are neither Alice nor a little kid.')
```

### Loops: while and for

#### while Loop Statements

```python
spam = 0
while spam < 5:
    print('Hello, world.')
    spam = spam + 1
```

#### break Statements

If the execution reaches a break statement, it immediately exits the while loop’s clause:

```python
while True:
    print('Please type your name.')
    name = input()
    if name == 'your name':
        break
print('Thank you!')
```

#### continue Statements

When the program execution reaches a continue statement, the program execution immediately jumps back to the start of the loop.

```python
while True:
    print('Who are you?')
    name = input()
    if name != 'Joe':
        continue
    print('Hello, Joe. What is the password? (It is a fish.)')
    password = input()
    if password == 'swordfish':
        break
print('Access granted.')
```

#### for Loops and the range() Function

```python
>>> print('My name is')
>>> for i in range(5):
>>>     print('Jimmy Five Times ({})'.format(str(i)))
My name is
Jimmy Five Times (0)
Jimmy Five Times (1)
Jimmy Five Times (2)
Jimmy Five Times (3)
Jimmy Five Times (4)
```

The _range()_ function can also be called with three arguments. The first two arguments will be the start and stop values, and the third will be the step argument. The step is the amount that the variable is increased by after each iteration.

```python
>>> for i in range(0, 10, 2):
>>>    print(i)
0
2
4
6
8
```

You can even use a negative number for the step argument to make the for loop count down instead of up.

```python
>>> for i in range(5, -1, -1):
>>>     print(i)
5
4
3
2
1
0
```

#### For else statement

This allows to specify a statement to execute in case of the full loop has been executed. Only useful when a `break` condition can occur in the loop:

```python
>>> for i in [1, 2, 3, 4, 5]:
>>>    if i == 3:
>>>        break
>>> else:
>>>    print("only executed when no item of the list is equal to 3")
```

## Functions
```python
>>> def hello(name):
>>>     print('Hello {}'.format(name))
>>>
>>> hello('Alice')
>>> hello('Bob')
Hello Alice
Hello Bob
```


### Return Values and return Statements

When creating a function using the def statement, you can specify what the return value should be with a return statement. A return statement consists of the following:

- The return keyword.

- The value or expression that the function should return.

```python
import random
def getAnswer(answerNumber):
    if answerNumber == 1:
        return 'It is certain'
    elif answerNumber == 2:
        return 'It is decidedly so'
    elif answerNumber == 3:
        return 'Yes'
    elif answerNumber == 4:
        return 'Reply hazy try again'
    elif answerNumber == 5:
        return 'Ask again later'
    elif answerNumber == 6:
        return 'Concentrate and ask again'
    elif answerNumber == 7:
        return 'My reply is no'
    elif answerNumber == 8:
        return 'Outlook not so good'
    elif answerNumber == 9:
        return 'Very doubtful'

r = random.randint(1, 9)
fortune = getAnswer(r)
print(fortune)
```


### The None Value

```python
>>> spam = print('Hello!')
Hello!
```

```python
>>> spam is None
True
```

Note: never compare to `None` with the `==` operator. Always use `is`.


### Keyword Arguments and print()

```python
>>> print('Hello', end='')
>>> print('World')
HelloWorld
```

```python
>>> print('cats', 'dogs', 'mice')
cats dogs mice
```

```python
>>> print('cats', 'dogs', 'mice', sep=',')
cats,dogs,mice
```


### Local and Global Scope

- Code in the global scope cannot use any local variables.

- However, a local scope can access global variables.

- Code in a function’s local scope cannot use variables in any other local scope.

- You can use the same name for different variables if they are in different scopes. That is, there can be a local variable named spam and a global variable also named spam.


### The global Statement

If you need to modify a global variable from within a function, use the global statement:

```python
>>> def spam():
>>>     global eggs
>>>     eggs = 'spam'
>>>
>>> eggs = 'global'
>>> spam()
>>> print(eggs)
spam
```

There are four rules to tell whether a variable is in a local scope or global scope:

1. If a variable is being used in the global scope (that is, outside of all functions), then it is always a global variable.

1. If there is a global statement for that variable in a function, it is a global variable.

1. Otherwise, if the variable is used in an assignment statement in the function, it is a local variable.

1. But if the variable is not used in an assignment statement, it is a global variable.


## Data Structures

### Set

From the Python 3 [documentation](https://docs.python.org/3/tutorial/datastructures.html)

> A set is an unordered collection with no duplicate elements. Basic uses include membership testing and eliminating duplicate entries. Set objects also support mathematical operations like union, intersection, difference, and symmetric difference.

#### Initializing a set

There are two ways to create sets: using curly braces `{}` and the built-in function `set()`

```python
>>> s = {1, 2, 3}
>>> s = set([1, 2, 3])
```

When creating an empty set, be sure to not use the curly braces `{}` or you will get an empty dictionary instead.

```python
>>> s = {}
>>> type(s)
<class 'dict'>
```

#### sets: unordered collections of unique elements

A set automatically remove all the duplicate values.

```python
>>> s = {1, 2, 3, 2, 3, 4}
>>> s
{1, 2, 3, 4}
```

And as an unordered data type, they can't be indexed.

```python
>>> s = {1, 2, 3}
>>> s[0]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'set' object does not support indexing
>>>
```

#### set add() and update()

Using the `add()` method we can add a single element to the set.

```python
>>> s = {1, 2, 3}
>>> s.add(4)
>>> s
{1, 2, 3, 4}
```

And with `update()`, multiple ones .

```python
>>> s = {1, 2, 3}
>>> s.update([2, 3, 4, 5, 6])
>>> s
{1, 2, 3, 4, 5, 6}  # remember, sets automatically remove duplicates
```

#### set remove() and discard()

Both methods will remove an element from the set, but `remove()` will raise a `key error` if the value doesn't exist.

```python
>>> s = {1, 2, 3}
>>> s.remove(3)
>>> s
{1, 2}
>>> s.remove(3)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 3
```

`discard()` won't raise any errors.

```python
>>> s = {1, 2, 3}
>>> s.discard(3)
>>> s
{1, 2}
>>> s.discard(3)
>>>
```

#### set union()

`union()` or `|` will create a new set that contains all the elements from the sets provided.

```python
>>> s1 = {1, 2, 3}
>>> s2 = {3, 4, 5}
>>> s1.union(s2)  # or 's1 | s2'
{1, 2, 3, 4, 5}
```

#### set intersection

`intersection` or `&` will return a set containing only the elements that are common to all of them.

```python
>>> s1 = {1, 2, 3}
>>> s2 = {2, 3, 4}
>>> s3 = {3, 4, 5}
>>> s1.intersection(s2, s3)  # or 's1 & s2 & s3'
{3}
```

#### set difference

`difference` or `-` will return only the elements that are unique to the first set (invoked set).

```python
>>> s1 = {1, 2, 3}
>>> s2 = {2, 3, 4}
>>> s1.difference(s2)  # or 's1 - s2'
{1}
>>> s2.difference(s1) # or 's2 - s1'
{4}
```

#### set symetric_difference

`symetric_difference` or `^` will return all the elements that are not common between them.

```python
>>> s1 = {1, 2, 3}
>>> s2 = {2, 3, 4}
>>> s1.symmetric_difference(s2)  # or 's1 ^ s2'
{1, 4}
```

### Lists

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam
['cat', 'bat', 'rat', 'elephant']
```

#### Getting Individual Values in a List with Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[0]
'cat'
```

```python
>>> spam[1]
'bat'
```

```python
>>> spam[2]
'rat'
```

```python
>>> spam[3]
'elephant'
```


#### Negative Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[-1]
'elephant'
```

```python
>>> spam[-3]
'bat'
```

```python
>>> 'The {} is afraid of the {}.'.format(spam[-1], spam[-3])
'The elephant is afraid of the bat.'
```


#### Getting Sublists with Slices

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[0:4]
['cat', 'bat', 'rat', 'elephant']
```

```python
>>> spam[1:3]
['bat', 'rat']
```

```python
>>> spam[0:-1]
['cat', 'bat', 'rat']
```

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[:2]
['cat', 'bat']
```

```python
>>> spam[1:]
['bat', 'rat', 'elephant']
```

Slicing the complete list will perform a copy:

```python
>>> spam2 = spam[:]
['cat', 'bat', 'rat', 'elephant']
>>> spam.append('dog')
>>> spam
['cat', 'bat', 'rat', 'elephant', 'dog']
>>> spam2
['cat', 'bat', 'rat', 'elephant']
```


#### Getting a List’s Length with len()

```python
>>> spam = ['cat', 'dog', 'moose']
>>> len(spam)
3
```


#### Changing Values in a List with Indexes

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam[1] = 'aardvark'

>>> spam
['cat', 'aardvark', 'rat', 'elephant']

>>> spam[2] = spam[1]

>>> spam
['cat', 'aardvark', 'aardvark', 'elephant']

>>> spam[-1] = 12345

>>> spam
['cat', 'aardvark', 'aardvark', 12345]
```


#### List Concatenation and List Replication

```python
>>> [1, 2, 3] + ['A', 'B', 'C']
[1, 2, 3, 'A', 'B', 'C']

>>> ['X', 'Y', 'Z'] * 3
['X', 'Y', 'Z', 'X', 'Y', 'Z', 'X', 'Y', 'Z']

>>> spam = [1, 2, 3]

>>> spam = spam + ['A', 'B', 'C']

>>> spam
[1, 2, 3, 'A', 'B', 'C']
```


#### Removing Values from Lists with del Statements

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> del spam[2]
>>> spam
['cat', 'bat', 'elephant']
```

```python
>>> del spam[2]
>>> spam
['cat', 'bat']
```


#### Using for Loops with Lists

```python
>>> supplies = ['pens', 'staplers', 'flame-throwers', 'binders']
>>> for i, supply in enumerate(supplies):
>>>     print('Index {} in supplies is: {}'.format(str(i), supply))
Index 0 in supplies is: pens
Index 1 in supplies is: staplers
Index 2 in supplies is: flame-throwers
Index 3 in supplies is: binders
```


#### Looping Through Multiple Lists with zip()

```python
>>> name = ['Pete', 'John', 'Elizabeth']
>>> age = [6, 23, 44]
>>> for n, a in zip(name, age):
>>>     print('{} is {} years old'.format(n, a))
Pete is 6 years old
John is 23 years old
Elizabeth is 44 years old
```

#### The in and not in Operators

```python
>>> 'howdy' in ['hello', 'hi', 'howdy', 'heyas']
True
```

```python
>>> spam = ['hello', 'hi', 'howdy', 'heyas']
>>> 'cat' in spam
False
```

```python
>>> 'howdy' not in spam
False
```

```python
>>> 'cat' not in spam
True
```


#### The Multiple Assignment Trick

The multiple assignment trick is a shortcut that lets you assign multiple variables with the values in a list in one line of code. So instead of doing this:

```python
>>> cat = ['fat', 'orange', 'loud']

>>> size = cat[0]

>>> color = cat[1]

>>> disposition = cat[2]
```

You could type this line of code:

```python
>>> cat = ['fat', 'orange', 'loud']

>>> size, color, disposition = cat
```

The multiple assignment trick can also be used to swap the values in two variables:

```python
>>> a, b = 'Alice', 'Bob'
>>> a, b = b, a
>>> print(a)
'Bob'
```

```python
>>> print(b)
'Alice'
```


#### Augmented Assignment Operators

| Operator    | Equivalent        |
|-------------|-------------------|
| `spam += 1` | `spam = spam + 1` |
| `spam -= 1` | `spam = spam - 1` |
| `spam *= 1` | `spam = spam * 1` |
| `spam /= 1` | `spam = spam / 1` |
| `spam %= 1` | `spam = spam % 1` |

Examples:

```python
>>> spam = 'Hello'
>>> spam += ' world!'
>>> spam
'Hello world!'

>>> bacon = ['Zophie']
>>> bacon *= 3
>>> bacon
['Zophie', 'Zophie', 'Zophie']
```


#### Finding a Value in a List with the index() Method

```python
>>> spam = ['Zophie', 'Pooka', 'Fat-tail', 'Pooka']

>>> spam.index('Pooka')
1
```


#### Adding Values to Lists with the append() and insert() Methods

**append()**:

```python
>>> spam = ['cat', 'dog', 'bat']

>>> spam.append('moose')

>>> spam
['cat', 'dog', 'bat', 'moose']
```

**insert()**:

```python
>>> spam = ['cat', 'dog', 'bat']

>>> spam.insert(1, 'chicken')

>>> spam
['cat', 'chicken', 'dog', 'bat']
```


#### Removing Values from Lists with remove()

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam.remove('bat')

>>> spam
['cat', 'rat', 'elephant']
```

If the value appears multiple times in the list, only the first instance of the value will be removed.


#### Removing Values from Lists with pop()

```python
>>> spam = ['cat', 'bat', 'rat', 'elephant']

>>> spam.pop()
'elephant'

>>> spam
['cat', 'bat', 'rat']

>>> spam.pop(0)
'cat'

>>> spam
['bat', 'rat']
```


#### Sorting the Values in a List with the sort() Method

```python
>>> spam = [2, 5, 3.14, 1, -7]
>>> spam.sort()
>>> spam
[-7, 1, 2, 3.14, 5]
```

```python
>>> spam = ['ants', 'cats', 'dogs', 'badgers', 'elephants']
>>> spam.sort()
>>> spam
['ants', 'badgers', 'cats', 'dogs', 'elephants']
```

You can also pass True for the reverse keyword argument to have sort() sort the values in reverse order:

```python
>>> spam.sort(reverse=True)
>>> spam
['elephants', 'dogs', 'cats', 'badgers', 'ants']
```

If you need to sort the values in regular alphabetical order, pass str. lower for the key keyword argument in the sort() method call:

```python
>>> spam = ['a', 'z', 'A', 'Z']
>>> spam.sort(key=str.lower)
>>> spam
['a', 'A', 'z', 'Z']
```

You can use the built-in function `sorted` to return a new list:

```python
>>> spam = ['ants', 'cats', 'dogs', 'badgers', 'elephants']
>>> sorted(spam)
['ants', 'badgers', 'cats', 'dogs', 'elephants']
```


### Tuples

```python
>>> eggs = ('hello', 42, 0.5)
>>> eggs[0]
'hello'
```

```python
>>> eggs[1:3]
(42, 0.5)
```

```python
>>> len(eggs)
3
```

The main way that tuples are different from lists is that tuples, like strings, are immutable.


#### Converting Types with the list() and tuple() Functions

```python
>>> tuple(['cat', 'dog', 5])
('cat', 'dog', 5)
```

```python
>>> list(('cat', 'dog', 5))
['cat', 'dog', 5]
```

```python
>>> list('hello')
['h', 'e', 'l', 'l', 'o']
```

### Dictionaries

Example Dictionary:

```python
myCat = {'size': 'fat', 'color': 'gray', 'disposition': 'loud'}
```


#### The keys(), values(), and items() Methods

values():

```python
>>> spam = {'color': 'red', 'age': 42}
>>> for v in spam.values():
>>>     print(v)
red
42
```

keys():

```python
>>> for k in spam.keys():
>>>     print(k)
color
age
```

items():

```python
>>> for i in spam.items():
>>>     print(i)
('color', 'red')
('age', 42)
```

Using the keys(), values(), and items() methods, a for loop can iterate over the keys, values, or key-value pairs in a dictionary, respectively.

```python

>>> spam = {'color': 'red', 'age': 42}
>>>
>>> for k, v in spam.items():
>>>     print('Key: {} Value: {}'.format(k, str(v)))
Key: age Value: 42
Key: color Value: red
```


#### Checking Whether a Key or Value Exists in a Dictionary

```python
>>> spam = {'name': 'Zophie', 'age': 7}
```

```python
>>> 'name' in spam.keys()
True
```

```python
>>> 'Zophie' in spam.values()
True
```

```python
>>> # You can omit the call to keys() when checking for a key
>>> 'color' in spam
False
```

```python
>>> 'color' not in spam
True
```


#### The get() Method

Get has two parameters: key and default value if the key did not exist

```python
>>> picnic_items = {'apples': 5, 'cups': 2}

>>> 'I am bringing {} cups.'.format(str(picnic_items.get('cups', 0)))
'I am bringing 2 cups.'
```

```python
>>> 'I am bringing {} eggs.'.format(str(picnic_items.get('eggs', 0)))
'I am bringing 0 eggs.'
```


#### The setdefault() Method

Let's consider this code:

```python
spam = {'name': 'Pooka', 'age': 5}

if 'color' not in spam:
    spam['color'] = 'black'
```

Using `setdefault` we could write the same code more succinctly:

```python
>>> spam = {'name': 'Pooka', 'age': 5}
>>> spam.setdefault('color', 'black')
'black'
```

```python
>>> spam
{'color': 'black', 'age': 5, 'name': 'Pooka'}
```

```python
>>> spam.setdefault('color', 'white')
'black'
```

```python
>>> spam
{'color': 'black', 'age': 5, 'name': 'Pooka'}
```


#### Pretty Printing

```python
>>> import pprint
>>>
>>> message = 'It was a bright cold day in April, and the clocks were striking
>>> thirteen.'
>>> count = {}
>>>
>>> for character in message:
>>>     count.setdefault(character, 0)
>>>     count[character] = count[character] + 1
>>>
>>> pprint.pprint(count)
{' ': 13,
 ',': 1,
 '.': 1,
 'A': 1,
 'I': 1,
 'a': 4,
 'b': 1,
 'c': 3,
 'd': 3,
 'e': 5,
 'g': 2,
 'h': 3,
 'i': 6,
 'k': 2,
 'l': 3,
 'n': 4,
 'o': 2,
 'p': 1,
 'r': 5,
 's': 3,
 't': 6,
 'w': 2,
 'y': 1}
```


#### Merge two dictionaries

```python
# in Python 3.5+:
>>> x = {'a': 1, 'b': 2}
>>> y = {'b': 3, 'c': 4}
>>> z = {**x, **y}
>>> z
{'c': 4, 'a': 1, 'b': 3}

# in Python 2.7
>>> z = dict(x, **y)
>>> z
{'c': 4, 'a': 1, 'b': 3}
```

## Google Colab

### Editor

### Kernel
### File upload and mount of Google Drive


## Machine Learning
### pandas
#### read csv

### sklearn

#### Linear Regression


# [ALL Base Python Modules](https://docs.python.org/3/py-modindex.html)

# 4 Python Arrays

# [list](https://www.w3schools.com/python/python_lists.asp)

- ordered
- changeable
- Allows duplicate members

list `thislist = ["apple", "banana", "cherry"]`

# [set](https://www.w3schools.com/python/python_sets.asp)

- unordered
- unindexed
- No duplicate members

set `thisset = {"apple", "banana", "cherry"}`

# [dictionary](https://docs.python.org/3/library/stdtypes.html#typesmapping) 

- unordered
- changeable
- indexed
- No duplicate members

`**name`

**dictionary `dictionary = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}`

**dictionary `thisdict = {"brand": "Ford", "model": "Mustang","year": 1964}`

# [tuple](https://docs.python.org/3/tutorial/datastructures.html#tut-tuples)

- ordered
- unchangeable
- Allows duplicate members

`*name`

*tuple: `t = 12345, 54321, 'hello!'`  

*tuple: `thistuple = ("apple", "banana", "cherry")`

*nested tuple: `u = ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))`

# [3. Basics](https://docs.python.org/3/tutorial/introduction.html)
## 3.1. Claculator
### 3.1.1. Numbers


```python
# this is the first comment
spam = 1  # and this is the second comment
          # ... and now a third!
text = "# This is not a comment because it's inside quotes."
```


```python
2 + 2
```




    4




```python
50 - 5*6
```




    20




```python
(50 - 5*6) / 4
```




    5.0




```python
8 / 5  # division always returns a floating point number
```




    1.6




```python
17 / 3  # classic division returns a float
```




    5.666666666666667




```python
17 // 3  # floor division discards the fractional part
```




    5




```python
17 % 3  # the % operator returns the remainder of the division
```




    2




```python
5 * 3 + 2  # result * divisor + remainder
```




    17




```python
5 ** 2  # 5 squared
```




    25




```python
2 ** 7  # 2 to the power of 7
```




    128




```python
width = 20
height = 5 * 9
width * height
```




    900




```python
4 * 3.75 - 1
```




    14.0




```python
#   _
# the last printed expression is assigned to the variable _
#round(number[, numberOFdigits])
round(_, 2)
```




    14.0




```python
dog = 35.4
dog = dog + _
print(dog)
```

    49.4


### 3.1.2. Strings
- immutable


```python
'spam eggs'  # single quotes
```




    'spam eggs'




```python
'doesn\'t'  # use \' to escape the single quote...
```




    "doesn't"




```python
"doesn't"  # ...or use double quotes instead
```




    "doesn't"




```python
'"Yes," they said.'
```




    '"Yes," they said.'




```python
"\"Yes,\" they said."
```




    '"Yes," they said.'




```python
'"Isn\'t," they said.'
```




    '"Isn\'t," they said.'




```python
'"Isn\'t," they said.'
```




    '"Isn\'t," they said.'




```python
print('"Isn\'t," they said.')
```

    "Isn't," they said.



```python
s = 'First line.\nSecond line.'  # \n means newline
s  # without print(), \n is included in the output
```




    'First line.\nSecond line.'




```python
print(s)  # with print(), \n produces a new line
```

    First line.
    Second line.



```python
print('C:\some\name')  # here \n means newline!
```

    C:\some
    ame



```python
print(r'C:\some\name')  # note the r before the quote
```

    C:\some\name

String literals can span multiple lines. One way is using triple-quotes: """...""" or '''...'''. End of lines are automatically included in the string, but it’s possible to prevent this by adding a \ at the end of the line. 

```python
print("""\
Usage: thingy [OPTIONS]
     -h                        Display this usage message
     -H hostname               Hostname to connect to
""")
```

    Usage: thingy [OPTIONS]
         -h                        Display this usage message
         -H hostname               Hostname to connect to
    



```python
# 3 times 'un', followed by 'ium'
3 * 'un' + 'ium'
```




    'unununium'




```python
'Py' 'thon'
```




    'Python'




```python
text = ('Put several strings within parentheses '
        'to have them joined together.')
text
```




    'Put several strings within parentheses to have them joined together.'


'''This only works with two literals though, not with variables or expressions:'''
prefix = 'Py'
prefix 'thon'  # can't concatenate a variable and a string literalFile "<stdin>", line 1
    prefix 'thon'
                ^
SyntaxError: invalid syntax
('un' * 3) 'ium'
  File "<stdin>", line 1
    ('un' * 3) 'ium'
                   ^
SyntaxError: invalid syntax

```python
# variable and a literal, use +
prefix = 'Py'
prefix + 'thon'
```




    'Python'




```python
'''INDEX string characters [0123]'''
word = 'Python'
word[0]  # character in position 0
```




    'P'




```python
word[5]  # character in position 5
```




    'n'




```python
word[-1]  # last character
```




    'n'




```python
word[-2]  # second-last character
```




    'o'




```python
word[-6]
```




    'P'




```python
word[0:2]  # characters from position 0 (included) to 2 (excluded)
```




    'Py'




```python
word[2:5]  # characters from position 2 (included) to 5 (excluded)
```




    'tho'




```python
word[:2] + word[2:]
```




    'Python'




```python
word[:4] + word[4:]
```




    'Python'




```python
word[:2]   # character from the beginning to position 2 (excluded)
```




    'Py'




```python
word[4:]   # characters from position 4 (included) to the end
```




    'on'




```python
word[-2:]  # characters from the second-last (included) to the end
```




    'on'


 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1>>> word[42]  # the word only has 6 characters
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range

```python
word[4:42]
```




    'on'




```python
word[42:]
```




    ''


>>> word[0] = 'J'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> word[2:] = 'py'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment

```python
'J' + word[1:]
```




    'Jython'




```python
word[:2] + 'py'
```




    'Pypy'




```python
s = 'supercalifragilisticexpialidocious'
len(s)
```




    34



### 3.1.3. Lists
- most versatile is the list, 
- which can be written as a list of comma-separated values (items) between square brackets. 
- Lists might contain items of different types
- mutable


```python
squares = [1, 4, 9, 16, 25]
squares
```




    [1, 4, 9, 16, 25]




```python
squares[0]  # indexing returns the item
```




    1




```python
squares[-1]
```




    25




```python
squares[-3:]  # slicing returns a new list
```




    [9, 16, 25]




```python
squares[:]
```




    [1, 4, 9, 16, 25]




```python
squares + [36, 49, 64, 81, 100] # concatenation
```




    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]




```python
'''RePlcae List value'''
cubes = [1, 8, "wrong"]  # something's wrong here
4 ** 3  # the cube of 4 is 64

cubes[2] = 64  # replace the wrong value
cubes
```




    [1, 8, 64]




```python
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
letters
```




    ['a', 'b', 'c', 'd', 'e', 'f', 'g']




```python
# replace some values
letters[2:5] = ['C', 'D', 'E']
letters
```




    ['a', 'b', 'C', 'D', 'E', 'f', 'g']




```python
# now remove them
letters[2:5] = []
letters
```




    ['a', 'b', 'f', 'g']




```python
# clear the list by replacing all the elements with an empty list
letters[:] = []
letters
```




    []




```python
letters = ['a', 'b', 'c', 'd']
len(letters)
```




    4




```python
''' Lost of Lists'''
a = ['a', 'b', 'c']
n = [1, 2, 3]
x = [a, n]
x
```




    [['a', 'b', 'c'], [1, 2, 3]]




```python
x[0]
```




    ['a', 'b', 'c']




```python
'''Picking element of list of lists'''
x[0][1]
```




    'b'




```python
'''[]++APPEND values'''
cubes2 = [1, 8, "wrong"]
cubes2.append(216)  # add the cube of 6
cubes2.append(7 ** 3)  # and the cube of 7
cubes2
```




    [1, 8, 'wrong', 216, 343]



## 3.2 `While` cycle


```python
# Fibonacci series:
# the sum of two elements defines the next
a, b = 0, 1
while a < 10:
    print(a)
    a, b = b, a+b
```

    0
    1
    1
    2
    3
    5
    8



```python
i = 256*256
print('The value of i is', i)
```

    The value of i is 65536

Comparison Operators: 
< (less than), 
> (greater than), 
== (equal to), 
<= (less than or equal to), 
>= (greater than or equal to) and 
!= (not equal to).

```python
a, b = 0, 1 #multiple assignment in 1 line
while a < 1000:
    print(a, end=',')
    a, b = b, a+b
```

    0,1,1,2,3,5,8,13,21,34,55,89,144,233,377,610,987,

# [4. Process Controll](https://docs.python.org/3/tutorial/controlflow.html)
`if for range break continue else pass def Lambda`
## 4.1 `if`


```python
x = int(input("Please enter an integer: "))

if x < 0:
    x = 0
    print('Negative changed to zero')
elif x == 0:
    print('Zero')
elif x == 1:
    print('Single')
else:
    print('More')
```

    Please enter an integer:  1


    Single


## 4.2 `for`


```python
# Measure some strings:
words = ['cat', 'window', 'defenestrate']
for w in words:
    print(w, len(w))
```

    cat 3
    window 6
    defenestrate 12



```python
for w in words[:]:  # Loop over a slice copy of the entire list.
    if len(w) > 6:
        words.insert(0, w)

words
```




    ['defenestrate', 'cat', 'window', 'defenestrate']



## 4.3 [`range()`](https://docs.python.org/3/library/stdtypes.html#range)


```python
for i in range(5):
    print(i)
```

    0
    1
    2
    3
    4



```python
#start at another number 
for i in range(5, 10):
    print(i)
```

    5
    6
    7
    8
    9



```python
#specify a different increment
for i in range(-10, -100, -30):
    print(i)
```

    -10
    -40
    -70



```python
# iterate over the indices of a sequence
a = ['Mary', 'had', 'a', 'little', 'lamb']
for i in range(len(a)):
    print(i, a[i])
```

    0 Mary
    1 had
    2 a
    3 little
    4 lamb



```python
print(range(10)) # wierd looking but normal
```

    range(0, 10)



```python
list(range(5)) #iterator, creates lists from iterables
```




    [0, 1, 2, 3, 4]



## 4.4. `break else continue`


```python
#BREAK
#breaks out of the innermost enclosing for or while loop.
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, '*', n//x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
```

    2 is a prime number
    3 is a prime number
    4 equals 2 * 2
    5 is a prime number
    6 equals 2 * 3
    7 is a prime number
    8 equals 2 * 4
    9 equals 3 * 3



```python
#CONTINUE
#continues with the next iteration of the loop
for num in range(2, 10):
    if num % 2 == 0:
        print("Found an even number", num)
        continue
    print("Found a number", num)
```

    Found an even number 2
    Found a number 3
    Found an even number 4
    Found a number 5
    Found an even number 6
    Found a number 7
    Found an even number 8
    Found a number 9


## 4.5. `pass`
- does nothing. 
- It can be used when a statement is required syntactically but the program requires no action.
- - Used is as a place-holder for a function or conditional body when you are working on new code, allowing you to keep thinking at a more abstract level.
while True:
    pass  # Busy-wait for keyboard interrupt (Ctrl+C)

#creating minimal classes
class MyEmptyClass:
    pass

def initlog(*args):
    pass   # Remember to implement this! The pass is silently ignored
## 4.6. `def` I.


```python
def fib(n):    # write Fibonacci series up to n
    """Print a Fibonacci series up to n."""
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    print()

# Now call the function we just defined:
fib(2000)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 



```python
fib # describe function
```




    <function __main__.fib(n)>




```python
f = fib #function inheritance
f(100)
```

    0 1 1 2 3 5 8 13 21 34 55 89 



```python
fib(0)
print(fib(0))
```

    
    
    None



```python
#RETURN
#returns with a value from a function
#
def fib2(n):  # return Fibonacci series up to n
    """Return a list containing the Fibonacci series up to n."""
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)    # see below
        a, b = b, a+b
    return result

f100 = fib2(100)    # call it
f100                # write the result
```




    [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]



## 4.7. `def` II.
### 4.7.1. `def` argument values


```python
def ask_ok(prompt, retries=4, reminder='Please try again!'):
    while True:
        ok = input(prompt)
        if ok in ('y', 'ye', 'yes'):
            return True
        if ok in ('n', 'no', 'nop', 'nope'):
            return False
        retries = retries - 1
        if retries < 0:
            raise ValueError('invalid user response')
        print(reminder)
```


```python
ask_ok('Do you really want to quit?')
```

    Do you really want to quit? 1


    Please try again!


    Do you really want to quit? y





    True




```python
 ask_ok('OK to overwrite the file?', 2) #auto response
```

    OK to overwrite the file? ok


    Please try again!


    OK to overwrite the file? 1


    Please try again!


    OK to overwrite the file? y





    True




```python
#Pre Defined Response at incorrect answer
ask_ok('OK to overwrite the file?', 2, 'Come on, only yes or no!') 
```

    OK to overwrite the file? y





    True




```python
#default values are evaluated at the point of function definition 
#in the defining scope
i = 5

def f(arg=i):
    print(arg)

i = 6
f()
```

    5



```python
def f(a, L=[]): #list can be modified continously
    L.append(a)
    return L

print(f(1))
print(f(2))
print(f(3))
```

    [1]
    [1, 2]
    [1, 2, 3]



```python
def f(a, L=None):
    if L is None:
        L = []
    L.append(a)
    return L
```

### 4.7.2. def parameters use II.


```python
#initalised Def
def parrot(voltage, state='a stiff', action='voom', type='Norwegian Blue'):
    print("-- This parrot wouldn't", action, end=' ')
    print("if you put", voltage, "volts through it.")
    print("-- Lovely plumage, the", type)
    print("-- It's", state, "!")
```

__corect calls__


```python
parrot('1','2','3','4') # adding def parameters
```

    -- This parrot wouldn't 3 if you put 1 volts through it.
    -- Lovely plumage, the 4
    -- It's 2 !



```python
parrot(1000)                                          # 1 positional argument
```

    -- This parrot wouldn't voom if you put 1000 volts through it.
    -- Lovely plumage, the Norwegian Blue
    -- It's a stiff !



```python
parrot(voltage=1000)                                  # 1 keyword argument
```

    -- This parrot wouldn't voom if you put 1000 volts through it.
    -- Lovely plumage, the Norwegian Blue
    -- It's a stiff !



```python
parrot(voltage=1000000, action='VOOOOOM')             # 2 keyword arguments
```

    -- This parrot wouldn't VOOOOOM if you put 1000000 volts through it.
    -- Lovely plumage, the Norwegian Blue
    -- It's a stiff !



```python
parrot(action='VOOOOOM', voltage=1000000)             # 2 keyword arguments
```

    -- This parrot wouldn't VOOOOOM if you put 1000000 volts through it.
    -- Lovely plumage, the Norwegian Blue
    -- It's a stiff !



```python
parrot('a million', 'bereft of life', 'jump')         # 3 positional arguments
```

    -- This parrot wouldn't jump if you put a million volts through it.
    -- Lovely plumage, the Norwegian Blue
    -- It's bereft of life !



```python
parrot('a thousand', state='pushing up the daisies')  # 1 positional, 1 keyword
```

    -- This parrot wouldn't voom if you put a thousand volts through it. E's pushing up the daisies !


__XXX Incorrect calls XXX__
parrot()                     # required argument missing
parrot(voltage=5.0, 'dead')  # non-keyword argument after a keyword argument
parrot(110, voltage=220)     # duplicate value for the same argument
parrot(actor='John Cleese')  # unknown keyword argument
def function(a):
    pass

function(0, a=0)

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: function() got multiple values for keyword argument 'a'

# [dictionary](https://docs.python.org/3/library/stdtypes.html#typesmapping) 
`**name`

**dictionary `dictionary = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}`

**dictionary `thisdict = {"brand": "Ford", "model": "Mustang","year": 1964}`

# [tuple](https://docs.python.org/3/tutorial/datastructures.html#tut-tuples)

`*name`

*tuple: `t = 12345, 54321, 'hello!'`  

*tuple: `thistuple = ("apple", "banana", "cherry")`

*nested tuple: `u = ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))`


```python
def cheeseshop(kind, *arguments, **keywords):
    print("-- Do you have any", kind, "?")
    print("-- I'm sorry, we're all out of", kind)
    
    for arg in arguments:
        print(arg)
    
    print("-" * 40)
    
    for kw in keywords:
        print(kw, ":", keywords[kw])
        
cheeseshop("Limburger", "It's very runny, sir.",
           "It's really very, VERY runny, sir.",
           shopkeeper="Michael Palin",
           client="John Cleese",
           sketch="Cheese Shop Sketch")
```

    -- Do you have any Limburger ?
    -- I'm sorry, we're all out of Limburger
    It's very runny, sir.
    It's really very, VERY runny, sir.
    ----------------------------------------
    shopkeeper : Michael Palin
    client : John Cleese
    sketch : Cheese Shop Sketch


#### DICTIONARY


```python
a = dict(one=1, two=2, three=3)
b = {'one': 1, 'two': 2, 'three': 3}
c = dict(zip(['one', 'two', 'three'], [1, 2, 3]))
d = dict([('two', 2), ('one', 1), ('three', 3)])
e = dict({'three': 3, 'one': 1, 'two': 2})
a == b == c == d == e
```




    True



#### TUPLE


```python
#TUPLE
t = 12345, 54321, 'hello!'
t[0]
```




    12345




```python
t
```




    (12345, 54321, 'hello!')




```python
# Tuples may be nested:
u = t, (1, 2, 3, 4, 5)
u
```




    ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))


# Tuples are immutable:
t[0] = 88888
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-53-9e19cce22619> in <module>
      1 # Tuples are immutable:
----> 2 t[0] = 88888

TypeError: 'tuple' object does not support item assignment

```python
# but they can contain mutable objects:
v = ([1, 2, 3], [3, 2, 1])
v
```




    ([1, 2, 3], [3, 2, 1])



### 4.7.3. `def` String Lists Formating


```python
def write_multiple_items(file, separator, *args):
    file.write(separator.join(args))
```


```python
def concat(*args, sep="/"):
    return sep.join(args)

concat("earth", "mars", "venus")
```




    'earth/mars/venus'




```python
concat("earth", "mars", "venus", sep=".")
```




    'earth.mars.venus'



### 4.7.4. def <- List, Tuples


```python
list(range(3, 6))            # normal call with separate arguments
```




    [3, 4, 5]




```python
args = [3, 6]
list(range(*args))            # call with arguments unpacked from a list
```




    [3, 4, 5]




```python
def parrot(voltage, state='a stiff', action='voom'):
    print("-- This parrot wouldn't", action, end=' ')
    print("if you put", voltage, "volts through it.", end=' ')
    print("E's", state, "!")

f = {"voltage": "1", "state": "2", "action": "3"}
parrot(**f)
```

    -- This parrot wouldn't 3 if you put 1 volts through it. E's 2 !



```python
d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
parrot(**d)
```

    -- This parrot wouldn't VOOM if you put four million volts through it. E's bleedin' demised !


### 4.7.5. [Lambda Expression](https://docs.python.org/3/reference/expressions.html#lambda)
- __Small anonymous functions__ can be created with the lambda keyword. 
- This function returns the sum of its two arguments: 
    - `lambda a, b: a+b`
- Lambda functions can be used wherever function objects are required. 
- They are syntactically restricted to a single expression. 
- Semantically, they are just syntactic sugar for a normal function definition. 
- Like nested function definitions, lambda functions can reference variables from the containing scope:


```python
def make_incrementor(n):
    return lambda x: x + n

f = make_incrementor(42)
```


```python
f(0)
```




    42




```python
f(1)
```




    43




```python
pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
pairs.sort(key=lambda pair: pair[1]) #pass a small lambda function as an argument
pairs
```




    [(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]



### 4.7.6. def Documentation Strings `__doc__`


```python
def my_function():
    """Do nothing, but document it.

    No, really, it doesn't do anything.
    """
    pass

print(my_function.__doc__)
```

    Do nothing, but document it.
    
        No, really, it doesn't do anything.
        


### 4.7.7. Function Annotations `__annotations__`


```python
def f(ham: str, eggs: str = 'eggs') -> str:
    print("Annotations:", f.__annotations__)
    print("Arguments:", ham, eggs)
    return ham + ' and ' + eggs

f('spam')
```

    Annotations: {'ham': <class 'str'>, 'eggs': <class 'str'>, 'return': <class 'str'>}
    Arguments: spam eggs





    'spam and eggs'



## 4.8. Intermezzo: Coding Style
[classes](https://docs.python.org/3/tutorial/classes.html#tut-firstclasses)

# [5. Data Structures](https://docs.python.org/3/tutorial/datastructures.html)
## 5.1. Lists 
`list.append(x)`
Add an item to the end of the list. Equivalent to a[len(a):] = [x].

`list.extend(iterable)`
Extend the list by appending all the items from the iterable. Equivalent to a[len(a):] = iterable.

`list.insert(i, x)`
Insert an item at a given position. The first argument is the index of the element before which to insert, so a.insert(0, x) inserts at the front of the list, and a.insert(len(a), x) is equivalent to a.append(x).

`list.remove(x)`
Remove the first item from the list whose value is equal to x. It raises a ValueError if there is no such item.

`list.pop([i])`
Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list. (The square brackets around the i in the method signature denote that the parameter is optional, not that you should type square brackets at that position. You will see this notation frequently in the Python Library Reference.)

`list.clear()`
Remove all items from the list. Equivalent to del a[:].

`list.index(x[, start[, end]])`
Return zero-based index in the list of the first item whose value is equal to x. Raises a ValueError if there is no such item.

The optional arguments start and end are interpreted as in the slice notation and are used to limit the search to a particular subsequence of the list. The returned index is computed relative to the beginning of the full sequence rather than the start argument.

`list.count(x)`
Return the number of times x appears in the list.

`list.sort(key=None, reverse=False)`
Sort the items of the list in place (the arguments can be used for sort customization, see sorted() for their explanation).

`list.reverse()`
Reverse the elements of the list in place.

`list.copy()`
Return a shallow copy of the list. Equivalent to a[:].


```python
fruits = ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']
fruits.count('apple')
```




    2




```python
fruits.count('tangerine')
```




    0




```python
fruits.index('banana')
```




    3




```python
fruits.index('banana', 4)  # Find next banana starting a position 4
```




    6




```python
fruits.reverse()
fruits
```




    ['banana', 'apple', 'kiwi', 'banana', 'pear', 'apple', 'orange']




```python
fruits.append('grape')
fruits
```




    ['banana', 'apple', 'kiwi', 'banana', 'pear', 'apple', 'orange', 'grape']




```python
fruits.sort() # abc 123
fruits
```




    ['apple', 'apple', 'banana', 'banana', 'grape', 'kiwi', 'orange', 'pear']




```python
fruits.pop()
```




    'pear'



### 5.1.1. Lists: Stacks up/down elements


```python
stack = [3, 4, 5]
stack.append(6)
stack.append(7)
stack
```




    [3, 4, 5, 6, 7]




```python
stack.pop() #retrieve an item from the top of the stack
```




    7




```python
stack
```




    [3, 4, 5, 6]



### 5.1.2. Waitning `List`


```python
from collections import deque
queue = deque(["Eric", "John", "Michael"])
queue.append("Terry")           # Terry arrives
queue.append("Graham")          # Graham arrives
queue.popleft()                 # The first to arrive now leaves 
# retrieve an item from the top of the stack
```




    'Eric'



### 5.1.3. `List` use in Complex Situations


```python
squares = []
for x in range(10):
    squares.append(x**2)

squares
```




    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]




```python
squares = list(map(lambda x: x**2, range(10)))   #?????????
```


```python
squares = [x**2 for x in range(10)]  #?????????
```


```python
[(x, y) for x in [1,2,3] for y in [3,1,4] if x != y] 
```




    [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]




```python
combs = []
for x in [1,2,3]:
    for y in [3,1,4]:
        if x != y:
            combs.append((x, y))

combs
```




    [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]




```python
vec = [-4, -2, 0, 2, 4]
```


```python
# create a new list with the values doubled
[x*2 for x in vec]
```




    [-8, -4, 0, 4, 8]




```python
# filter the list to exclude negative numbers
[x for x in vec if x >= 0]
```




    [0, 2, 4]




```python
# apply a function to all the elements
[abs(x) for x in vec]
```




    [4, 2, 0, 2, 4]




```python
# call a method on each element
freshfruit = ['  banana', '  loganberry ', 'passion fruit  ']
[weapon.strip() for weapon in freshfruit]
```




    ['banana', 'loganberry', 'passion fruit']




```python
# create a list of 2-tuples like (number, square)
[(x, x**2) for x in range(6)]
```




    [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]


# the tuple must be parenthesized, otherwise an error is raised
[x, x**2 for x in range(6)]

  File "<ipython-input-103-702d12ece8a4>", line 2
    [x, x**2 for x in range(6)]
               ^
SyntaxError: invalid syntax

```python
# flatten a list using a listcomp with two 'for'
vec = [[1,2,3], [4,5,6], [7,8,9]]
[num for elem in vec for num in elem]
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
from math import pi
[str(round(pi, i)) for i in range(1, 6)]
```




    ['3.1', '3.14', '3.142', '3.1416', '3.14159']



### 5.1.4. Nested List Understand
[Unpacking Argument Lists](https://docs.python.org/3/tutorial/controlflow.html#tut-unpacking-arguments)


```python
matrix = [
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12],
]
```


```python
#transpose rows and columns
#A.
[[row[i] for row in matrix] for i in range(4)] 
```




    [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]




```python
#B.
transposed = []
for i in range(4):
    transposed.append([row[i] for row in matrix])

transposed
```




    [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]




```python
#C.
transposed = []
for i in range(4):
    # the following 3 lines implement the nested listcomp
    transposed_row = []
    for row in matrix:
        transposed_row.append(row[i])
    transposed.append(transposed_row)

transposed
```




    [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]




```python
#D. https://docs.python.org/3/library/functions.html#zip
list(zip(*matrix))
```




    [(1, 5, 9), (2, 6, 10), (3, 7, 11), (4, 8, 12)]



## 5.2. `del`  = DELETE list value
remove an item from a list given its index instead of its value


```python
a = [-1, 1, 66.25, 333, 333, 1234.5]
del a[0]
a
```




    [1, 66.25, 333, 333, 1234.5]




```python
del a[2:4]
a
```




    [1, 66.25, 1234.5]




```python
del a[:]
a
```




    []



## 5.3. `Tuples` & [`Sequences`: list, tuple, range](https://docs.python.org/3/library/stdtypes.html#typesseq) data types


```python
t = 12345, 54321, 'hello!'
t[0]
```




    12345




```python
# Tuples NESTable
u = t, (1, 2, 3, 4, 5)
u
```




    ((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))


# Tuples immutable
t[0] = 88888

---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-121-9e19cce22619> in <module>
      1 # Tuples are immutable:
----> 2 t[0] = 88888

TypeError: 'tuple' object does not support item assignment

```python
# Tuples can contain mutable objects:
v = ([1, 2, 3], [3, 2, 1])
v
```




    ([1, 2, 3], [3, 2, 1])




```python
# empty Tuples
empty = ()
len(empty)
```




    0




```python
singleton = 'hello',    # <-- note trailing comma
len(singleton)
```




    1




```python
singleton # <-- note trailing comma "following comma"
```




    ('hello',)




```python
#tuple packing
t = 1, 2, 'hello!'

#reverse tuple UN-packing = sequence unpacking
x, y, z = t

print(x , y, z)
```

    1 2 hello!


## 5.4. `Sets` data types


```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
print(basket)                      # show that duplicates have been removed
```

    {'pear', 'orange', 'apple', 'banana'}



```python
'orange' in basket                 # fast membership testing
```




    True




```python
'crabgrass' in basket
```




    False




```python
# Demonstrate set operations on unique letters from two words
a = set('abracadabra')
b = set('alacazam')
a                                  # unique letters in a
```




    {'a', 'b', 'c', 'd', 'r'}




```python
a - b                              # letters in a but not in b
```




    {'b', 'd', 'r'}




```python
a | b                              # letters in a or b or both
```




    {'a', 'b', 'c', 'd', 'l', 'm', 'r', 'z'}




```python
a & b                              # letters in both a and b
```




    {'a', 'c'}




```python
a ^ b                              # letters in a or b but not both
```




    {'b', 'd', 'l', 'm', 'r', 'z'}



## 5.7 Conditions II.
"#generalBooleanAlgebraStaff"


```python
'''?????????????????'''
string1, string2, string3 = '', 'Trondheim', 'Hammer Dance'
non_null = string1 or string2 or string3
non_null
```




    'Trondheim'



## 5.8. Comparing Sequences and Other Types


```python
(1, 2, 3)              < (1, 2, 4)
```




    True




```python
[1, 2, 3]              < [1, 2, 4]
```




    True




```python
'ABC' < 'C' < 'Pascal' < 'Python'
```




    True




```python
(1, 2, 3, 4)           < (1, 2, 4)
```




    True




```python
(1, 2)                 < (1, 2, -1)
```




    True




```python
(1, 2, 3)             == (1.0, 2.0, 3.0)
```




    True




```python
(1, 2, ('aa', 'ab'))   < (1, 2, ('abc', 'a'), 4)
```




    True



# [6. Modules](https://docs.python.org/3/tutorial/modules.html)
`Script`: 
- If you quit from the Python interpreter and enter it again, the definitions you have made (functions and variables) are lost. 
- longer program
    - using a text editor 
    - to prepare the input for the interpreter and running it with that file as input instead.
    - split in to several files for better organisation
- MODULE:
    - Pyhton def -> file
        - scrit
        - interactice instance
        -  filename = module name



```python
#SAVED as: "fibo.py"
def fib(n):    # write Fibonacci series up to n
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    print()

def fib2(n):   # return Fibonacci series up to n
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a+b
    return result

'''
if __name__ == "__main__":
    import sys
    fib(int(sys.argv[1]))'''
```




    '\nif __name__ == "__main__":\n    import sys\n    fib(int(sys.argv[1]))'




```python
#fibo.py file created in a text editor document isn the same folder
import fibo # import
```


```python
fibo.fib(1000)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 



```python
fibo.fib2(100)
```




    [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]




```python
fibo.__name__
```




    'fibo'




```python
fib = fibo.fib
fib(500)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 


## 6.1. Modules I.
- executable statements
    - initialise
    - 1st time rune wheh module importd
- def functions
- each modul
    - own private symbol table
    - used as GLOBAL for all -> def in that modul
- can use GLOBAL variables ex.: "modname.itemname"
- imported module names -[placed]-> importing module’s global symbol table    


```python
#This does not introduce the module name (fibo and if it would have other defs) from which the imports are taken 
#in the local symbol table (so in the example, fibo is not defined)
from fibo import fib, fib2
fib(500)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 



```python
#import all names that a module defines
#except those beginning with an underscore _
#NOT used: introduces an unknown set of names into the interpreter
from fibo import * 
fib(500)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 



```python
#import fibo will do, with the only difference of it being available as fib
import fibo as fib
fib.fib(500)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 



```python
# import a pecific def iunder a better name
from fibo import fib as fibonacci
fibonacci(500)
```

    0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 


### 6.1.1. Executing modules as scripts
added to fibo module

if __name__ == "__main__":
    import sys
    fib(int(sys.argv[1]))RUN IN TERMINAL
>>bash-3.2$ python fibo.py 50
0 1 1 2 3 5 8 13 21 34
### 6.1.2. Module Search Path
aka how does the computer finds your staff
- When a module named spam is imported, the interpreter first searches for a built-in module with that name. 
- If not found, it then searches for a file named spam.py in a list of directories given by the variable __`sys.path`__
-  __`sys.path`__ is initialized from these locations:
    - The directory containing the input script (or the current directory when no file is specified).
    - [PYTHONPATH](https://docs.python.org/3/using/cmdline.html#envvar-PYTHONPATH) (a list of directory names, with the same syntax as the shell variable PATH).
    - The installation-dependent default. 

### 6.1.3. “Compiled” Python files
- speed up loading modules, Python caches the compiled version of each module in the __pycache__ directory under the name module.version.pyc

## 6.2. Standard Modules
- official python standard library modules


```python
import sys
sys.ps1
```




    'C> '




```python
sys.ps2
```




    '...: '




```python
sys.ps1 = 'C> '
```


```python
# modify interpreter;s serch parth for modul (using standard list operations)
import sys
sys.path.append('/ufs/guido/lib/python')
```

## 6.3 [dir()](https://docs.python.org/3/library/functions.html#dir) def
modul's all defs


```python
import fibo, sys
dir(fibo)
```




    ['__builtins__',
     '__cached__',
     '__doc__',
     '__file__',
     '__loader__',
     '__name__',
     '__package__',
     '__spec__',
     'fib',
     'fib2']




```python
dir(sys)
```




    ['__breakpointhook__',
     '__displayhook__',
     '__doc__',
     '__excepthook__',
     '__interactivehook__',
     '__loader__',
     '__name__',
     '__package__',
     '__spec__',
     '__stderr__',
     '__stdin__',
     '__stdout__',
     '_clear_type_cache',
     '_current_frames',
     '_debugmallocstats',
     '_framework',
     '_getframe',
     '_git',
     '_home',
     '_xoptions',
     'abiflags',
     'api_version',
     'argv',
     'base_exec_prefix',
     'base_prefix',
     'breakpointhook',
     'builtin_module_names',
     'byteorder',
     'call_tracing',
     'callstats',
     'copyright',
     'displayhook',
     'dont_write_bytecode',
     'exc_info',
     'excepthook',
     'exec_prefix',
     'executable',
     'exit',
     'flags',
     'float_info',
     'float_repr_style',
     'get_asyncgen_hooks',
     'get_coroutine_origin_tracking_depth',
     'get_coroutine_wrapper',
     'getallocatedblocks',
     'getcheckinterval',
     'getdefaultencoding',
     'getdlopenflags',
     'getfilesystemencodeerrors',
     'getfilesystemencoding',
     'getprofile',
     'getrecursionlimit',
     'getrefcount',
     'getsizeof',
     'getswitchinterval',
     'gettrace',
     'hash_info',
     'hexversion',
     'implementation',
     'int_info',
     'intern',
     'is_finalizing',
     'last_traceback',
     'last_type',
     'last_value',
     'maxsize',
     'maxunicode',
     'meta_path',
     'modules',
     'path',
     'path_hooks',
     'path_importer_cache',
     'platform',
     'prefix',
     'ps1',
     'ps2',
     'ps3',
     'set_asyncgen_hooks',
     'set_coroutine_origin_tracking_depth',
     'set_coroutine_wrapper',
     'setcheckinterval',
     'setdlopenflags',
     'setprofile',
     'setrecursionlimit',
     'setswitchinterval',
     'settrace',
     'stderr',
     'stdin',
     'stdout',
     'thread_info',
     'version',
     'version_info',
     'warnoptions']




```python
# empty dir() = currently defined def-s
a = [1, 2, 3, 4, 5]
import fibo
fib = fibo.fib


#dir()
```


```python
import builtins #list the names of built-in functions and variables
#dir(builtins) 
```

## 6.4. Packages
- extensions: .wav, .aiff, .au
-  A.B designates: A package, B submodule
-  __ __init__ __.py files are required to make Python treat directories containing the file as packages.
- EX.: __Sound__ module (no module have benn found under this name so I only used them as articel not code so it doesent gives error)
sound/                          Top-level package
      __init__.py               Initialize the sound package
      formats/                  Subpackage for file format conversions
              __init__.py
              wavread.py
              wavwrite.py
              aiffread.py
              aiffwrite.py
              auread.py
              auwrite.py
              ...
      effects/                  Subpackage for sound effects
              __init__.py
              echo.py
              surround.py
              reverse.py
              ...
      filters/                  Subpackage for filters
              __init__.py
              equalizer.py
              vocoder.py
              karaoke.py
              ...
import individual modules from the package
import sound.effects.echo
use submodul of a flully imported library
import sound 
sound.effects.echo.echofilter(input, output, delay=0.7, atten=4)
alternative way of importing the submodule

from sound.effects import echo

also loads the submodule echo, and makes it available without its package prefix

echo.echofilter(input, output, delay=0.7, atten=4)

import the desired function or variable directly
from sound.effects.echo import echofilter
Again, this loads the submodule echo, but this makes its function echofilter() directly available:
echofilter(input, output, delay=0.7, atten=4)
### 6.4.1. Importing * From a Package
#??????????????????????????????
from sound.effects import *

__all__ = ["echo", "surround", "reverse"]

#............
### 6.4.2. Intra-package References
from . import echo
from .. import formats
from ..filters import equalizer
### 6.4.3. Packages in Multiple Directories

# [7. Input and Output](https://docs.python.org/3/tutorial/inputoutput.html) printout
## 7.1. Output Formatting


```python
year = 2016
event = 'Referendum'
f'Results of the {year} {event}'
```




    'Results of the 2016 Referendum'




```python
yes_votes = 42_572_654
no_votes = 43_132_495
percentage = yes_votes / (yes_votes + no_votes)

'{:-9} YES votes  {:2.2%}'.format(yes_votes, percentage) #formating
```




    ' 42572654 YES votes  49.67%'




```python
s = 'Hello, world.'
str(s) #human-readable values
```




    'Hello, world.'




```python
repr(s) #interpreter can reed these values
```




    "'Hello, world.'"




```python
str(1/7)
```




    '0.14285714285714285'




```python
x = 10 * 3.25
y = 200 * 200
s = 'The value of x is ' + repr(x) + ', and y is ' + repr(y) + '...'
print(s)
```

    The value of x is 32.5, and y is 40000...



```python
# The repr() of a string adds string quotes and backslashes:
hello = 'hello, world\n'
hellos = repr(hello)
print(hellos)
```

    'hello, world\n'



```python
# The argument to repr() may be any Python object:
repr((x, y, ('spam', 'eggs')))
```




    "(32.5, 40000, ('spam', 'eggs'))"



### 7.1.1. [String fromating](https://docs.python.org/3/reference/lexical_analysis.html#f-strings) [+Examples](https://docs.python.org/3/library/string.html#formatstrings)


```python
import math
print(f'The value of pi is approximately {math.pi:.3f}.')
```

    The value of pi is approximately 3.142.



```python
table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
for name, phone in table.items():
    print(f'{name:10} ==> {phone:10d}')
```

    Sjoerd     ==>       4127
    Jack       ==>       4098
    Dcab       ==>       7678



```python
animals = 'eels'
print(f'My hovercraft is full of {animals}.')
```

    My hovercraft is full of eels.



```python
print(f'My hovercraft is full of {animals!r}.')
```

    My hovercraft is full of 'eels'.


### 7.1.2. `String format()` Method


```python
print('We are the {} who say "{}!"'.format('knights', 'Ni'))
```

    We are the knights who say "Ni!"



```python
print('{0} and {1}'.format('spam', 'eggs'))
```

    spam and eggs



```python
print('{1} and {0}'.format('spam', 'eggs'))
```

    eggs and spam



```python
print('This {food} is {adjective}.'.format(
      food='spam', adjective='absolutely horrible'))
```

    This spam is absolutely horrible.



```python
print('The story of {0}, {1}, and {other}.'.format('Bill', 
                                                   'Manfred',other='Georg'))
```

    The story of Bill, Manfred, and Georg.



```python
table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678} #dictionary
print('Jack: {0[Jack]:d}; Sjoerd: {0[Sjoerd]:d}; '
      'Dcab: {0[Dcab]:d}'.format(table))
```

    Jack: 4098; Sjoerd: 4127; Dcab: 8637678



```python
table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678} #dictionary
print('Jack: {Jack:d}; Sjoerd: {Sjoerd:d}; Dcab: {Dcab:d}'.format(**table))
```

    Jack: 4098; Sjoerd: 4127; Dcab: 8637678



```python
for x in range(1, 11):
    print('{0:2d} {1:3d} {2:4d}'.format(x, x*x, x*x*x))
```

     1   1    1
     2   4    8
     3   9   27
     4  16   64
     5  25  125
     6  36  216
     7  49  343
     8  64  512
     9  81  729
    10 100 1000


### 7.1.3. `String Formatting` Manualy
`str.rjust()` right-justifies a string in a field of a given width by padding it with spaces on the left

`str.ljust()`

`str.center()`

slice operation: `x.ljust(n)[:n]`


```python
for x in range(1, 11):
    print(repr(x).rjust(2), repr(x*x).rjust(3), end=' ')
    # Note use of 'end' on previous line
    print(repr(x*x*x).rjust(4))
```

     1   1    1
     2   4    8
     3   9   27
     4  16   64
     5  25  125
     6  36  216
     7  49  343
     8  64  512
     9  81  729
    10 100 1000



```python
'12'.zfill(5)
```




    '00012'




```python
'-3.14'.zfill(7)
```




    '-003.14'




```python
'3.14159265359'.zfill(5)
```




    '3.14159265359'



### 7.1.4. Old string formatting


```python
import math
print('The value of pi is approximately %5.3f.' % math.pi)
```

    The value of pi is approximately 3.142.


## 7.2. Reading and Writing Files
[open](https://docs.python.org/3/library/functions.html#open)

returns a [file object](https://docs.python.org/3/glossary.html#term-file-object)

`open(filename, mode)`

modes:
- __`r`__ only be read file
- __`w`__ only writing file
- __`a`__ opens the file for appending; any data written to the file is automatically added to the end
- __`r+`__ opens the file for both reading and writing
-  __`b`__ appended to the mode opens the file in binary mode
    - JPEG or EXE files

readig modes:
- \n on Unix, 
- \r\n on Windows


```python
f = open('workfile', 'w')
```

### `with` Advantage:
- the file is properly closed after its suite finishes, 
    - even if an exception is raised at some point. 
- Using with is also much shorter than writing equivalent `try-finally` blocks:


```python
with open('workfile.txt') as f:
    read_data = f.read()
f.closed
```




    True



### 7.2.1. File Objects Methods

`f.close()`

`f.read()`

`f.readline()` reads a single line from the file

`\n` a newline character 


```python
f.readline()

f.readline()

f.readline()
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-462-790e3b5ef116> in <module>
    ----> 1 f.readline()
          2 
          3 f.readline()
          4 
          5 f.readline()


    ValueError: I/O operation on closed file.



```python
#reading lines from a file
#loop over the file object

for line in f:
    print(line, end='')
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-463-a2240113506e> in <module>
          2 #loop over the file object
          3 
    ----> 4 for line in f:
          5     print(line, end='')


    ValueError: I/O operation on closed file.



```python
#file --[read all lines]--> list 

list(f)
f.readlines()
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-464-cdae811366b7> in <module>
          1 #file --[read all lines]--> list
          2 
    ----> 3 list(f)
          4 f.readlines()


    ValueError: I/O operation on closed file.



```python
#f.write(string)
#writes the contents of string to the file, 
#returning the number of characters written.

f.write('This is a test\n')
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-465-b140dfe3afed> in <module>
          3 #returning the number of characters written.
          4 
    ----> 5 f.write('This is a test\n')
    

    ValueError: I/O operation on closed file.



```python
value = ('the answer', 42)
s = str(value)  # convert the tuple to string
f.write(s)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-466-ed08d1bc4d2e> in <module>
          1 value = ('the answer', 42)
          2 s = str(value)  # convert the tuple to string
    ----> 3 f.write(s)
    

    ValueError: I/O operation on closed file.


returns an integer giving the file object’s current position

`f.tell()`

To change the file object’s position

`f.seek(offset, from_what)`


```python
f = open('workfile', 'rb+')
f.write(b'0123456789abcdef')
```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    <ipython-input-467-1e25b45cd89f> in <module>
    ----> 1 f = open('workfile', 'rb+')
          2 f.write(b'0123456789abcdef')


    FileNotFoundError: [Errno 2] No such file or directory: 'workfile'



```python
f.seek(5)      # Go to the 6th byte in the file
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-468-19c1b8db62c8> in <module>
    ----> 1 f.seek(5)      # Go to the 6th byte in the file
    

    ValueError: I/O operation on closed file.



```python
f.read(1)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-469-5a354f952aa4> in <module>
    ----> 1 f.read(1)
    

    ValueError: I/O operation on closed file.



```python
f.seek(-3, 2)  # Go to the 3rd byte before the end
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-470-5a87e8acba68> in <module>
    ----> 1 f.seek(-3, 2)  # Go to the 3rd byte before the end
    

    ValueError: I/O operation on closed file.



```python
f.read(1)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-471-5a354f952aa4> in <module>
    ----> 1 f.read(1)
    

    ValueError: I/O operation on closed file.


### 7.2.2. Structured Data --[Saving]--> [JSON](https://docs.python.org/3/library/json.html#module-json)

`dumps()`
view JSON string representation


```python
import json
json.dumps([1, 'simple', 'list'])
```




    '[1, "simple", "list"]'



#### serializes the object to a text file
- x: object to save
- f: text file

`json.dump(x, f)`

#### decode the object
- f is a text file object 
- which has been opened for reading

x = json.load(f)

### [pickle](https://docs.python.org/3/library/pickle.html#module-pickle)
- SAVE MACHINE LEARNING TRAINED MODELS
- allows the serialization of arbitrarily complex Python objects. 
- As such, it is specific to Python and cannot be used to communicate with applications written in other languages. 
- It is also insecure by default: deserializing pickle data coming from an untrusted source can execute arbitrary code, if the data was crafted by a skilled attacker.

# [8. Errors and Exceptions](https://docs.python.org/3/tutorial/errors.html)
## 8.1. Syntax Errors
Syntax errors = parsing errors
while True print('Hello world')


  File "<stdin>", line 1
    while True print('Hello world')
                   ^
SyntaxError: invalid syntax
Correct runs till intifnity

`while True: print('Hello world')`

## 8.2. Exceptions
- [ZeroDivisionError](https://docs.python.org/3/library/exceptions.html#ZeroDivisionError)
- [NameError](https://docs.python.org/3/library/exceptions.html#NameError)
- [TypeError](https://docs.python.org/3/library/exceptions.html#TypeError)

>>> 10 * (1/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero

>>> 4 + spam*3
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'spam' is not defined

>>> '2' + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: Can't convert 'int' object to str implicitly
## 8.3. Handling Exceptions
except (RuntimeError, TypeError, NameError):
     pass
### [__try__](https://docs.python.org/3/reference/compound_stmts.html#try)
- First, the try clause (the statement(s) between the try and except keywords) is executed.
- If no exception occurs, the except clause is skipped and execution of the try statement is finished.
- If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try statement.
- If an exception occurs which does not match the exception named in the except clause, it is passed on to outer try statements; if no handler is found, it is an unhandled exception and execution stops with a message as shown above.


```python
while True:
    try:
        x = int(input("Please enter a number: "))
        break
    except ValueError:
        print("Oops!  That was no valid number.  Try again...")
```

    Please enter a number:  4


### [except](https://docs.python.org/3/reference/compound_stmts.html#except)
except clause is compatible with an exception if it is the same class or a base class thereof (but not the other way around — an except clause listing a derived class is not compatible with a base class
??????????????????????????????????


```python
class B(Exception):
    pass

class C(B):
    pass

class D(C):
    pass

for cls in [B, C, D]:
    try:
        raise cls()
    except D:
        print("D")
    except C:
        print("C")
    except B:
        print("B")
```

    B
    C
    D



```python
import sys

try:
    f = open('myfile.txt') #creatd file filled with strings
    s = f.readline()
    i = int(s.strip())
except OSError as err:
    print("OS error: {0}".format(err))
except ValueError:
    print("Could not convert data to an integer.")
except:
    print("Unexpected error:", sys.exc_info()[0])
    raise
```

    Could not convert data to an integer.



```python
# try … except statement has an optional else clause,
for arg in sys.argv[1:]:
    try:
        f = open(arg, 'r')
    except OSError:
        print('cannot open', arg)
    else:
        print(arg, 'has', len(f.readlines()), 'lines')
        f.close()
```

    cannot open -f
    /Users/macbookair13/Library/Jupyter/runtime/kernel-715733f0-9a51-43df-ab48-069c7b7993af.json has 12 lines



```python
try:
    raise Exception('spam', 'eggs')
except Exception as inst:
    print(type(inst))    # the exception instance
    print(inst.args)     # arguments stored in .args
    print(inst)          # __str__ allows args to be printed directly,
                         # but may be overridden in exception subclasses
    x, y = inst.args     # unpack args
    print('x =', x)
    print('y =', y)
```

    <class 'Exception'>
    ('spam', 'eggs')
    ('spam', 'eggs')
    x = spam
    y = eggs



```python
def this_fails():
    x = 1/0

try:
    this_fails()
except ZeroDivisionError as err:
    print('Handling run-time error:', err)
```

    Handling run-time error: division by zero


## 8.4. `raise` Exceptions
`raise` force a specified exception to occur
raise NameError('HiThere')


---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-112-72c183edb298> in <module>
----> 1 raise NameError('HiThere')

NameError: HiTheretry:
    raise NameError('HiThere')
except NameError:
    print('An exception flew by!')
    raise
    
    
An exception flew by!
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-113-bf6ef4926f8c> in <module>
      1 try:
----> 2     raise NameError('HiThere')
      3 except NameError:
      4     print('An exception flew by!')
      5     raise

NameError: HiThere
## 8.5. User-defined Exceptions
- [classes](https://docs.python.org/3/tutorial/classes.html#tut-classes)
    - [Exception](https://docs.python.org/3/library/exceptions.html#Exception)


```python
class Error(Exception):
    """Base class for exceptions in this module."""
    pass

class InputError(Error):
    """Exception raised for errors in the input.

    Attributes:
        expression -- input expression in which the error occurred
        message -- explanation of the error
    """

    def __init__(self, expression, message):
        self.expression = expression
        self.message = message

class TransitionError(Error):
    """Raised when an operation attempts a state transition that's not
    allowed.

    Attributes:
        previous -- state at beginning of transition
        next -- attempted new state
        message -- explanation of why the specific transition is not allowed
    """

    def __init__(self, previous, next, message):
        self.previous = previous
        self.next = next
        self.message = message
```

## 8.6. try `finally`
- Defining Clean-up Action
- must be executed under all circumstances
try:
    raise KeyboardInterrupt
finally: #cean-up actions that must be executed under all circumstances
    print('Goodbye, world!')
    
    
---------------------------------------------------------------------------
KeyboardInterrupt                         Traceback (most recent call last)
<ipython-input-117-8cf82136c8c0> in <module>
      1 try:
----> 2     raise KeyboardInterrupt
      3 finally: #cean-up actions that must be executed under all circumstances
      4     print('Goodbye, world!')

KeyboardInterrupt: 

```python
def bool_return(): #-> bool:
    try:
        return True
    finally:
        return False

bool_return()
```




    False




```python
#def try exxcept else finally
def divide(x, y):
    try:
        result = x / y
    except ZeroDivisionError:
        print("division by zero!")
    else:
        print("result is", result)
    finally:
        print("executing finally clause")
        
divide(2, 1)
```

    result is 2.0
    executing finally clause



```python
divide(2, 0)
```

    division by zero!
    executing finally clause

divide("2", "1")

executing finally clause
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-123-3ad63cdb9b7d> in <module>
----> 1 divide("2", "1")

<ipython-input-121-cbf715cb4bcb> in divide(x, y)
      1 def divide(x, y):
      2     try:
----> 3         result = x / y
      4     except ZeroDivisionError:
      5         print("division by zero!")

TypeError: unsupported operand type(s) for /: 'str' and 'str'
## 8.7. Clean-up files loaded in
### X file not closes itself


```python
for line in open("myfile.txt"):
    print(line, end="")
```

    hey
    hello hohohoh
    hiiihihi
    asfasf
    asfasf
    fas
    fasfasf

### Y file closes itself 
because it is loaded in to a `f` variable


```python
with open("myfile.txt") as f:
    for line in f:
        print(line, end="")
```

    hey
    hello hohohoh
    hiiihihi
    asfasf
    asfasf
    fas
    fasfasf

# [9. Classes](https://docs.python.org/3/tutorial/classes.html)
- class is never used as a global scope


## 9.1. A Word About Names and Objects

## 9.2. Python Scopes and Namespaces

### 9.2.1. Scopes and Namespaces Example
- reference 
    - scopes  
    - namespaces
- global and nonlocal affect 
    - variable binding


```python
def scope_test():
    def do_local():
        spam = "local spam"

    def do_nonlocal():
        nonlocal spam
        spam = "nonlocal spam"

    def do_global():
        global spam
        spam = "global spam"

    spam = "test spam"
    do_local()
    print("After local assignment:", spam)
    do_nonlocal()
    print("After nonlocal assignment:", spam)
    do_global()
    print("After global assignment:", spam)

scope_test()
print("In global scope:", spam)
```

    After local assignment: test spam
    After nonlocal assignment: nonlocal spam
    After global assignment: nonlocal spam
    In global scope: global spam


## 9.3. Classes I.
- 9.3.1. __new syntax__ 
- 9.3.2-4. __3 new object types__
    - Class Objects
    - Instance Objects
    - Method Objects 
- 9.3.5. __new semantics__

### 9.3.1. Class Definition Syntax
- new namespace
- local variables
- class definition END -> class object created
class ClassName:
    <statement-1>
    .
    .
    .
    <statement-N>
### 9.3.2. Class Objects I.
#### Attribute references
`MyClass.i` - integer object

`MyClass.f` - function object


```python
class MyClass:
    """A simple example class"""
    i = 12345

    def f(self):
        return 'hello world'
```

#### Instantiation
- CLASS -> OBJECT
- MyClass() -> x
- function notation
- Just pretend that the class object is a parameterless function that returns a new instance of the class


```python
x = MyClass()
```


```python
def __init__(self): #initial state def inside a class
    self.data = []
```


```python
class Complex:
    def __init__(self, realpart, imagpart):
        self.r = realpart
        self.i = imagpart

x = Complex(3.0, -4.5)
x.r, x.i
```




    (3.0, -4.5)



### 9.3.3. Instance Objects II.

#### A.) Data Atributes


```python
x.counter = 1
while x.counter < 10:
    x.counter = x.counter * 2
print(x.counter)
del x.counter
```

    16


#### B.) Methods:  
- is a function that “belongs to” an object
- not unique to class instances: other object types can have methods as well. 
    - EX.: list objects have methods called: `append, insert, remove, sort`


### 9.3.4. Method Objects
x.f() #method is called right after it is boundxf = x.f  #storing away methods
while True:
    print(xf())
### 9.3.5. Class and Instance Variables


```python
class Dog:
    kind = 'canine'         # class variable shared by all instances
    def __init__(self, name):
        self.name = name    # instance variable unique to each instance

d = Dog('Fido')
e = Dog('Buddy')
d.kind                  # shared by all dogs
```




    'canine'




```python
e.kind                  # shared by all dogs
```




    'canine'




```python
d.name                  # unique to d
```




    'Fido'




```python
e.name                  # unique to e
```




    'Buddy'



### X Wrong Class Design
Tricks list in the following code should not be used as a class variable because just a single list would be shared by all Dog instances


```python
class Dog:
    tricks = []             #!!! mistaken use of a class variable
    def __init__(self, name):
        self.name = name

    def add_trick(self, trick):
        self.tricks.append(trick)

d = Dog('Fido')
e = Dog('Buddy')
d.add_trick('roll over')
e.add_trick('play dead')

d.tricks                # unexpectedly shared by all dogs
```




    ['roll over', 'play dead']



### Y Correct Class Design 
use an instance variable instead

` self.tricks = []    #YYY creates a new empty list for each dog`


```python
class Dog:
    def __init__(self, name):
        self.name = name
        self.tricks = []    #YYY creates a new empty list for each dog
        
    def add_trick(self, trick):
        self.tricks.append(trick)

d = Dog('Fido')
e = Dog('Buddy')
d.add_trick('roll over')
e.add_trick('play dead')

d.tricks
```




    ['roll over']




```python
e.tricks
```




    ['play dead']



## 9.4. Random Remarks `self`
`self` - less error as a global variable

`self` - share variables inside the class

`self` - first __argument__ of a method


```python
# Function defined outside the class
def f1(self, x, y):
    return min(x, x+y)

class C:
    f = f1

    def g(self):
        return 'hello world'

    h = g
```

### Methods call --[self agrument, method attributes]--> other methods


```python
class Bag:
    def __init__(self):
        self.data = []

    def add(self, x):
        self.data.append(x)

    def addtwice(self, x):
        self.add(x)
        self.add(x)
```

## 9.5. Class Inheritance
class DerivedClassName(BaseClassName):
    <statement-1>
    .
    .
    .
    <statement-N>class DerivedClassName(modname.BaseClassName):
`isinstance()` to check an instance’s type: isinstance(obj, int) will be True only if "obj.__ _class_ __" is int or some class derived from int.

`issubclass()` to check class inheritance: issubclass(bool, int) is True since bool is a subclass of int. However, issubclass(float, int) is False since float is not a subclass of int.

### 9.5.1. Multiple Inheritance
class DerivedClassName(Base1, Base2, Base3):
    <statement-1>
    .
    .
    .
    <statement-N>
## 9.6. Private Variables
“Private” instance variables that cannot be accessed except from inside an object don’t exist in Python

`__spam` non-public part

`_classname__spam` classname is the current class name with leading underscore(s) stripped

letting subclasses override methods without breaking intraclass method calls:


```python
class Mapping:
    def __init__(self, iterable):
        self.items_list = []
        self.__update(iterable)

    def update(self, iterable):
        for item in iterable:
            self.items_list.append(item)

    __update = update   # private copy of original update() method

class MappingSubclass(Mapping):

    def update(self, keys, values):
        # provides new signature for update()
        # but does not break __init__()
        for item in zip(keys, values):
            self.items_list.append(item)
```

## 9.7. Uniqe Data Types Create
`m.__self__` Instance method object attributes

`m.__func__` is the function object corresponding to the method

data type similar to the Pascal “record” or C “struct”

bundling together a few named data items


```python
class Employee: #empty class definition
    pass

john = Employee()  # Create an empty employee record

# Fill the fields of the record
john.name = 'John Doe'
john.dept = 'computer lab'
john.salary = 1000
```

## 9.8. Iterators `for`


```python
for element in [1, 2, 3]:
    print(element)
for element in (1, 2, 3):
    print(element)
for key in {'one':1, 'two':2}:
    print(key)
for char in "123":
    print(char)
for line in open("myfile.txt"):
    print(line, end='')
```

    1
    2
    3
    1
    2
    3
    one
    two
    1
    2
    3
    hey
    hello hohohoh
    hiiihihi
    asfasf
    asfasf
    fas
    fasfasf
>>> s = 'abc'
>>> it = iter(s)
>>> it
<iterator object at 0x00A1DB50>
>>> next(it)
'a'
>>> next(it)
'b'
>>> next(it)
'c'
>>> next(it)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    next(it)
StopIteration
### mechanics behind the iterator protocol

1.`for`

2.`iter()` container object

3.return iterator object

4.`__next__()` def method

5.no more elements

6.`__next__()` raises a StopIteration exception

7.`for` terminate 


```python
class Reverse:
    """Iterator for looping over a sequence backwards."""
    def __init__(self, data):
        self.data = data
        self.index = len(data)

    def __iter__(self):
        return self

    def __next__(self):
        if self.index == 0:
            raise StopIteration
        self.index = self.index - 1
        return self.data[self.index]
```


```python
rev = Reverse('spam')
iter(rev)
```




    <__main__.Reverse at 0x10934cb70>




```python
for char in rev:
    print(char)
```

    m
    a
    p
    s


## 9.9. [Generators](https://docs.python.org/3/glossary.html#term-generator) 
~ normal def

`yield` - statement ENDING -> Return Data

Each time `next()` is called on it, the generator resumes where it left off (it remembers all the data values and which statement was last executed).

Generators  ~ class-based iterators


```python
def reverse(data):
    for index in range(len(data)-1, -1, -1):
        yield data[index]
```


```python
for char in reverse('golf'):
    print(char)
```

    f
    l
    o
    g


## 9.10. Generator Expressions


```python
sum(i*i for i in range(10))                 # sum of squares
```




    285




```python
xvec = [10, 20, 30]
yvec = [7, 5, 3]
sum(x*y for x,y in zip(xvec, yvec))         # dot product
```




    260




```python
from math import pi, sin
sine_table = {x: sin(x*pi/180) for x in range(0, 91)}
```
unique_words = set(word  for line in page  for word in line.split())valedictorian = max((student.gpa, student.name) for student in graduates)

```python
data = 'golf'
list(data[i] for i in range(len(data)-1, -1, -1))
```




    ['f', 'l', 'o', 'g']



# [10. Python Basic Modules I.](https://docs.python.org/3/tutorial/stdlib.html)
## 10.1. `OS` - Operating System Interface


```python
import os
os.getcwd()      # Return the current working directory
```




    '/Users/macbookair13/Google Drive/# Job/00 Study/Python/python_tutorial_official_3.7'




```python
# Change current working directory
#XXXXX os.chdir('/Users/macbookair13/Google\ Drive/#\ Job/00\ Study/Python/python_tutorial_official_3.7/new_folder')
os.chdir('/Users/macbookair13/Google Drive/# Job/00 Study/Python/python_tutorial_official_3.7')

os.system('mkdir today')   # Run the command mkdir in the system shell (cretes a directory)
```




    256


import os
dir(os)help(os)
### `shutil` - file and directory management tasks


```python
import shutil #file and directory management tasks

# myfile.txt -[content copy]-> archive
shutil.copyfile('myfile.txt', 'archive.txt')
```




    'archive.txt'




```python
#today/hello_today folder -[move]-> brand_new folder
shutil.move('today/hello_today', 'band_new')
```


    ---------------------------------------------------------------------------

    Error                                     Traceback (most recent call last)

    <ipython-input-515-fa3c164f7e97> in <module>
          1 #today/hello_today folder -[move]-> brand_new folder
    ----> 2 shutil.move('today/hello_today', 'band_new')
    

    ~/anaconda3/lib/python3.7/shutil.py in move(src, dst, copy_function)
        559         real_dst = os.path.join(dst, _basename(src))
        560         if os.path.exists(real_dst):
    --> 561             raise Error("Destination path '%s' already exists" % real_dst)
        562     try:
        563         os.rename(src, real_dst)


    Error: Destination path 'band_new/hello_today' already exists


## 10.2. List out Files
`glob` module: directory wildcard searches -> file lists 


```python
import glob
glob.glob('*.py')
```

## 10.3. Command Line Arguments
`sys` -  utility scripts often need to process command line arguments
import sys
print(sys.argv)

'''
it sould have printed out:
['demo.py', 'one', 'two', 'three']

instead:
['/Users/macbookair13/anaconda3/lib/python3.7/site-packages/ipykernel_launcher.py', '-f',
'/Users/macbookair13/Library/Jupyter/runtime/kernel-852f43cc-8390-48bd-b941-83df4240ec53.json']
'''import argparse
from getpass import getuser
parser = argparse.ArgumentParser(description='An argparse example.')
parser.add_argument('name', nargs='?', default=getuser(), help='The name of someone to greet.')
parser.add_argument('--verbose', '-v', action='count')
args = parser.parse_args()
greeting = ["Hi", "Hello", "Greetings! its very nice to meet you"][args.verbose % 3]
print(f'{greeting}, {args.name}')
if not args.verbose:
    print('Try running this again with multiple "-v" flags!')
    
'''
usage: ipykernel_launcher.py [-h] [--verbose] [name]
ipykernel_launcher.py: error: unrecognized arguments: -f
An exception has occurred, use %tb to see the full traceback.

SystemExit: 2
'''
## 10.4. Error Output Redirection -> Program Termination
`sys` module

`stdin`, `stdout`, `stderr` attributes


```python
sys.stderr.write('Warning, log file not found starting a new one\n')
```

## 10.5. String Pattern Matching
`re` - [regular expression tools for advanced string processing](https://docs.python.org/3/library/re.html#module-re)
- grammatic correctios
- repeted workd correction in a sentence
- replace works by pattern matching


```python
import re
re.findall(r'\bf[a-z]*', 'which foot or hand fell fastest')
```


```python
re.sub(r'(\b[a-z]+) \1', r'\1', 'cat in the the hat') #
```


```python
#            replace this-[to]->this
'tea for too'.replace('too', 'two')
```

## 10.6. Mathematics

### OTHERS -> [SciPy](https://scipy.org/) , [COOKBOOK](https://scipy-cookbook.readthedocs.io/index.html)
- [NumPy: Base N-dimensional array package](https://numpy.org/)
- [SciPy: Fundamental library for scientific computing](https://scipy.org/scipylib/index.html)
- [Matplotlib: Comprehensive 2D Plotting](https://matplotlib.org/)
- [IPython: Enhanced Interactive Console](http://ipython.org/)
- [Sympy: Symbolic mathematics](https://www.sympy.org/en/index.html)
- [Pandas: Data structures & analysis](https://pandas.pydata.org/)

`math` [module - C library functions](https://docs.python.org/3/library/math.html#module-math)


```python
import math
math.cos(math.pi / 4)
```


```python
math.log(1024, 2)
```

### `random`  [Library - random slections](https://docs.python.org/3/library/random.html#module-random)


```python
import random
random.choice(['apple', 'pear', 'banana'])
```


```python
random.sample(range(100), 10)   # sampling without replacement
```


```python
random.random()    # random float
```


```python
random.randrange(6)    # random integer chosen from range(6)
```

### `statistics` [Library ex.: mean, median, varianc](https://docs.python.org/3/library/statistics.html#module-statistics)


```python
import statistics
data = [2.75, 1.75, 1.25, 0.25, 0.5, 1.25, 3.5]
statistics.mean(data)
```


```python
statistics.median(data)
```


```python
statistics.variance(data)
```

## 10.7. Internet Access

`urllib.request` - [retrieving data from URLs](https://docs.python.org/3/library/urllib.request.html#module-urllib.request)


```python
from urllib.request import urlopen
with urlopen('http://tycho.usno.navy.mil/cgi-bin/timer.pl') as response:
    for line in response:
        line = line.decode('utf-8')  # Decoding the binary data to text.
        if 'EST' in line or 'EDT' in line:  # look for Eastern Time
            print(line)
```

`smtplib` - [sending mail](https://docs.python.org/3/library/smtplib.html#module-smtplib) needs a mailserver running on localhost.
import smtplib
server = smtplib.SMTP('localhost')
server.sendmail('soothsayer@example.org', 'jcaesar@example.org',
"""To: jcaesar@example.org
From: soothsayer@example.org

Beware the Ides of March.
""")
server.quit()
## 10.8. [datetime module](https://docs.python.org/3/library/datetime.html#module-datetime)


```python
# dates are easily constructed and formatted
from datetime import date
now = date.today()
now
```


```python
now.strftime("%m-%d-%y. %d %b %Y is a %A on the %d day of %B.")
```


```python
# dates support calendar arithmetic
birthday = date(1964, 7, 31)
age = now - birthday
age.days
```

## 10.9. Data Compression
directly supported:
- [zlib](https://docs.python.org/3/library/zlib.html#module-zlib)
- [gzip](https://docs.python.org/3/library/gzip.html#module-gzip)
- [bz2](https://docs.python.org/3/library/bz2.html#module-bz2)
- [lzma](https://docs.python.org/3/library/lzma.html#module-lzma)
- [zip](https://docs.python.org/3/library/zipfile.html#module-zipfile)
- [tar](https://docs.python.org/3/library/tarfile.html#module-tarfile)


```python
import zlib
s = b'witch which has which witches wrist watch'
len(s)
```


```python
t = zlib.compress(s)
len(t)
```


```python
zlib.decompress(t)
```


```python
zlib.crc32(s)
```

## 10.10. Performance Measurement
[`timeit`](https://docs.python.org/3/library/timeit.html#module-timeit)


```python
from timeit import Timer
Timer('t=a; a=b; b=t', 'a=1; b=2').timeit()
```


```python
Timer('a,b = b,a', 'a=1; b=2').timeit()
```

## 10.11. Quality Control
`doctest` - [module provides a tool for scanning a module and validating tests embedded in a program’s docstrings.](https://docs.python.org/3/library/doctest.html#module-doctest)


```python
def average(values):
    """Computes the arithmetic mean of a list of numbers.

    >>> print(average([20, 30, 70]))
    40.0
    """
    return sum(values) / len(values)

import doctest
doctest.testmod()   # automatically validate the embedded tests
```

`unittest` - [more comprehensive set of tests to be maintained in a separate file](https://docs.python.org/3/library/unittest.html#module-unittest)


```python
import unittest

class TestStatisticalFunctions(unittest.TestCase):

    def test_average(self):
        self.assertEqual(average([20, 30, 70]), 40.0)
        self.assertEqual(round(average([1, 5, 7]), 1), 4.3)
        with self.assertRaises(ZeroDivisionError):
            average([])
        with self.assertRaises(TypeError):
            average(20, 30, 70)

unittest.main()  # Calling from the command line invokes all tests
```

## 10.12. Other Useful Moduls
`xmlrpc.client` [modules](https://docs.python.org/3/library/xmlrpc.client.html#module-xmlrpc.client)

`xmlrpc.server` [modules](https://docs.python.org/3/library/xmlrpc.server.html#module-xmlrpc.server)
- remote procedure call
- no direct knowledge or handling of XML is needed

`email` [package](https://docs.python.org/3/library/email.html#module-email)
- managing email messages, 
- including MIME and other RFC 2822-based message documents. 
- Unlike smtplib and poplib which actually send and receive messages, 
- the email package has a complete toolset for building or decoding complex message structures (including attachments)
- for implementing internet encoding and header protocols.

`json` [package](https://docs.python.org/3/library/json.html#module-json) 
- parsing this popular data interchange format. 
- csv module supports direct reading and writing of files in Comma-Separated Value format
    - supported by databases and spreadsheets. 
- XML processing is supported by the xml.etree.ElementTree, xml.dom and xml.sax packages. 
- data interchange between Python applications and other tools.

`sqlite3` [module](https://docs.python.org/3/library/sqlite3.html#module-sqlite3)
- wrapper for the __SQLite__ database library, 
- providing a persistent database 
- updated and accessed using slightly nonstandard SQL syntax.

__Internationalization modules__
- [gettext](https://docs.python.org/3/library/gettext.html#module-gettext)
- [locale](https://docs.python.org/3/library/locale.html#module-locale)
- [codecs](https://docs.python.org/3/library/codecs.html#module-codecs)

# [11. Python Advanced Modules II.](https://docs.python.org/3/tutorial/stdlib2.html)
- Support professional programming needs
- These modules rarely occur in small scripts

## 11.1. Output Formatting
`reprlib` - [creates abrecations in Alphabetical order](https://docs.python.org/3/library/reprlib.html#module-reprlib)


```python
import reprlib
reprlib.repr(set('supercalifragilisticexpialidocious'))
```




    "{'a', 'c', 'd', 'e', 'f', 'g', ...}"



`pprint` module
- sophisticated control over printing both 
    - built-in and 
    - user defined objects 
- in a way that is readable by the interpreter. 
- When the result is longer than one line, the “pretty printer” adds line breaks and indentation to more clearly reveal data structure:


```python
import pprint
t = [[[['black', 'cyan'], 'white', ['green', 'red']], [['magenta',
    'yellow'], 'blue']]]

pprint.pprint(t, width=30)
```

    [[[['black', 'cyan'],
       'white',
       ['green', 'red']],
      [['magenta', 'yellow'],
       'blue']]]


`textwrap` - [module](https://docs.python.org/3/library/textwrap.html#module-textwrap) 
- formats paragraphs of text to 
- fit a given screen width


```python
import textwrap
doc = """The wrap() method is just like fill() except that it returns
a list of strings instead of one big string with newlines to separate
the wrapped lines."""

print(textwrap.fill(doc, width=40))
```

    The wrap() method is just like fill()
    except that it returns a list of strings
    instead of one big string with newlines
    to separate the wrapped lines.


`locale` - [module](https://docs.python.org/3/library/locale.html#module-locale) 
- accesses a database of culture specific data formats
- ex.: direct way of formatting numbers with group separators:


```python
import locale
locale.setlocale(locale.LC_ALL, '')
```




    'en_US.UTF-8'




```python
conv = locale.localeconv()          # get a mapping of conventions
x = 1234567.8
locale.format("%d", x, grouping=True)
```

    /Users/macbookair13/anaconda3/lib/python3.7/site-packages/ipykernel_launcher.py:3: DeprecationWarning: This method will be removed in a future version of Python. Use 'locale.format_string()' instead.
      This is separate from the ipykernel package so we can avoid doing imports until





    '1,234,567'




```python
locale.format_string("%s%.*f", (conv['currency_symbol'],
                     conv['frac_digits'], x), grouping=True)
```




    '$1,234,567.80'



## 11.2. Template

### `$` - placeholder: put whatever you want there


```python
from string import Template
t = Template('${village}folk send $$10 to $cause.')
t.substitute(village='Nottingham', cause='the ditch fund')
```




    'Nottinghamfolk send $10 to the ditch fund.'




```python
t = Template('Return the $item to $owner.')
d = dict(item='unladen swallow')
```
t.substitute(d)
Traceback (most recent call last):
  ...
KeyError: 'owner'

```python
t.safe_substitute(d)
```




    'Return the unladen swallow to $owner.'



### Renaming photo batch


```python
import time, os.path
photofiles = ['img_1074.jpg', 'img_1076.jpg', 'img_1077.jpg']
class BatchRename(Template):
    delimiter = '%'
fmt = input('Enter rename style (%d-date %n-seqnum %f-format):  ')
```

    Enter rename style (%d-date %n-seqnum %f-format):   10 10 2019



```python
t = BatchRename(fmt)
date = time.strftime('%d%b%y')
for i, filename in enumerate(photofiles):
    base, ext = os.path.splitext(filename)
    newname = t.substitute(d=date, n=i, f=ext)
    print('{0} --> {1}'.format(filename, newname))
```

    img_1074.jpg --> 10 10 2019
    img_1076.jpg --> 10 10 2019
    img_1077.jpg --> 10 10 2019


## 11.3. Binary Data
[pack()](https://docs.python.org/3/library/struct.html#struct.pack)

[unpack()](https://docs.python.org/3/library/struct.html#struct.unpack)


```python
import struct

with open('myfile.zip', 'rb') as f:
    data = f.read()

start = 0
for i in range(3):                      # show the first 3 file headers
    start += 14
    fields = struct.unpack('<IIIHH', data[start:start+16])
    crc32, comp_size, uncomp_size, filenamesize, extra_size = fields

    start += 16
    filename = data[start:start+filenamesize]
    start += filenamesize
    extra = data[start:start+extra_size]
    print(filename, hex(crc32), comp_size, uncomp_size)

    start += extra_size + comp_size     # skip to the next header
```

    b'archive copy.txt' 0x0 0 0
    b'@\x18\x84\x00PK\x07\x08\x1c\x82l\xe3"\x00\x00\x004\x00\x00\x00PK\x01\x02\x15\x03\x14\x00\x08\x00\x08\x00\x87q0O\x1c\x82l\xe3"\x00\x00\x004\x00\x00\x00\x10\x00\x0c\x00\x00\x00\x00\x00\x00\x00\x00@\xa4\x81\x00\x00\x00\x00archive copy.txtUX\x08\x00\xc7\xe3\x80]\x1d|\x7f]PK\x05\x06\x00\x00\x00\x00\x01\x00\x01\x00J\x00\x00\x00p\x00\x00\x00\x00\x00' 0xcccc8cae 3827305676 55454794



    ---------------------------------------------------------------------------

    error                                     Traceback (most recent call last)

    <ipython-input-527-0fe7e8b76313> in <module>
          7 for i in range(3):                      # show the first 3 file headers
          8     start += 14
    ----> 9     fields = struct.unpack('<IIIHH', data[start:start+16])
         10     crc32, comp_size, uncomp_size, filenamesize, extra_size = fields
         11 


    error: unpack requires a buffer of 16 bytes


## 11.4. Multi-threading | | | |
decoupling NOT sequentially tasks

`queue` - [feeds the therad](https://docs.python.org/3/library/queue.html#module-queue)

`threading` - [run tasks in background while the main program continues to run:](https://docs.python.org/3/library/threading.html#module-threading)


```python
import threading, zipfile

class AsyncZip(threading.Thread):
    def __init__(self, infile, outfile):
        threading.Thread.__init__(self)
        self.infile = infile
        self.outfile = outfile

    def run(self):
        f = zipfile.ZipFile(self.outfile, 'w', zipfile.ZIP_DEFLATED)
        f.write(self.infile)
        f.close()
        print('Finished background zip of:', self.infile)

background = AsyncZip('mydata.txt', 'myarchive.zip')
background.start()
print('The main program continues to run in foreground.')

background.join()    # Wait for the background task to finish
print('Main program waited until background was done.')
```

    The main program continues to run in foreground.
    Finished background zip of: mydata.txt
    Main program waited until background was done.


## 11.5. Logging
flexible logging system

`sys.stderr` log messages sent

Messages: DEBUG, INFO, WARNING, ERROR, and CRITICAL


```python
import logging
logging.debug('Debugging information')
logging.info('Informational message')
logging.warning('Warning:config file %s not found', 'server.conf')
logging.error('Error occurred')
logging.critical('Critical error -- shutting down')
```

    WARNING:root:Warning:config file server.conf not found
    ERROR:root:Error occurred
    CRITICAL:root:Critical error -- shutting down


## 11.6. Weak References
`weakref` [module](https://docs.python.org/3/library/weakref.html#module-weakref) 
- provides tools for tracking objects 
- without creating a reference
- automatic memory management (Python)
- [garbage collection](https://docs.python.org/3/glossary.html#term-garbage-collection)



```python
import weakref, gc
class A:
    def __init__(self, value):
        self.value = value
    def __repr__(self):
        return str(self.value)

a = A(10)                   # create a reference
d = weakref.WeakValueDictionary()
d['primary'] = a            # does not create a reference
d['primary']                # fetch the object if it is still alive
```




    10




```python
del a                       # remove the one reference
gc.collect()                # run garbage collection right away
```




    396




```python
d['primary']                # entry was automatically removed
```




    10



## 11.7. `List` tools
`array` - [moule](https://docs.python.org/3/library/array.html#module-array)
- array() object that is like a list that stores only homogeneous data 
- more compactly
- [array class sub objects](https://docs.python.org/3/library/array.html#array.array)
    - array.typecodes
    - array.typecode
    - array.itemsize
    - array.append(x)
    - array.buffer_info()
    - array.byteswap()
    - array.count(x)



```python
from array import array
a = array('H', [4000, 10, 700, 22222]) #stored as two byte unsigned binary numbers
sum(a)
```




    26932




```python
a[1:3]
```




    array('H', [10, 700])




```python
from collections import deque
d = deque(["task1", "task2", "task3"])
d.append("task4")
print("Handling", d.popleft())
```

    Handling task1

unsearched = deque([starting_node])
def breadth_first_search(unsearched):
    node = unsearched.popleft()
    for m in gen_moves(node):
        if is_goal(m):
            return m
        unsearched.append(m)
`bisect` - [module](https://docs.python.org/3/library/bisect.html#module-bisect)
- manipulate sorted lists


```python
import bisect
scores = [(100, 'perl'), (200, 'tcl'), (400, 'lua'), (500, 'python')]
bisect.insort(scores, (300, 'ruby'))
scores
```




    [(100, 'perl'), (200, 'tcl'), (300, 'ruby'), (400, 'lua'), (500, 'python')]



`heapq` - [module](https://docs.python.org/3/library/heapq.html#module-heapq)


```python
from heapq import heapify, heappop, heappush
data = [1, 3, 5, 7, 9, 2, 4, 6, 8, 0]
heapify(data)                      # rearrange the list into heap order
heappush(data, -5)                 # add a new entry
[heappop(data) for i in range(3)]  # fetch the three smallest entries
```




    [-5, 0, 1]



## 11.8. Decimal Arithmetic

`decimal` - [module](https://docs.python.org/3/library/decimal.html#module-decimal)

`Decimal` - [datatype](https://docs.python.org/3/library/decimal.html#decimal.Decimal)

### Used at:
- financial applications and other uses which require exact decimal representation,
- control over precision,
- control over rounding to meet legal or regulatory requirements,
- tracking of significant decimal places, or
- applications where the user expects the results to match calculations done by hand.

calculating a 5% tax on a 70 cent phone charge gives different results in decimal floating point and binary floating point. The difference becomes significant if the results are rounded to the nearest cent:


```python
from decimal import *
round(Decimal('0.70') * Decimal('1.05'), 2)
```




    Decimal('0.74')




```python
round(.70 * 1.05, 2)
```




    0.73




```python
Decimal('1.00') % Decimal('.10')
```




    Decimal('0.00')




```python
1.00 % 0.10
```




    0.09999999999999995




```python
sum([Decimal('0.1')]*10) == Decimal('1.0')
```




    True




```python
sum([0.1]*10) == 1.0
```




    False




```python
getcontext().prec = 36
Decimal(1) / Decimal(7)
```




    Decimal('0.142857142857142857142857142857142857')



## 11.9. Floating Point Arithmetic
`float` - [module](https://docs.python.org/3/library/functions.html#float)

# [12. Virtual Environments and Packages](https://docs.python.org/3/tutorial/venv.html)
cd /Users/macbookair13/Google\ Drive/#\ Job/00\ Study/Python/python_tutorial_official_3.7/venv_test
## 12.1. Introduction
`venv` - [virtual environment](https://docs.python.org/3/glossary.html#term-virtual-environment)

storring the correct/reaquired/needed version of packages

### Creating Venv
- To create a __virtual environment__
- decide upon a __directory__ where you want to place it
    - create the tutorial-env directory (if it doesn’t exist)
    - create directories:
        - Python interpreter
        - standard library
        - various supporting files
- run the __venv module__ as a script with the directory path:
python3 -m venv venv_test
### Activate/Run
shell Types:
- bash -> .bat file
- csh -> .csh file
- fish -> .fish file
#windows
venv_test\Scripts\activate.bat#Linux & macOS
source venv_test/bin/activate
### After Activation
- change your shell’s prompt 
- to show what virtual -> Wanted Python Version 
$ source ~/envs/tutorial-env/bin/activate
(tutorial-env) $ python
Python 3.5.1 (default, May  6 2016, 10:59:36)
  ...
  
>>> import sys
>>> sys.path
['', '/usr/local/lib/python35.zip', ...,
'~/envs/tutorial-env/lib/python3.5/site-packages']
>>>
## 12.3. `pip` Managing Packager
- mange
- update
- from: https://pypi.org/

### Serch - package
pip search astronomy

skyfield               - Elegant astronomy for Python
gary                   - Galactic astronomy and gravitational dynamics.
novas                  - The United States Naval Observatory NOVAS astronomy library
astroobs               - Provides astronomy ephemeris to plan telescope observations
PyAstronomy            - A collection of astronomy related tools for Python.
...
### Install - package
pip install novas

Collecting novas
  Downloading novas-3.1.1.3.tar.gz (136kB)
Installing collected packages: novas
  Running setup.py install for novas
Successfully installed novas-3.1.1.3
### Install - Specific Version of a package
pip install requests==2.6.0

Collecting requests==2.6.0
  Using cached requests-2.6.0-py2.py3-none-any.whl
Installing collected packages: requests
Successfully installed requests-2.6.0
### Update - Previousely intalled packages to the latest version
pip install --upgrade requests

Collecting requests
Installing collected packages: requests
  Found existing installation: requests 2.6.0
    Uninstalling requests-2.6.0:
      Successfully uninstalled requests-2.6.0
Successfully installed requests-2.7.0
### Uninstall - packages
pip uninstall novas

Uninstalling novas-3.1.1.4:
  Would remove:
### Show info
pip show requests

---
Metadata-Version: 2.0
Name: requests
Version: 2.7.0
Summary: Python HTTP for Humans.
Home-page: http://python-requests.org
Author: Kenneth Reitz
Author-email: me@kennethreitz.com
License: Apache 2.0
Location: /Users/akuchling/envs/tutorial-env/lib/python3.4/site-packages
Requires:
### List - out all installed packages
pip list

Package    Version
---------- -------
pip        19.0.3 
requests   2.6.0  
setuptools 40.8.0 
### Requirements File Create
pip freeze > requirements.txt
### Show - the file's contents
cat requirements.txt
### Install packages - form .txt 
pip install -r requirements.txt

Collecting novas==3.1.1.3 (from -r requirements.txt (line 1))
  ...
Collecting numpy==1.9.2 (from -r requirements.txt (line 2))
  ...
Collecting requests==2.7.0 (from -r requirements.txt (line 3))
  ...
Installing collected packages: novas, numpy, requests
  Running setup.py install for novas
Successfully installed novas-3.1.1.3 numpy-1.9.2 requests-2.7.0
# [13. Python Others](https://docs.python.org/3/tutorial/whatnow.html)
- [ALL Python Modules](https://docs.python.org/3/py-modindex.html)
- [Installing Python Modules](https://docs.python.org/3/installing/index.html#installing-index)
- [Distributing Own New Python Modules](https://docs.python.org/3/distributing/index.html#distributing-index)
- [Heavy Python Grammar](https://docs.python.org/3/reference/index.html#reference-index)
- https://www.python.org: The major Python Web site. It contains code, documentation, and pointers to Python-related pages around the Web. This Web site is mirrored in various places around the world, such as Europe, Japan, and Australia; a mirror may be faster than the main site, depending on your geographical location.
- https://docs.python.org: Fast access to Python’s documentation.
- https://pypi.org: The Python Package Index, previously also nicknamed the Cheese Shop 1, is an index of user-created Python modules that are available for download. Once you begin releasing code, you can register it here so that others can find it.
- https://code.activestate.com/recipes/langs/python/: The Python Cookbook is a sizable collection of code examples, larger modules, and useful scripts. Particularly notable contributions are collected in a book also titled Python Cookbook (O’Reilly & Associates, ISBN 0-596-00797-3.)
- http://www.pyvideo.org collects links to Python-related videos from conferences and user-group meetings.
- https://scipy.org: The Scientific Python project includes modules for fast array computations and manipulations plus a host of packages for such things as linear algebra, Fourier transforms, non-linear solvers, random number distributions, statistical analysis and the like.
- MAILING LSIT: https://mail.python.org/pipermail/ to develope the language python-list@python.org
    - [FAQ](https://docs.python.org/3/faq/index.html#faq-index)

# [14. Code Editor](https://docs.python.org/3/tutorial/interactive.html)
- [__IPython__](https://ipython.org/)
    - A powerful interactive shell.
    - A kernel for [__Jupyter__](https://jupyter.org)
    - Support for interactive data visualization and use of GUI toolkits.
    - Flexible, embeddable interpreters to load into your own projects.
    - Easy to use, high performance tools for parallel computing.
- [bpython](https://bpython-interpreter.org/)
    - In-line syntax highlighting
    - Readline-like autocomplete with suggestions displayed as you type.
    - Expected parameter list for any Python function.
    - "Rewind" function to pop the last line of code from memory and re-evaluate.
    - Send the code you've entered off to a pastebin.
    - Save the code you've entered to a file.
    - Auto-indentation.
    - Python 3 support.

# [15. Float: ERRORS](https://docs.python.org/3/tutorial/floatingpoint.html)
........
#descrbing 0.1 in 2(binary) number system
0.1
0.0001100110011001100110011001100110011001100110011...

```python
format(math.pi, '.12g')  # give 12 significant digits
```




    '3.14159265359'




```python
format(math.pi, '.2f')   # give 2 digits after the point
```




    '3.14'




```python
repr(math.pi)
```




    '3.141592653589793'



Illusion: you’re simply rounding the display of the true machine value.


```python
.1 + .1 + .1 == .3
```




    False




```python
0.1 + 0.1 + 0.1 == 0.3
```




    False




```python
#0.1 cannot get any closer to the exact value of 1/10 and 
#0.3 cannot get any closer to the exact value of 3/10, 
#then pre-rounding with round() function canNOT help:
round(.1, 1) + round(.1, 1) + round(.1, 1) == round(.3, 1)
```




    False




```python
round(.1 + .1 + .1, 10) == round(.3, 10)
```




    True




```python
x = 3.14159
x.as_integer_ratio()
```




    (3537115888337719, 1125899906842624)




```python
x == 3537115888337719 / 1125899906842624
```




    True




```python
#float --[x.hex()]--> hexadecimal
x.hex()
```




    '0x1.921f9f01b866ep+1'




```python
x == float.fromhex('0x1.921f9f01b866ep+1')
```




    True




```python
sum([0.1] * 10) == 1.0
```




    False




```python
math.fsum([0.1] * 10) == 1.0
```




    True



## 15.1. Representation Error
- some (most, actually) decimal fractions cannot be represented exactly as binary (base 2) fractions.
- 1/10 is not exactly representable as a binary fraction.
- IEEE-754 “double precision” = 754 doubles contain 53 bits of precision
- onvert 0.1 to the closest fraction it can of the form `J/2**N` where J is an integer containing exactly 53 bits

....


```python
from decimal import Decimal
from fractions import Fraction

Fraction.from_float(0.1)
```




    Fraction(3602879701896397, 36028797018963968)




```python
(0.1).as_integer_ratio()
```




    (3602879701896397, 36028797018963968)




```python
Decimal.from_float(0.1)
```




    Decimal('0.1000000000000000055511151231257827021181583404541015625')




```python
format(Decimal.from_float(0.1), '.17')
```




    '0.10000000000000001'



# [16. Appendix](https://docs.python.org/3/tutorial/appendix.html)
## 16.1. Interactive Mode
### 16.1.1. Error Handling
### 16.1.2. Executable Python Scripts

- Python scripts can be made directly executable ~ like shell scripts
- (assuming that the interpreter is on the user’s PATH) at the beginning of the script and giving the file an executable mode. The #! must be the first two characters of the file. On some platforms, this first line must end with a Unix-style line ending ('\n'), not a Windows ('\r\n') line ending. Note that the hash, or pound, character, '#', is used to start a comment in Python.
#!/usr/bin/env python3.5
- Windows: no notion of an “executable mode”. The Python installer automatically associates .py files with python.exe so that a double-click on a Python file will run it as a script.
- UNIX/Linux: Script executable mode/permission:
$ chmod +x myscript.py
### 16.1.3. Interactive Startup File
- standard commands executed every time the interpreter is started
- [PYTHONSTARTUP](https://docs.python.org/3/using/cmdline.html#envvar-PYTHONSTARTUP) ~ .profile feature of the Unix shells


```python
import os
filename = os.environ.get('PYTHONSTARTUP')
if filename and os.path.isfile(filename):
    with open(filename) as fobj:
        startup_file = fobj.read()
    exec(startup_file)
```

### 16.1.4. Customization Modules
`sitecustomize`

`usercustomize`

# [Python Setup and Usage](https://docs.python.org/3/using/index.html)


```python

```

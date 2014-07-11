#### Python Syntax

##### Multi-Line Comments
``` python
"""Sipping from your cup 'til it runneth over,
Holy Grail.
"""
```
#### Strings & Console Output

##### Escaping characters
``` python
'There\'s a snake in my boot!'
```
##### String methods
 - `len()`
 - `lower()`
 - `upper()`
 - `str()`

```python
"Ryan".lower()
"Ryan".upper()
str(3.14)
len("roar")
```
##### String Formatting with `%`
``` python
print "The %s who %s %s!" % ("Knights", "say", "Ni")
# This will print "The Knights who say Ni!"
```
#### Date and Time

##### Getting the Current Date and Time

``` python
from datetime import datetime

now = datetime.now()
print now
```
##### Extracting Information

``` python
from datetime import datetime
now = datetime.now()

current_year = now.year
current_month = now.month
current_day = now.day
```

##### Pretty Time

``` python
from datetime import datetime
now = datetime.now()

print '%s:%s:%s' % (now.hour, now.minute, now.second)
```
#### Conditionals & Control Flow

##### And
 - 1 < 2 `and` 2 < 3 is True
 - 1 < 2 `and` 2 > 3 is False

##### This and That (or This, But Not That!)
Boolean operators aren't just evaluated from left to right. Just like with arithmetic operators, there's an order of operations for boolean operators:
 - `not` is evaluated first
 - `and` is evaluated next
 - `or` is evaluated last

##### The Big If
``` python
if this_might_be_true():
    print "This really is true."
elif that_might_be_true():
    print "That is true."
else:
    print "None of the above."
```

#### PygLatin

##### Input!
``` python
name = raw_input("What's your name?")
print name
```

##### Check Yourself... Some More
``` python
x = "J123"
x.isalpha()  # False
```

#### Functions

##### Generic Imports 
``` python
# Ask Python to print sqrt(25) on line 3.
import math

print math.sqrt(25)
```

##### Function Imports
``` python
from module import function

print sqrt(25)
```

##### Universal Imports
``` python
from module import *
```

##### Here Be Dragons

``` python
import math            # Imports the math module
everything = dir(math) # Sets everything to a list of things from math
print everything       # Prints 'em all!
```

``` text
['__doc__', '__name__', '__package__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'hypot', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'trunc']
None
```

##### On Beyond Strings

``` python
def biggest_number(*args):
    print max(args)
    return max(args)
    
biggest_number(-10, -5, 5, 10)    
```

##### Built-in Functions

``` python
maximum = max(1, 1.1, -3.2)
print maximum

minimum = min(-100, 0, 44, 100.3)
print minimum

absolute = abs(-42)
print absolute

print type(4)     # <type 'int'>
print type(4.2)   # <type 'float'>
print type('hello') # <type 'str'>
```

#### Python Lists and Dictionaries

##### Introduction to Lists
Lists are a datatype you can use to store a collection of different pieces of information as a sequence under a single variable name.

##### Late Arrivals & List Length
``` python
letters = ['a', 'b', 'c']
letters.append('d')
print len(letters)
print letters
```

##### List Slicing
``` python
suitcase = ["sunglasses", "hat", "passport", "laptop", "suit", "shoes"]

first  = suitcase[0:2]  # The first and second items (index zero and one)
middle = suitcase[2:4]  # Third and fourth items (index two and three)
last   = suitcase[4:6]  # The last two items (index four and five)
```

##### Slicing Lists and Strings
``` python
animals = "catdogfrog"
cat  = animals[:3]   # The first three characters of animals
dog  = animals[3:6]              # The fourth through sixth characters
frog = animals[6:]              # From the seventh character to the end
```

##### Maintaining Order
``` python
animals = ["ant", "bat", "cat"]
print animals.index("bat")

animals.insert(1, "dog")
print animals
```

##### For One and All

``` python
my_list = [1,9,3,8,5,7]

for number in my_list:
    # Your code here
    print 2 * number
```

##### More with 'for'

``` python
animals = ["cat", "ant", "bat"]
animals.sort()

for animal in animals:
    print animal
```

##### This Next Part is Key

``` python
# Assigning a dictionary with three key-value pairs to residents:
residents = {'Puffin' : 104, 'Sloth' : 105, 'Burmese Python' : 106}

print residents['Puffin'] # Prints Puffin's room number

# Your code here!
print residents['Sloth']
print residents['Burmese Python']
```

##### New Entries
``` python
dict_name[new_key] = new_value
```

##### Changing Your Mind

``` python
del dict_name[key_name]

dict_name[key] = new_value
```

##### Remove a Few Things
``` python
beatles = ["john","paul","george","ringo","stuart"]
beatles.remove("stuart")
print beatles
>> ["john","paul","george","ringo"]
```

##### It's Dangerous to Go Alone! Take This
``` python
my_dict = {
    "fish": ["c", "a", "r", "p"],
    "cash": -4483,
    "luck": "good"
}
print my_dict["fish"][0]
```

#### A Day at the Supermarket
##### This is KEY!
``` python
# A simple dictionary
d = {"foo" : "bar"}

for key in d: 
    print d[key]  # prints "bar" 
```





















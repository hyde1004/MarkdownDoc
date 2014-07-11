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

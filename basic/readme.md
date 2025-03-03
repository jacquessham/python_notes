# Basic
Coming soon...

## Basic Syntax
Coming soon...

### List Syntax
```
list1 = [1,2,3,4]

# One line Filtering
list2 = [num for num in list1 if num%==1 else] # If only
list2 = [num if num%2 else None for num in list1] # If-else

# Replace element in place
nums = [1,2,2,3,4]
nums[:] = sorted(set(nums)) # [1,2,3,4,_]

```

## Environment
Coming soon...
<br><br>
Create a virtual environment:

```
python3 -m venv (env_name)
```

<br>
It would create a virtual environment and a folder contains all the files.
<br><br>
To activate a virtual environment, change the directory to the environment folder and execute:

```
source (env_name/bin/activate)
```

<br>
To deactivate the virtual environment:

```
deactivate
```

## datetime

```
from datetime import datetime

# Declare datetime object - year, month, day, hour, minute, second
a = datetime(2024,1,5,10,00,00)
b = datetime(2024,1,10,12,30,00)
c = datetime.now()

difference = b - a

difference # Output: 5 Days, 2:30:00

# To obtain only the day portion
difference.days

# To obtain only the second portion
difference.seconds

# To obtain the difference in total seconds
difference.total_seconds()

```

## Collections
### Counter
Counter accepts a list or a string
```
lst1 = Counter([1,2,2,3,4,5,6,6,6]) # Counter({6:3, 2:2, 1:1, 3:1, 4:1, 5:1})
str1 = Counter('bell') # Counter({'l':2, 'b':1, 'e':1})
```

<br>
Accessing counter like dictionary:

```
lst1[6] => 3 # k=6 , v=3
```

<br>
Updating counter means adding more elements to the object:

```
lst1.update([1,1,1]) # Becomes -> Counter({6:3, 2:2, 1:4, 3:1, 4:1, 5:1})
```

<br>
most_common() is the most useful method: It sort the elements by the most frequency to the least, and return a list of (key, frequency) tuples.

```
print(lst1.most_common(1)) => [(1, 4)]
print(lst1.most_common()) => [(1, 4), (6, 3), (2, 2), (3, 1), (4, 1), (5, 1)]
```

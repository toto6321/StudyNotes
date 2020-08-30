# Python





## Data Type

### Built-in Data Types

| Category | Date Type |
| -------- | --------- |
| Text Types | str |
| Number Types | int, float, complex |
| Binary Types | bytes, bytearray, memoyview |
| Sequence Types | list, tuple, range |
| Mapping Types | dict |
| Set Types | set, frozenset |
| Boolean Types | bool |





### Get Data Type

```python
x=5
type(x)
```



### Set Data Type

| Example (Implicit Data Type Assignment) | Explicit | Data Type |
| ------- | --------- | --------- |
|x = 'hello'|str('hello')|str|
|x = b'hello'|bytes('hello', encoding='utf8')|bytes|
|x = bytearray(5)|bytearray(5)|byetarray|
|x = 20|int(20)|int|
|x = 20.0|float(20.0)|float|
|x = 1j|complex(1j)|complex|
|-|range(6)|range|
|x = [1, 2, 3]|list((1,2,3))|list|
|x = (1, 2, 3)|tuple((1,2,3))|tuple|
|x = {'name': 'John', 'age': 20'}|dict(name='John', age=20)|dict|
|x = {1, 2, 3}|                                 |            |
| -                                       |fronzenset((1, 2, 3))|fronzenset|
|x = True|bool(1)|bool|
|-|memoryview(bytes(5))|memoryview|



##  API

### List

```python
array = list(range(5))

# list.append(element)
# add an item to the end
array.apend(5) #
# [0,1,2,3,4,5]

# list.insert(index, element)
array.insert(0, -1) #
# [-1,0,1,2,3,4]

# list.remove(element)
# remove the first item from the list
array.remove(4) #
# [0,1,2,3]

# list.pop(index)
# Remove the item at the given position in the list, and return it.
array.pop(0) # 0
# [1,2,3,4]

# list.extend(iterable)
array.extend([5,6,7,8]) #
# [0,1,2,3,4,5,6,7,8]

# list.clear()
# remove all elements, equivalent to `del array[:]`
array.clear()
# []

# list.index(element)
# return the index of the first item whose value is euqal to element
array.index(1) # 1
# [0,1,2,3,4]

# list.count(element)
# Return the number of times element appears in the list.
array.count(1) # 1
# [0,1,2,3,4]

# list.sort(key=None, reverse=False)
# Sort the items of the list in place
array.sort(reverse=True) #
# ［4,3,2,1,0]

# list.copy()
# Return a shallow copy of the list. Equivalent to a[:]
b = array.copy() # b=[0,1,2,3,4]
array.pop() # 4
# array=[0,1,2,3]; b=[0,1,2,3,4]

```





### String

```python
s = 'Python is great'

s.find()
s.rfind()
s.index()
s.rindex()
s.split(sep=None, maxsplit=-1)
s.rsplit(sep=None, maxsplit=-1)
s.splitlines()
s.strip([char])
s.rstrip([char])
s.partition(sep)
s.replace(old, new, count)
s.count(substring, start, end)
'[char]'.join()

s.startswith(prefix, start, end)
s.endswith(suffix, start,end)


s.isnumeric()
s.isdigit()
s.isdecimal()
s.isalnum()
s.alpha()
s.isidentifier()

s.islower()
s.isupper()

s.lower()
s.upper()
s.swapcase()

s.istitle()
s.title()
s.capitalize()


```


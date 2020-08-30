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


## Mathematics operator

### Division

```python
15 / 3		# 5.0 always return float
17 // 3		# 5 정수 부분만 반환
```

## Interactive Mode (대화형 모드)

### _

```python
>>> 1 + 3
3
>>> _
3
>>> tax = 2
>>> _
3
```

## String

### Raw String

```python
>>> print('C:\some\name')  # here \n means newline!
C:\some
ame
>>> print(r'C:\some\name')  # note the r before the quote
C:\some\name
```

### Multiline String

```python
'''
multi\
line
string
'''
# '\nmultiline\nstring\n', to escape '\n' use '\'
```

### Auto Concat

```python
'this ' 'will' ' be ' 'merged'		# 'this will be merged'
```

### Immutable

```python
word = 'word'
word[0] = 'k'		# TyeError: 'str' object does not support item assignment
word = 'k' + word[1:]
```

## List

### shallow

```python
a_list[:]
```

### Mutable

```python
abc = [1,2,3,4,5,6,7,8,9]
abc[2:5] = [1,2,3,4,5]
# [1,2,1,2,3,4,5,6,7,8,9]
```

## Control Flow

### Change list in for

```python
for w in words[:]:
    words.append('HI')
```

### for else

```python
for i in range(10):
    # do something here
else:
    # reach when does not break above
```

### default value shared

```python
def func(a, l=[]):
    l.append(a)
    return l

func(1)		# [1]
func(2)		# [1,2]
```

### function *arguments, **keywords

```python
def cheeseshop(kind, *arguments, **keywords):
    print("-- Do you have any", kind, "?")
    print("-- I'm sorry, we're all out of", kind)
    for arg in arguments:
        print(arg)
    print("-" * 40)
    for kw in keywords:
        print(kw, ":", keywords[kw])
```

```python
cheeseshop("Limburger", "It's very runny, sir.",
           "It's really very, VERY runny, sir.",
           shopkeeper="Michael Palin",
           client="John Cleese",
           sketch="Cheese Shop Sketch")
```

```
-- Do you have any Limburger ?
-- I'm sorry, we're all out of Limburger
It's very runny, sir.
It's really very, VERY runny, sir.
----------------------------------------
shopkeeper : Michael Palin
client : John Cleese
sketch : Cheese Shop Sketch
```

### parameter unpacking

```python
# unpack list or tuple
range(*[3,6])
range(3, 6)
# unpack dictionary
func(p1=1, p2=2)
func(**{'p1':1, 'p2':2})
```



## References

https://docs.python.org
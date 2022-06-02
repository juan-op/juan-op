# Basics

# Types of data

* Strings:
```python
"Words"
```
* Integers:
```python
1, 2, 3...
```
* Floats:
```python
1.5, 1.8, 2.5...
```
* Booleans:
```python
True
False
```

# Math operators

* Exponent: **
* Modulus: %
* Integer division: //
* Division: /
* Multiplication: *
* Subtraction: -
* Addition: +

# Logical operators

* Equal to: ==
* Not equal to: !=
* Less than: <
* Greather than: >
* Less than or equal to: <=
* Greater than or equal to: >=
* `and`
* `or`

# Basic functions

* Print:
```python
print()
```
* Input:
```python
input()
```
* Length:
```python
len()
```
* Type conversion:
```python
str()
int()
float()
```

# Conditional statements

* If:
```python
if name == 'Alice':
    print('Hi, Alice.')
```
* Else:
```python
name = 'Bob'
if name == 'Alice':
    print('Hi, Alice.')
else:
    print('Hello, stranger.')
```
* Elif:
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
* Ternary operator:
```python
age = 30
name = 'Bob' if age == 30 else 'Alice'
```
# Loops

* For loops:
```python
for i in range(10):
    print(i)
```

* While loops:
```python
spam = 0
while spam < 5:
    print('Hello, world.')
    spam = spam + 1
```

* Break and continue:
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


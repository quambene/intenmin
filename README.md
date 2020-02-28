# XYZ in under 10 minutes

Concise tutorials and summaries for developers in less than 2380 words.

#### Contents

[Python](#python)

## Python

### Print

```python
name = "world"
print(f"Hello, {name}!")
print("This %(verb)s a %(noun)s." % {"noun": "test", "verb": "is"})
```

### Variables

```python
x: int # Declare type
x = 4 # Assign value
x: int = 4 # Assign value (typed)
x = y = z = 0 # Multiple assignment
x += 1 # Increment
x -= 1 # Decrement
```

### Data types

```python
# List
x = ["item1", "item2", "item3"]
x: List[str] = ["item1", "item2", "item3"] # typed
x[0:3] # Indexing is inclusive-exclusive
x[-3:-1] # Negative indexes count from the last item backwards

# Tuple
x = (1, 2, 3)
x: Tuple[int, int, int] = (1, 2, 3) # typed

# Dictionary
x = {"key1": 1, "key2": 2}
x: Dict[int, int] = {"key1": 1, "key2": 2} # typed

# Option
x: Optional[str] = some_function()
```

### Control flow

```python
# for loop
for i in range(10):
    print(i)

# while loop
while i < 3:
    print(i)

# if-else
if a < b:
    # statement
elif a == b:
    # statement
else:
    # statement
```

### Functions

```python
def my_function(arg, optional_arg = 'default value'):
    return arg, optional_arg

# Typed function
def my_function(arg1: int, arg2: int) -> Tuple[int, int]:
    return arg1, arg2

# Lambda function
add_one = lambda x: x + 1
```

### Classes

```python
class MyClass:
    instance_var = 100

    def __init__(self):
        self.my_variable = 3

    def my_function(self, arg1, arg2):
        return self.my_variable

# Instantiation
class_instance = MyClass()
class_instance.my_function(1, 2)
```

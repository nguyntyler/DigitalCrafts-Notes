# **Sequences**

A sequence is a data type that stores multiple values.
    
    - List
    - Strings
    - Tuples

# Lists

Lists are ***mutable***, meaning they are able to be changed. They tend to be more versatile and general-purposed.

Lists can hold any type of data type (strings, numbers, other lists).

```Python
todo = ["pet the cat", 5, ["do one", "do two"], "sleep"]
```
This is a ***list literal***. It:

- Contains one or more values.
- Is separated by commas.
- Enclosed in brackets.

You can access certain values in the sequence by calling on its ***index***. The first index always start at 0.

```Python
print("First item: ", todo[0])
# Prints "pet the cat"
```

Trying to call on a non-existing index will result in an ***index error***.

You can also call on an index with negative numbers. They start at -1 and will call the last item first.

```Python
print("Last item: ", todo[-1])
# Prints "sleep"
```

***Slicing*** occurs when you want to access a portion of a list.
```Python
print("A few: ", todo[1:3])
# Prints 5, ["do one", "do two"]
```
The first number indicates the starting number. It is included in the print statement.

The second number indicated the stop number and is not included in the print statement.

```Python
print(todo[:3])
# Prints from index 0 to the sub list.
print(todo[2:])
# Prints from the sub list to the end.
```

Empty indexes will print either starting from the beginning or to the end. Using negative numbers will do the opposite.

# Iteration
It is possible to access each item in a list automatically. This is done through loops.

If using a while loop, an easy way to prevent infinite looping is through the ***len()*** function.

```Python
todo = ["pet the cat", 5, ["do one", "do two"], "sleep"]

index = 0
while index < len(todo):
    todo = todo[index]
    print("%d: %s" % (index + 1, todo))
    index +=1
```

***For loops*** offer another way to iterate through the list. However, this type of loop only grabs a specific item at a time. 

```Python
for i in todo:
    print(i)
```
This will print out each indiviual item of todo as it passes through them.

# Modification
There are only three ways to add to a list:

- .append()
- Concatenation
- .extend()

### Append
Adds an item to the end of the list.
### Concatenate
Combines two lists together.
### Extend
Does the same thing concatenate does but in a method.

> When you concatenate, you produce a new list. This means you must assign it to a variable in order to use it again.

> Append and extend modifies the original list and doesn't return a new list.
___
To replace an item in a list, you need to refer to a specific place in the list with the index.

```Python
todo[1] = "eat"
```
This modifies the second item in the list to now read "eat".

If you try to replace multiple items:
```Python
todo[1:4] = 1, 2
```
Python will delete three items and replace it with 2 items. 

To manually delete an item, do:
```Python
del todo[1:3]
```
This deletes all items from index 1 to 2.

# Nested Loops
You can have lists inside lists.
```Python
nest_list = ["apple", ["fiji", "granny smith"], "banana"]
```
To access "fiji" you must do:
```Python
print(nest_list[1][0])
```

With nested loops, you can create numbers that read the value of other numbers.
```Python
size = 2

for x in range(size):
    for y in range(size):
        print(y, x)
```
Range returns integers that go up to but not including that number.
```
0 0
0 1
1 0
1 1
```
___
## Strings as a Sequence
You can index, slice and get the length of a string just like a list.
```Python
letters = "abcdefghijklmnopqrstuvwxyz"

print(letters[0])
print(letters[:4])
print(letters[5:11])
print(len(letters))
```
All of these commands work for the string and will return a value of some sort.

And as such, can be iterated through as well.
```Python
for letter in letters:
    print(letter)
```

This will print each letter one by one.

One big difference is that strings cannot be changed like a list. Certain indexes can be changed in list but not in a string. 

Doing...
```Python
letters[0] = 1
```
...will result in a type error.
> TypeError: 'str' object does not support item assignment

There is a function that does allow you to change a string into a list:
```Python
letterlist = list(letters)
letterlist[0] = "1"
letterlist = "1", "b", "c", "d", "e", etc.
```

To turn a list back into a string, you need to use the .join() method.

```Python
letters = "".join(letterlist)
```
The .join() method reconnects the items of a list.

The empty string "" allows the items to be reconnected without a space inbewteen.

While this does look like we mutated the original variable, the .join() method created a whole new variable.

# Tuples
Just like with strings, you can slice, index, and get the length of a tuple. However, you cannot modify it. 

Tuples are indicated by a () instead of a [].

```Python
number = (101, 404, 909)

print(number[1])

# 404
```
Trying to change an index of a tuple will result in a TypeError
> TypeError: 'tuple' object does not support item asssignment

While this is true, you can either remove or add onto the tuple to create a new tuple. 
```Python
number = number[:-1] # All but the last.

number = number + "000"
```
Each of these reassigns the variable a new data type. 
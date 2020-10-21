# Function
Functions allow for repeated actions without rewriting them.

```Python
def my_func():
    print("I am a function")

def add_numbers():
    num1 = 10
    num2 = 20
    num3 = num1 + num2
    print(num3)
```

Functions are indicated by the ***def*** command. This creates a new function with the name that's given after it. The code block inside the new function is what will run when one ***calls*** the function. You call the function by writing:
```Python
my_func()

add_numbers()
```
This will run each of the functions and return:
> I am a function
> 30
___
### Return
***Return*** Is the value that the function sends out of a result of calling that function.
```Python
def add_nums(a, b):
    result = a + b
    return result

def multi_nums(a, b):
    return a*b
```
Without the return, the function **add_nums()** will not do anything when called.
```Python
num1 = add_nums(1, 4)
print(num1)

print(multi_nums(3, 3))
```
This is what you would have to do to see the value or the result.

Do note that return exits the function.

This works when trying to create a dictionary.
```Python
def make_dictionary(first, last, age):
    return{
        "FirstName": first,
        "LastName": last,
        "Age": age
    }

tyler_data = make_dictionary("Tyler", "Nguyen", 24)

for key in tyler_data:
    print(key, tyler_data[key])
```
# Scope
***Global scope*** Variables in this global scope can be used anywhere.
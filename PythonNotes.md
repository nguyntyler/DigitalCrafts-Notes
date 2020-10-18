# Python Notes
```Python
print("Hello world!")
```
Expression is ["Hello world!"].

Statement is [print("Hello world!")]
```Python
message = "Hello world!"
```
___
## **Variables**
Assigning a data type to a variable.

Python reads from top to bottom. So:
```Python
age = 30
print(age)
age = 40
print(age)
```
The first print would output 30 but the second would output 40. Variables can change.
```Python
age1 = 10
age2 = 20
total_age = age1 + age2
print(total_age)
age2 = 40
print(total_age)
```
Both the first and second print would be 30. total_age has not changed since the age2 has been changed.
___
## **Numbers**
Numbers can be assigned to a variable and used that way to evaluate mathematical problems.
```python
a = 10
a += 2

b = 10
b -= 2
```
This is an incrementer and a decrememter. It takes whatever value a or b is at the moment, adds or subtracts it by however much you input (in this case 2) and returns the value.

```
a += b
```

This itself is a statement. 

```Python
print(a += b)
```
This would not work because the print function cannot run a statement. It needs an expression. a += b does not return a value but rather assigns a value to a variable.
___
## **Strings**
A ***literal*** string is a value that is not a variable.

A ***concatenation*** is a joining of two or more strings. (With a +)

To span multiple lines, use triple quotes:
```Python
'''
I
Am
Here.
'''
```
Triple double quotes work as well.

Ways to combine strings:
> Using + or , :
```Python
print("Hello", person + ",I hope that your", today,"is going well. I'm personally really", emotion, ".")
```
> Using Interpolation :
```Python
print("Hello %s,\nI hope that your %s is going well.\nI'm personally really %s." %(person, today, emotion))
```
> Using Formatting :
```Python
print(f"Hello {person},\nI hope that your {today} is going well.\nI'm personally really {emotion}.")
```
Special characters can be used to customize your strings :

    \n  - Creates a new line.
    \t  - Creates a tab.
___
## **Comparisons and Booleans**
***Booleans*** are either True or False.

***Code blocks*** are sections of code that runs should an if-statement runs True.


|Comparison Operators |  |
|-----|-|
| ==  | Equals to. |
| <   | Less than. |
| >   | Greater than. |
| <=  | Less than or equal to. |
| >=  | Greater than or equal to. |
| !=  | Not equal to. |

With if-statements, code inside a code block will run if the statement returns true.
```Python
if 0 == 0:
    print("This will print.")

if 0 == "Hello":
    print("This will not print.")
```
___
## **User Input**

***Code blocking*** occurs when the terminal waits for further instructions before continuing the code. Usually after the user asks for an input.

Input often returns whatever the user inputs as a string. If you need to use the input as another data type, you must ***type cast***.

```Python
age = int(input("What's your age?"))

a = "10" #This is a string.

int(a) #This converts the string to an integer.
```
___
## **Nesting & Conditionals**
Coding inside code.
```Python
pet_name = input("What is your pet's name?\n> ")
if len(pet_name) < 3:
    print("That name is too short.")
elif len(pet_name) > 3:
    print(f"Aww, sweet {pet_name}!")

    if pet_name == "Shadow":
        print("El gato diablo!")
    elif pet_name == "Daisy":
        print("Good dog!")
else:
    print("That's as short as 'Tom'.")
```
|Conditional Operators    |     |
|-----------|-|
| and        | Both conditions must be true. |
| or         | Checks for the first Truthy condition. |
| not         | Makes a Truthy condition Falsey and vise-versa. |

These operators also work alongside comparison operators.
___

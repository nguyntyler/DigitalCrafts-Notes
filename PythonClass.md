# Classes
Classes are a type of functions that act like a blueprint.

To create a class:
```Python
class Person:
    pass
```
***Pass*** causes the function to continue on. It's a way to not have any code in the code block and have it not error out.

To use a class:
```Python
tyler = Person()
```
This is call ***instantiation***. You create a copy of something using the blueprint provided by the class function.

```Python
class Person:
    def __init__(self):
        print("You created a new instance of Person.)
```
The print function only runs when you create an instance of Person. It doesn't run when you act on the instatiation. 

The ***self*** parameter can be anything. It is considered the standard. It's the first parameter that's is called on in python. When you print it, it refers to a location in memory.

Through the self referral, you can include other attributes to refer to the instantiation or the "self".
```Python
class Person:
    def __init__(self):
        print("You created a new instance of Person.)
        self.name = "Tyler"
        self.age = 24
tyler = Person()

print(tyler.age)
```
The problem with this is that all new instatiations will have the **self.name** of "Tyler". To make this dynamic:
```Python
class Person:
    def __init__(self, name, age):
        print("You created a new instance of Person.)
        self.name = name
        self.age = age
```
___
### Class Methods
```Python
class Mob:
    def __init__(self, name, health=10):
        self.name = name
        self.health = health
    def get_hit(self, dmg):
        print(f"I was hit for {dmg} points")

hero = Mob("Shera", 30)

hero.get_hit(3) # This will run the print function. "I was hit for 3 points.
```
Methods can be modified.
```Python
    def get_hit(self, dmg):
        self.health = self.health - power
        print(f"I was hit for {dmg} points")
    def attack(self, enemy):
        enemy.get_hit(self.power)
```
___
### Class Inheritance
If you wanted to use the attributes of one class in another, you can have the new class ***inherit** the old class.
```Python
class Mob:
    def __init__(self, name, health = 10, attack_power = 2):
        self.name = name
        self.health = health
        self.attack_power = attack_power 

    def get_hit(self, power):
        self.health = self.health - power            

    def attack(self, enemy):           
        enemy.get_hit(self.attack_power)

class Hero(Mob):
    pass

good_guy = Hero("Tyler")

good_guy.name # Outputs "Tyler"
```

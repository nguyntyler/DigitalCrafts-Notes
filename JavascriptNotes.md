# Variables
Before, you had to declare a variable with 'var' and ending with a ';'.
```javascript
var a;
a = 10

var b = 11
```
Technically you can just assign a variable without the var but it's bad practice.

var allows you to change a variable that's inside a function. let doesn't allow you to do that.

let is the modern way to assign variables that has more specificity.
```javascript
let a = 2

const b = 33
```

const creates a variable that cannot be touched again. Because of this, you must assign it to a value right away. Doing const c by itself does not work and will result in an error.

You can format string
```javascript
let a = 100
let b = 130
let myTemplate = `${a} is great ${b} is better`
```

Javascript also has index that starts at 0.
```javascript
myTemplate[1] 
// Would equal 0.
myTemplate[4]
// Would equal i.
```
When you try to add anything to a string, it registers the other value as a string and literally adds it to the string.

# Operators
```javascript
let a = 10

a == 10 //True
a == '10' //Also true. Due to coercion.
```

> $$ means and.
> || means or.

# Conditions
**If statements**
```javascript
let a = 10, b = 20, c = 30

if(a === 10 && b == 10){
    console.log('a is actually 10')
} else {
    console.log('One of these are not true.')
}
```
Indention does not matter. For conditional statements, the condition must be inside the parenthasis. 

Javascript does not have an elif. They only have the else then another if conditional.
```javascript
if(a === 10){
    console.log('a is actually 10')
} else if(b == 10){
    console.log('a is less 10')
} else {
    console.log('One of these are not true.')
}
```

# Ternary
```javascript
let a = 10
a == 10 ? 'yes!' : 'no'


if(a == 11){
    result = 'yes'
} else {
    result = 'guess again'
}
```
If we are trying to get one value out of an if else statement, a ternary operator is more ideal.

```javascript
if(a > 5) console.log("yes. it's more than 5")

// is the same with or without the brackets.
```
# Switch
Good if we have multiple if statements and we are comparing it to a value.
```javascript
let a = 10

  switch (a) {
      case 20:
          console.log('a is 20')
          break;
      case 15:
          console.log('a is 15')
          break;
      case 10:
          console.log('a is 10')
          break;
      default:
          console.log("I really don't know")
  }
```
You need breaks. Otherwise, it will keep finding true statements, print them.

# Loops
```javascript
let i = 5;
while(i < 10){
    console.log(i)
    i++
}

console.log(i)
while(i > 0){
    console.log(i)
    i--
}
```
While loops are less often used. 

```javascript
for(let i = 0; i < num; i++){
    console.log(i)
}

let i = 1
for(; i < 20;){
    console.log(i)
}

for(let i = 0; i < 20; i ++){
    if(!(i % 2)) {
        continue;
    }
    console.log(i)
}
```
# Functions
They are similar to Python in that you do
```javascript
function myFunc(){
    -code block-
}

// ----------

function myFunc(myName){
    return(`I, ${myName} have returned`)
}
let result = funcName("Clint", "this is dumb", 2)

console.log(result)

// -----------

function ff(bar1, bar2, bar3){
    if(!bar3) bar3 = 0
    bar3 = bar3 || 0
    return bar1 + bar2 + bar3
}
console.log(foo(1,2))
```
Javascript loads all the functions first before running script. Unlike Python, js can run a function before it's declared.

Anon functions can be used inside other functions.
<!-- first anon -->

```javascript
const myFunc = function(someArg){
    console.log('Im anon', someArg)
}

function hasArgFunc(argFunc, passArg){
    console.log('I have a function as an arg')
    argFunc(passArg)
}

hasArgFunc(myFunc, 'This is amazing')
```
We set a blueprint for a function that inputs our args to run another set function.
```javascript
function hasArgFunc(argFunc, passArg){
    console.log('I have a function as an arg')
    argFunc(passArg)

hasArgFunc(function(myArg){
    console.log('This is going to happen a lot.')
    console.log('my arg is '+myArg)
}, 'This is amazing')
```

```javascript
function foo(bar){
    bar()
}

foo(function(){
    console.log('print foo, bar')
})

foo(()=>console.log('do something'))
```
# Arrays
They function the same way as lists in Python.
```js
let myArr = ['a', 'b', 'c', false, 0]

console.log(myArr[0])
// outputs 'a'
```

In Python, we had the .append method to add stuff to the end of a list. In JS, we have .push.

> myArr.push('d')

To remove the last item, we do .pop. However, this also returns a value.

> let removed = myArr.pop()

This means we can assign the removed item to a variable.

To affect the beginning of a list by adding, we do .unshift.

> myArr.unshift('z')

Removing from the beginning uses .shift.

> myArr.shift()

```js
let anothArr = ['a', 'b', 'c', 'd']

for(let i = 0; i < anothArr.length; i++){
    console.log(anothArr[i])
}
```
This is the same as the for loops we were doing before. The .length sets the length of the list to a value. This is old, but still viable.

The modern way is using a for-each:

```js
anothArr.forEach(function(letter, idx){
    console.log(letter, idx)
})
```
forEach has preset parameters. The first argument, which is letter, is each item in the list. The second is the index (can be any word) that lists the index.

# Objects
### **As Dictionaries**
In JS, objects are literal instances of the root object of JS.

```js
let myObj = {}

let newObj = {
    name:'Tyler',
    age:24,
    tall:false,
}
```
In JS, dictionaries will automatically turn everything into a string. The key also does not need to be in quotations like Python.

You can also call on it like Python.

```js
console.log(newObj[name])
```

However, in JS you can also call on it like a method. Which is the standard way.

```js
console.log(newObj.name, newObj.age)
```

To change a value, you do:

```js
newObj.name = 'Tyler Nguyen'

newObj.name += ' Okurr'
```

You can add a new key:value pair:

```js
newObj.gender = Male
```

To remove a pair:

```js
delete newObj.tall
```

```js
for(foo in newObj){
    console.log(foo)
    console.log(newObj[foo])
}
```
This is a way to show the key value pair. When you do the for loop, you get the key in the dictionary. This is foo.

```js
for(foo in newObj){
    if(!newObj.hasOwnProperty(foo)) continue;
    console.log(foo, newObj[foo])
}
```
The if statement checks to see if something exists. If it doesn't, it continues. This is the correct way to loop through an object.

# Arrays of Objects

```js
let people = [
    {
        name:'tyler',
        age:24,
    },
    {
        name:'tony',
        age:23,
        gender:'male',
    }
]

console.log(people[0].name)

people.forEach(function(person){
    console.log(person.name+' is'+person.age+' years old.')
})
```

# More Objects

Everything is an object in JS. When you use the 'new' function, you instantiate whatever you are 'new'ing.

```js
console.log(typeof 'yes')
console.log(typeof new String('yes'))

let myString = 'yes'
let anotherString = new String('yes')

console.log(myString, myString.length)
console.log(anotherString, anotherString.length)
```
They both output the same thing but anotherString outputs as an object. 

new String creates an instance of the string 'yes'.

```js
new String('yes') instanceof Object
// True
new String('yes') instanceof String
// True
```

Functions are also objects. To make an instance of a function and make the instance a type of object:

```js
function Animal() {}
let rainbow = new Animal()


rainbow instanceof Object
// true
```

```js
function Animal (type, name, noise) {
    this.name = name;
    this.type = type;
    this.noise = noise
    this.makeNoise = function(){
        console.log(this.name+' says '+this.noise)
    }
}

let shadow = new Animal('cat', 'shadow', 'GROWWWL')
// shadow now is {name: 'shadow', type: 'cat', noise: 'GROWWWL'}
// You can now do
console.log(shadow.name)
// shadow
shadow.makeNoise()
// shadow says GROWWWL

for(att in shadow){
    console.log(att)
}
// name
// type
// noise
// nameNoise
```
This pattern is mostly for JS based video games. Not the standard for front-end.

JS is based on prototypes. Not raw inheritence. Prototype is an object carried within an object. 

```js
Animal.prototype.makeNoise = function(){
    console.log(this.name+' says '+this.noise)
}

for(i in shadow){
    console.log(i)
}
// shows makeNoise() which is a problem because makeNoise() is part of the prototype.

for(i in shadow){
    if(!shadow.hasOwnProperty(i)) continue;
    console.log(i)
}
// now outputs everything shadow does in the above example.
```
___
```js
let myArr = [1, 2, 3, 4, 5]

myArr.forEach(function(n){
    console.log(n)
})
// forEach is done on the instance of the array myArr. Not on the array itself.

myArr.reverse()
// [5, 4, 3, 2, 1]

myArray.isArray()
// Error. myArr.isArray is not a function.

Array.isArray('test')
// false
Array.isArray(myArr)
// true
```

The math object is done on the actual math object itself. That's why it doesn't have any .prototype.

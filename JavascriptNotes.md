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

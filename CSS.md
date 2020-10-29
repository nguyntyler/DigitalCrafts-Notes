# Cascading Style Sheet
Signified by a name of the element. Followed by curly brackets that will house the CSS styles. 

In the brackets are declarations. Property and value. Separated by colons. Ends with a semicolon.

***Selector Types***

```CSS
a {
    font-weight: bold;
    background: blue;
}
div {
    text-decoration: underline; color:rgb(10,20,30);
    font-size: 2px;
}
.content-item {
    color:#33ddff;
}
```
You should not use id as a selector because it will only modify one thing since you can only have one id.

***Pseudo Selector***
```CSS
.nav-item:hover {
/* insert css */
}
```
This affects the element more specifically.
___
## Specificity
**Inheritance** - In css terms, Inheritance is how elements are styled when not directly selected. The inheritance order is parent -> User Angent (Browser default) -> Selected via selector

**Specificity** - In CSS, specificity refers to how specific the selector is. If there is more than one selector that can impact an element, declerations from less specfic will be overwritten by more specific. Specificy goes in the order tag->class->psudo-class->id.
___
## Box Model
A webpage is divided into separate "boxes" that encapsulates each other like russian dolls.

Margin > Border > Padding > Content
___
## Position

Static : Default.

Fixed : Based on the screen and not the document position.

Absolute : Takes the element out of the flow. Not always recommended.

Relative : Can be moved with other declarations.

Sticky : Based on the document but stays on the screen.
___
## Flexbox
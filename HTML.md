# HTML

Meant to only have text. No design.

```html
<!-- Comment -->

<div> Tags that allow for content. </div>
```
HTML comments are very rarely used in final product.

Tags do not show up in final product.

Even though tags don't affect the final layout, semantics matter. 

```html
<div>
    <p>
        a nested paragraph
    </p>
    <p>
        another nested paragraph number 2
    </p
</div>
```
Tags can exist within tags for organization.

```html
<ul>
    <li> peas </li>
</ul>
<ol>
    <li> carrots </li>
</ol>
```

```html
<a href="https://google.com">Goto Google</a>
```
This is a link. It uses an anchor tag.

href is the attribute.
```html
<img src="kittens.jpg" />
```
This implements an image. 
___
ID's describe a tag or portion of your HTML. However, they are unique. You should never have multiple ids in the same document.

Class on the other hand describe portions as well but they aren't limited to just one of the same name. By assigning multiple portions of your document to the same class, they can all be adjusted at the same time through CSS.

###**They should be written in kebob case. (kjshfd-sdf).**
___
Between the H tags, each subsequent tag creates a new line. Anchor tags and span tags do not separate.

Blocking elements vs Inline elements. 

Block elements take up the whole horizontal space. 

div tags are also block elements.
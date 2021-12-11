# BASIC INTRODUCTION TO PUG
- Pug is a template engine for Node and for the browser. 
- It compiles to HTML and has a simplified syntax, which can make you more productive and your code more readable. 
- Pug makes it easy both to write reusable HTML, as well as to render data pulled from a database or API
- Pug is a more efficient, more readable,  less verbose version of html
- Roughly speaking, it is easier to write pug code and compile to html than writing html
- Pug uses tabs instead of closing and opening tags
- ex: The following html code:

```html
<div>
    <p> I am doing okey </p>
</div>
```
in pug looks like below:

```pug
div
    p I am okey
```

As you can see pug code is less verbose and a lot more cleaner

Note that:
1. Pug uses tabs instead of `<>` and `</>`
2. It is important to use same indentation throughout the document
3. Attributes are specified in parentheses, after the element
   - Ex:  `p(class='red')`

## Examples:

### example1: 

html code:

```html
<div>
    <p> Hello there </p>
    <p>This is me, paragraph</p>
    <a>Click me</a>
    <img src = 'images/bla.jpg'>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
    <ol>
        <li>Food</li>
            <ul>
                <li>Breakfast</li>
                <li>Lunch</li>
                <li>Dinner</li>
            </ul>
        <li>Shelter</li>
        <li>Drink</li>
    </ol>
</div>
```

equivalent pug code:

```pug
div
    p Hello there
    p This is me, paragraph
    a Click me
    img(scr='images/bla.jpg')
    ul
        li Item 1
        li Item 2
        li Item 3
    ol
        li Food
            ul
                li Breakfast
                li Lunch
                li Dinner
        li Shelter
        li Drink
```

### example2: 

html code:

```html
<div class="parent">
    <div class="nav">
        <span>
            <a href="https://google.com">Visit Google</a>
        </span>
        <img src="images/bla.jpg" height="30px" width="40px">
    </div>
     <div class="view">
        <div>
            <p class="notification">Hello, mate</p>
        </div>
        <img src="images/bla2.jpg" height="30px" width="40px">
    </div>
</div>
```

equivalent pug code:

```pug
div(class='parent')
    div(class='nav')
        span
            a(href='https://google.com') Visit Google
        img(src = 'images/bla.jpg', height='30px', width='40px')
    div(class='view')
        div
            p(class='notification') Hello, mate
        img(src='images/bla2.jpg', height='30px', width='40px')
```

## Class attribute
html class attributes could also be specified in alternative way using `.` notation in pug

For example, the following two codes are equivalent

```pug
div(class='nav')
    p hello there
```

```pug
div.nav
    p hello there
```

Another example, the following two codes are equivalent

```pug
p(class='green', font-size='12px') Hello, you
```

```pug
p(font-size='12px').green Hello, you
```

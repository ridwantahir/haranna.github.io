# What is HTML
- The HyperText Markup Language, or HTML is the standard markup language for documents designed to be displayed in a web browser. 
- It defines objects in a browser page and how they are organized in hierarchy
- Key points
  - Parent child relationship
    - Defines which component contains which component
  - Object tags
    - Distinguishes different types of object from one another
  - attributes
    - Defines properties of objects like height and width
## Basic html document

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
The above document will display in the browser as in the following screen shot

![Basic Image]({{site.url}}/images/html1.png)

In the above basic html document:
- The `html` tag is the parent of all objects in a page. It is mandatory to have one and only one `html` tag in the document. And it should be the root element in a page
- The `head` tag defines metadata about the page. For example, title of the page
- `body` tag is the parent element of all the html elements in  page. Like `html` tag, there should be only one `body` in an html document. Everything inside the `body` tag constitutes the 'actual' content that is displayed in the browser. In the above example, the `h1` tag and the `p` tag constitute the content of the page that is displayed in the browser
- Also notice that the `<>` is used to mark the beginning of  the tag, and `</>` is used to mark the end of the same tag

## Basic html tags
- `html`: is the root container. It contains `body` and `head` tags
- `body`: is the parent container for all objects that are displayed by the browser
- `p`: is a paragraph element
  - ex: `<p>I am a paragraph</>`
- `h1`, `h2`, `h3`, `h4`, `h5`, `h6` are heading elements. `h1` has the biggest font size by default, while `h6` has smallest font.
  - ex: `<h1>I am big heading </h1>`
  - ex: `<h5>This is heading 5</h5>`
- `li` : is an entry in a list (one bullet item in power point)
    - `<li>Item1</li>`
    - `<li>Item2</li>`
- `ul`: is container for unordered  `li` elements that belong together

 ```html
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
 ```
The above code produces

![list 1]({{site.url}}/images/li1.png)


- `ol`: is a container for order `li` elements that belong together

```html
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

The above code produces

![list 2]({{site.url}}/images/li2.png)

- `a`: is a link
  - ex: `<a>Click Here</a>`
- `img`: is an image
  - ex: `<img src="http://bla.co/images/g.gif">`
- `table`: is a table
- `tr` is a table row
- `th` is a column in a table header
- `td` is a column in a table row 

example:

```html
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```
The above code (credit: [w3schools](w3schools.com) produces:

![list 2]({{site.url}}/images/table1.png)

- `pre`: is a code block or any other text that should be displayed as is
- `code`: display code excerpts

example:

```html
<pre>
<code>
x = 5;
y = 6;
z = x + y;
</code>
</pre>
```

The above code produces:

![list 2]({{site.url}}/images/table1.png)

- `canvas`: is a drawing canvas
- `div`: is a generic container. It defines a division in html page
  - In the next example a `div` contains other elements
Example:

```html
<div>
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div>
```

The above code produces:

![Div2]({{site.url}}/images/div2.png)

- `span`: is a generic inline (does not create new line) container for phrasing, etc
  - ex: `<span><a>Click this link</a></span>`

## HTML Attributes
- All HTML elements can have attributes
- Attributes provide additional information about elements
- Attributes are always specified in the start tag
- Attributes usually come in name/value pairs like: name="value"
- ex1: `<img src="img_girl.jpg" width="500" height="600">`
- ex2: <a href="https://www.w3schools.com">Visit W3Schools</a>

Adding style attribute to the div in the above example:

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
  <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
</div> 
```
Produces:

![Div2]({{site.url}}/images/div3.png)

# What is PUG
Pug is a template engine for Node and for the browser. It compiles to HTML and has a simplified syntax, which can make you more productive and your code more readable. Pug makes it easy both to write reusable HTML, as well as to render data pulled from a database or API

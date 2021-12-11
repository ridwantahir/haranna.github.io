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
- `a`: is a link
- `img`: is an image
- `table`: is a table
- `tr` is a table row
- `th` is a column in a table header
- `td` is a column in a table row 
- `pre`: is a code block or any other text that should be displayed as is
- `canvas`: is a drawing canvas
- `div`: is a generic container. It defines a division in html page
- `span`: is a generic inline (does not create new line) container for phrasing, etc

# What is PUG
Pug is a template engine for Node and for the browser. It compiles to HTML and has a simplified syntax, which can make you more productive and your code more readable. Pug makes it easy both to write reusable HTML, as well as to render data pulled from a database or API

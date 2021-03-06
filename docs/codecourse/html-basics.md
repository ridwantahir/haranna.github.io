# BASIC INTRODUCTION TO HTML
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

![Div2]({{site.url}}/images/div1.png)

- `span`: is a generic inline (does not create new line) container for phrasing, etc
  - ex: `<span><a>Click this link</a></span>`
  
- `br` : is a new line tag

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
Produces the following image. Notice how the background color changed

![Div2]({{site.url}}/images/div3.png)

## A complete html example


```html
<!DOCTYPE html>
<html>
<body>

<div id="div1" style="background-color:lightgreen;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
  <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
  
  <a href="https://london.com"></a>
</div> 

<div id="div11" style="background-color:lightblue;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div> 

<h3>Places To Visit in London</h3>
<ul>
	<li>The Wembley Stadium</li>
    <li>The ww2 memorial musium</li>
    <li>Stanford Bridge<li>
    <li>The Emirates Stadium</li>
</ul>
<h3>Hotels Rank in London</h3>
<ol>
<li>The Hilton Hotel</li>
<li>Trump Hotel</li>
<li>The Global</li>
</ol>


<pre>
<code>
Class Student(){
	int age;
    String name;
    String fullName
}
</code>
</pre>

</body>
</html>

```

The Above example produces:

![Div2]({{site.url}}/images/html2.png)

## CSS in html
- CSS is a language used to style and change how html document is presented
- CSS rules specify presentation properties like color, height and width, etc
- style attribute of an html element follows css rule
- for example in the following code, style attribute specifies background color, color and padding of the div element

```html
<div id="div1" style="background-color:lightgreen;color:white;padding:20px;">
<div>
```

- css rules are key value pairs, terminated by `;` ex: `background-color:lightgreen;`
- more css rules can be specified together `style="background-color:lightgreen;color:white;padding:20px;height:200px;`

# The 'class' attribute in html
- In html and css, class attribute is used to target elements, with css rules
- 'class' is a special attribute
- - More than one class can be added to an element by separating them with with ' ' (space)
- For example in the following code, the 'class' attribute of the div element is set to 'parent-container', while the p is assigned two classes named 'red-p' and 'big-p'

  
```html
<div id="div1" class="parent-container">
  <p class='red-p big-p'>Hey I am and I have two classes.</p>
<div>
```
# The 'id' attribute in html
- In html, the 'id' attribute is used to uniquely identify an element
- ex:

```html
<p id="para1"></p>
```
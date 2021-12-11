# Basic Markdown Tutorial
This is a basic introduction to markdown (abbreviated as md)

For a detailed markdown(md) syntax visit [this link](https://www.markdownguide.org/basic-syntax/)

## What is markdown
- Markdown is a lightweight markup language for creating formatted text using a plain-text editor. 
- Is widely used for documentation in software projects
- Rendered to html by markdown applications and displayed in browsers, for example
- Easy syntax
- Markdown file extension is `.md`
## Example md documents
Example1:

```md
# Major Cities in the UNS
Ten of the largest cities in the world are found in the US. This is not actually true. It is totally made up. Like fake news. 
## New York City
Places to visit in new york city:
- The UN office
    1. It is awesome
    2. Easy to get to by subway
- Empire State building
- Central Park

## Los Angeles
Top Restuarants in LA
1. The Cabbanna
    - Great menu
        - Pizza
        - Lobster
    - Great staff
2. Bre Pizza
3. The Rasta Guy

```
The Above will be rendered as in the follows:

---
![list 1]({{site.url}}/images/md1.png)

---

Example 2:

```md
# Major Cities in the UNS
## Seattle
To book a ticket: [click here](https://seattle.com)
Here is an image of lovely Seattle:
![My Image](https://www.freepnglogos.com/uploads/amazon-png-logo-vector/amazon-emblem-png-logo-vector-13.png)

## San Fransisco
### Taxi Rates In Sanfransico by distance
Taxi is not cheap in SF. Look at the following table
| Distnace | Price |  Company name |
|----------|-------------|------|
|  <3km  |  $10  | Yellow Cab |
| <10km  |  $20  |   Black Cab |
| <15km  | $30  |    Uber |



```
The Above will be rendered as in the following image

---
![list 1]({{site.url}}/images/md2.png)

---

## Markdown Syntax
### Headings

```md
  # heading level 1
  ## heading level 2
  ### heading level 3
  #### heading level 4
  #### heading level 5
  #### heading level 6
```

produces the following output
---
# heading level 1
## heading level 2
### heading level 3
#### heading level 4
#### heading level 5
#### heading level 6
---

  
### Unordered lists

```md
- Item1
- Item2
    - Item2.1
    - Item2.2
        - Item2.2.1
    - Item2.3
- Item3
```
produces the following output

---
- Item1
- Item2
    - Item2.1
    - Item2.2
        - Item2.2.1
    - Item2.3
- Item3
---

### Ordered lists

```md
1. Item First
2. Item Second
3. Item Third
    1. Item 3.1
        - bullet bla
        - bullet bla2
    2. Item 3.2
```

produces the following output:

---
1. Item First
2. Item Second
3. Item Third
    1. Item 3.1
        - bullet bla
        - bullet bla2
    2. Item 3.2
---

### link

```md
[click me](https://google.com)
```
produces the following output:

---
[click me](https://google.com)

---

### Image

```md
![My Image](https://www.freepnglogos.com/uploads/amazon-png-logo-vector/amazon-emblem-png-logo-vector-13.png)
```

produces the following output:

---
![My Image](https://www.freepnglogos.com/uploads/amazon-png-logo-vector/amazon-emblem-png-logo-vector-13.png)

---

### Tables

```md
| Header1    | Header2 |
| -----------| -----------|
| Column11   | Column12     |
| Column21    | Column22   |
```

produces the following output:

---

| Header1    | Header2 |
| -----------| -----------|
| Column11   | Column12     |
| Column21    | Column22   |

---
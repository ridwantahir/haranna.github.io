# CodeCourse Guide
CodeCourse is a nodejs based tool, that is built on top of [Reveal.js](https://revealjs.com/). Walk through their [documentation](https://revealjs.com/) and make yourself familiar with the tool and then head back here to continue this tutorial

## Recap of the features of RevealJs used in CodeCourse
- Slide Features
- Code
- Fragment
- External plugin
- Speaker View
- Auto-animate
## Features of reveal.js not used in CodeCourse
- Markdown
- Vertical Slides
- PDF Export

## Course Language
- CodeCourse lesson files should be written using [pug](https://pugjs.org/api/getting-started.html)
- Other documentations are written in markdown (md)

## Create Lesson Slides
- Add Lesson slides under `/course-materials/lessons` under the respective charter. If needed, create new sub-folders
- The lesson files are pug files
- Each slide is an html `section`.
- Example pug file: `lesson1.pug`

```pug
// slide1
section
    h1 Introduction to Database
    p A database is a machine that eats data
    p It is widely used to catch fake news
// slide2
section
    h1 Types of databases
    ul
        li Relational databases
        li NoSql Databases
        li All kinds of databases
    p They all use water to extinguish fire
// slide1
section
    h2 Is Hitler really dead
    p How can one possibly know if he is?
    p Some conspiracy theorists say, he fled to Latin America
```

## Add images and other resource files
If you have supporting resources (other than slides) like images, code samples, table data, chart data, etc, put them as follows:
- images: `/course-materials/resources/images/`
- code samples: `/course-materials/resources/codes`
- chart data: `/course-materials/resources/misc/charts`
- table data: `/course-materials/resources/misc/tables`
- directory data: `/course-materials/resources/misc/dirs`

Also note that these resources are references by their **FULL QUALIFIED NAME** in the slides. for examples if an image named `chapter1/a.png` is to be referenced in the lesson pug files the attribute src should be: `/course-materials/resources/images/chapter1/a.png`

## Add Assessments to the course
To add quizzes, labs, and tests to the course, add them as below:
- quizzes: `/course-materials/assessments/quizzes`
- labs: `/course-materials/assessments/labs`
- tests: `/course-materials/assessments/tests`

Make necessary sub-folders by chapter for example, as needed.

## Add Extra resources for students
All extra reference materials for students to download go under `/course-materials/downloadable-materials/codes` or `/course-materials/downloadable-materials/reference-materials`.

Make necessary sub-folders, as needed. 

## CodeCourse Features that are not part of reveal js

### External Charts
Chart can be added to slide from a csv file. Currently only four chart types supported:
- bar chart
- doughnut chart
- pie chart
- line chart
Here is an example of how to add external charts to you slide:

```pug
section
    h2 charts
    p charts can be displayed from a csv data on file 
    div(style='width:100%;height:35vh')
            canvas(data-chart-type='doughnut', data-chart-src='/course-materials/resources/misc/charts/pie-chart1-data.csv')     
```

- `data-chart-type` could be one of 'bar', 'doughnut', 'pie' and line
- `data-chart-src` is the qualified file name of the csv data to be displayed. 

Here is an example pie/doughnut chart data format in the csv file:

```
,January, February, March, April, May, June, July
My first dataset, 65, 59, 80, 81, 56, 55, 40
```
Here is an example line/bar chart data format in the csv file:

```
,January, February, March, April, May, June, July
My first dataset, 65, 59, 80, 81, 56, 55, 40
My second dataset, 28, 48, 40, 19, 86, 27, 90
```

### External Table
Table can be displayed from csv file. 
Here is an example of how to do do the same:

```pug
section 
    h2 Tables from files 
    p Tables can be read from csv file
    div(class='data-file-table', data-file-table-active-rows='3,4', data-file-table-active-cols='3', 
            data-file-table-src='/course-materials/resources/misc/tables/table1-data.csv')

```

- `data-file-table-src` is the path where the csv file is
-  `data-file-table-active-rows` and `data-file-table-active-cols` are comma-separated list of columns and row numbers to highlight, if necessary. These fields are optional
-  the csv file should of the following format:

```
year,month,date,country
1999,03,11,US
2999,04,12,USA
3999,05,13,USS
4999,06,14,USB
5999,07,15,USC
6999,08,16,USD
7999,09,17,USV
```
  
### External Code
Code can be added to the slide from an external file.  Here is an example of how to do it:

```
section 
    h2 Code from file system 
    p You can also show code from file. you can specify start line, finish line
    p See the following example usage
    div(style='width:52vw;height:20vh', data-external-code-begin='1', data-external-code-end='14',  lang='python', 
                        data-external-code-src='/course-materials/resources/codes/lab1/example.py', class = 'data-external-code',
                        data-line-numbers='|1-7|8-9|10-14')

```
- ` data-external-code-src` is an optional attribute and specifies where in the file to start from. default is 1
- `data-external-code-end` is an optional attribute and it specifies the end line. if not specified, every line until the end of the file is read
- `data-external-code-src` is the path of the code to read.
- Also, note that all reveal.js attributes are also supported. for example, `data-line-numbers` could be added to step through the code


### External Directory tree
A beautiful directory tree can be added to the slide as well. Here is an example:

```pug
section 
    h3 DIrectory tree 
    div(style='width:20vw;height:50vh', class='data-dir-tree fragment', data-dir-tree-active-path="example - 2/day2/tree.css",
                    data-dir-tree-path='/course-materials/resources/misc/dirs/proj1-dir-tree.txt')

```

- ` data-dir-tree-path` is where the directory listing is saved. 
- `data-dir-tree-active-path` is an optional attribute to select which path to highlight, to mimic a file being edited.


### SVG Animate(Fragments)
SVG Fragments could be added to the slide. Look at the following example:

```
section 
    h2 SVG with fragments 
    p SVG is awesome. watch below 
    img(src='/course-materials/resources/images/chapter1/gf.svg', class='data-svg-animate', style="height:50vh")

```

For the fragment to work `data-fragment="7"` should be set properly on the elements that need to be fragmented. 
Refer to [this guide](/codecourse/drawio) to learn how to draw svg diagrams add attributes to svg

### SVG Motion
Basic SVG animation could be added the slide. Look at the following example:

```pug
section 
    h2 SVG Basic Animation 
    p SVG is awesome.
    img(src='/course-materials/resources/images/chapter1/hn.svg', class='data-svg-motion', style="height:40vh")

```
For the animation to work two attributes need to be set:
- `data-keyframe-id` to indicate which fragment index the element need to be added at
- `data-motion-id` to identify which objects are different versions of the same object

Refer to [this guide](/codecourse/drawio) to learn how to draw svg diagrams add attributes to svg
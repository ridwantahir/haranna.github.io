# Guidelines to Author Courses For Oromia Foundation
Here at Oromia Foundation we use a concept called coding your presentation (coding a course) to autor courses. This approach, unlike the traditional WYSIWYG tools, simplifies collaboration, versioning, QA contorl. Furthermore, it helps us keep clean separation between authoring courses and preparing course videos. 

We use a node js based tool called CodeCourse, that is built on top of the awesome  [Reveal Js](http://revealjs.com/). While [Reveal Js](http://revealjs.com/) is a rich tool, we have added new features on top of [Reveal Js](http://revealjs.com/) and some of the features in [Reveal Js](http://revealjs.com/) are not supported.  

To help us maintian the same standard, we strongly encourage the course authors to follow this guide line. 

### Required basic skills
To author courses using CodeCourse, a basic knowledge of pug or html is required. A basic html/pug tutorial will be added soon

### Setting up authoring environment
- CodeCourse is a Node.js based tool. So, node js is mandatory requirement. CodeCourse is tested with only version  16.13.1 of Node.js.
  - visit [https://nodejs.org/en/download/](https://nodejs.org/en/download/) to download the appropriate version and distribution of Node.js. Please be reminded that CodeCourse is only tested with version 16.13.1 and it may not work with other versions

- An IDE or text editor of your choice. Feel free to choose any IDE, but we recommend [visual studio code](https://code.visualstudio.com).
  - Visit [https://code.visualstudio.com/download](https://code.visualstudio.com/download) to download and install the latest version. [Visual studio code](https://code.visualstudio.com) comes with a git client which is a huge bonus.

- We use github as a repository. So, a git client should be installed on your computer. 
  - If you have installed [visual studio code](https://code.visualstudio.com), you don't need to install git client separately .
  -  Otherwise visit  [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

#### Recommended Visual Studio Code Extensions
- Draw.io integration
  - helps with drawing svg images straight from within vs code
- JS-CSS-HTML Formatter
  - helps with formatting pug/html/javascript code
- Markdown All in One
  - helps with viewing markdown files while editting
- SVG
  - previews svg images

## Getting Started with Course Authoring using CodeCourse
### Step 1 
- Go into the folder where you want to save the courses locally
    - for example, if you want to keep the course under '/home/yourname/workspaces' in linux or mac
        ```sh
        cd /home/yourname/workspaces
        ```
    - or something similar
- Clone the template course repository by running the following command
    ```sh
    git clone https://github.com/se-oromiafoundation/template-course.git
    ```
- Rename template-course to the name of your course. For example on linux or mac, if your course name is Data-Analytics
  ```sh
  mv template-course data-analytics
  ```

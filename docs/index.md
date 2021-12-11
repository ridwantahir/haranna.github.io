# Guidelines to Author Courses For Oromia Foundation
Here at Oromia Foundation we use a concept called coding your presentation (coding a course) to autor courses. This approach, unlike the traditional WYSIWYG tools, simplifies collaboration, versioning, QA contorl. Furthermore, it helps us keep clean separation between authoring courses and preparing course videos. 

We use a node js based tool called CodeCourse, that is built on top of the awesome  [Reveal Js](http://revealjs.com/). While [Reveal Js](http://revealjs.com/) is a rich tool, we have added new features on top of [Reveal Js](http://revealjs.com/) and some of the features in [Reveal Js](http://revealjs.com/) are not supported.  

To help us maintian the same standard, we strongly encourage the course authors to follow this guide line. 

### Required basic skills
To author courses using CodeCourse:
-  A basic knowledge of pug or html is required. A basic html/pug tutorial will be added soon
-  A basic familiarity with git and Github is also required

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
  - helps with viewing markdown files while editing
- SVG
  - previews svg images
- Code Spell Checker
  - To check spellings in your code and docs
## Overview of course repository on Github
All courses have their own repository on github

## Getting Started with Course Authoring using CodeCourse
### Step 1 Fetch the course from github
- Make sure that the course has already a repository on Github. If the course does not have a repository yet, please contact administrators to create the course on github first and then continue with the next steps
- Go into the folder where you want to save the courses locally
    - for example, if you want to keep the course under '/home/yourname/workspaces' in linux or mac
        ```sh
            cd /home/yourname/workspaces
        ```
    - or something similar
- Clone the course repository by running the following command. replace the course name with actual name of the course.
    ```sh
        git clone https://github.com/se-oromiafoundation/{course-name}.git
    ```
- go into the course folder. for example in linux or mac
    ```sh
        cd course-name
    ```
- and run the following command to install nodejs dependencies
    ```sh
        npm install
    ```
- Make sure that all the above commands run successfully
- To verify, everyting is setup correctly, run the following command to lauch node.js server.
    ```sh
        node server.js 
    ```
- Visit [localhost](localhost:8080) to view the slides. You should be able to see list of lessons already on the page
- Click on one of the lessons and you should see the presentaiton slides
- Congrats, now you are ready to start developing the course

### Step 2 Start Making Changes
Take a look around and make yourself familier with the folder structure. 
- For now, you can ignore all the folders except `course-materials`
- `course-materials` folder is where the course materials live.
-  `course-materials` folder is orgnaized by sub folders and further subfolders
   -  'assesments': stores course assesments. Put courses assesments under appropriate sub folders (labs, quizzes, tests). It is advised that you create additional sub folders under each sub folders (labs, quizzes, tests) by chapter and so on
   -  'downloadable-materials': This folder is not used to make course videos at all. It keeps extra materials to be shared with students. If you have a piece of code or book you want to share with students, it is here. Use the appropriate sub-folders under 'downloadable' materials and you may create new ones as needed. Please note that there is a separate folder for code excerpts used for making course videos. 
   -  'lessons': further devided by chapters, this folder contains course slides. Create as many chapters as needed. Under each chapter, create lessons. The naming convention for lessons is `lesson`{num}{extension}. 'num' is lesson number while extension is either 'pug' or 'html'. forexample, 'lesson1.pug', 'lesson2.html' are good names. This folder will be monitored by CodeCourse and there fore do not store non-slide files (html or pug) under this folder
   -  `resources`: contains supporting materials used in the slide. Use 'codes' sub folder to store codes and project files. use 'images' sub folder to store images. 'misc' folder is used to keep other types of resources such as chart data, table data, etc. Please be reminded to create new sub folders to make directory heirarchy cleaner. For example, under 'code' sub folder, you may create 'lab1', 'lab2', 'project1', etc sub folders for a logical heirarchy
   - `course-summary.md`: is a markdown file and contains general information about the course. The information includes: course prerequisites, intended audience, course content, etc

Once you are familiar with the folder structure, add new content to the course folder under `course-materials`. 

### Step 3 Committing your changes
- If this is the first time, run the following commands to initialize git repository

    ```sh
        git init
        git remote add origin https://github.com/se-oromiafoundation/template-course.git
    ```
- git branch naming convention is `w/feature` where feature is the change you made. For example, if you have added a new chapter called chapter-3, a good branch name could be `w/chapter-3`
- If you have not created a branch yet, run the following command to create a new branch named 'w/chapter-1'
    ```
        git checkout -b w/chapter-1
    ```
- To commit your changes run the followng commands. note that `-m` flag stands for commit message. Use a descriptive brief langauge to explain the changes you made
    ```
        git add .
        git commit -m 'added chapter 1'
    ```
- To Push your changes to remote github repository, run the following command
    ```sh
        git push origin w/chapter-1
    ```

### Step 4 Create pull request
- Once you are happy with all the changes you have made so far, head to the course repository on github and creae a [pull request](https://docs.github.com/en/pull-requests)
- An admin will review your changes

### Next Steps
Visit [codecourse home page](/codecourse/gettingstarted) to learn how to write pug or html slides
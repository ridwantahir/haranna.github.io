# How to use draw.io to create svg animation in CodeCourse
- [draw.io](https://draw.io/)(also called [diagrams.net](https://diagrams.net)) is a free drag and drop diagram maker
- draw.io makes it easy to make diagrams and have support for svg export
- If you have not used [draw.io](https://draw.io/) before, it is easy. it is a drag and drop tool that any one can use. Please, head to [draw.io](https://draw.io/) and make yourself familiar with platform and head back here once you are comfortable

## How to add attributes to svg export in draw.io
- First Add svgdata plugin
  - click on `Extra` from tje top menu bar
  - select `plugins`
  - in the dialogue box, click `add`
  - from the dropdown select `svgdata`
  - click `ok`
  - click `apply`
  - click `ok` again if asked again
  - draw.io will ask you to confirm to load the plugin every time the application is loaded. please confirm

![SVG motion]({{site.url}}/images/add-svg-plugin.gif)

- draw Your diagram
- Once the diagram is finished, add attributes
  - right click on the diagram you want to add attribute to
  - click `Edit Data`
  - type name of the attribute. For example, for svg fragment, type `fragment`. click on `add-property`. Then provide a value for the attribute. You can add more attributes
  - Once you are done, click apply.
  - Repeat the same procedure for other objects in the diagram that you want to add attributes to

![SVG motion]({{site.url}}/images/add-svg-data.gif)

## How to export diagram as svg
once the diagram is ready for export:
- click on `file` menu
- select `Export as`
- select `SVG`
- check
  - Transparent Background
  - Embed Images
  - Embed fonts
  - Include copy of my diagram
- click `export`
- click `download`

![SVG motion]({{site.url}}/images/export-svg.gif)

## How to create SVG Fragments
- To create svg fragments, add `fragment` property in draw.io, to all the elements you want, before exporting the svg. Remember to add `svgdata` plugin as discussed above

![SVG motion]({{site.url}}/images/add-svg-data.gif)

- Then export the svg
- To use it in the slide:

```pug
 img(src='/course-materials/resources/images/chapter1/gf.svg', class='data-svg-animate', style="height:50vh")

```

## How to create SVG motion
SVG motion works by creating key frames of a given object at different points in time. 

To animate an svg element
- Assign a `motion-id` to the object. There will be multiple versions of this object and they should share the same `motion-id`
- Create copies(duplicates) of the object and move them to a desired location and size. Each copy of the object servers as key frame. For each copy and the original add attribute `keyframe-id` and give a value. `keyframe-id` is similar to `data-fragment-index` in that it specifies when should the object be in a state that the current copy is in. For example, if a copy is assigned `key-frame-id` = 2 , the original object will move to the location of this copy on the second fragment(click on the slide), by animating its property
- Then export the svg

![SVG motion]({{site.url}}/images/svg-motion.gif)

- To use it in the slide:
  
``` pug
img(src='/course-materials/resources/images/chapter1/hn.svg', class='data-svg-motion', style="height:40vh")
```

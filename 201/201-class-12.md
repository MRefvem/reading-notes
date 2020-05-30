# Class 12 Reading Notes

### MDN Web Docs: Basic usage of canvas

Looking at the HTML `<canvas>` element. The `<canvas>` element allows us to draw 2D pictures on our website and is formatted like: `<canvas id="tutorial" midth="150" height="150"></canvas>`. Providing a useful fallback text or sub DOM helps make the canvas more accessible. Unlike the `<img>` tag, `<canvas>` comes with a closing `</canvas>` tag, which is required. The canvas tool allows us to make drawings in JavaScript. 

### Drawing shapes with canvas

By the end of this article, you will have learned how to draw rectangles, triangles, lines, arcs and curves, providing familiarity with some of the basic shapes. The canvas grid, also known as the **coordinate space**, is an HTML skeleton that allows us to draw shapes.`<canvas>` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. 

#### Drawing Rectangles

There are three functions that draw rectangles on the canvas. `fillRect(x, y, width, height)` - draws a filled rectangle. `strokeRect(x, y, width, height)` - draws a rectangular outline. `clearRect(x, y, width, height)` - clears the specified rectangular area, making it fully transparent. Each of these three functions takes the same parameters. `x` and `y` specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. `width` and `height` provide the rectangle's size.

#### Drawing Paths

A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

1. First, you create the path.
2. Then you use drawing commands to draw into the path.
3. Once the path has been created, you can stroke or fill the path to render it.

These are the functions used to perform these steps:

`beginPath()` - Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
##### Path Methods
`closePath()` - Adds a straight line to the path, going to the start of the current sub-path.
`stroke()` - Draws the shape by stroking its outline.
`fill()` - Draws a solid shape by filling the path's content area.

### Applying styles and colors

Here we will explore the canvas options we have at our disposal to make our drawings a little more attractive. You will learn how to add different colors, line styles, gradients, patterns and shadows to your drawings.

### MDN Web Docs: "Drawing Text" 

Canvas can even be used to draw and stylize text onto the canvas.
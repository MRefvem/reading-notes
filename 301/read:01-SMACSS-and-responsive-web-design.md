# Read:01 SMACSS and Responsive Web Design

## Article: Shay Howe's intro to RWD
[https://learn.shayhowe.com/advanced-html-css/responsive-web-design/](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

"The Internet took off quicker than anyone would have predicted, growing like crazy. Now, for the past few years, mobile growth has exploded onto the scene. The growth of mobile Internet usage is also far out pacing that of general Internet usage growth."

Responsive Web Design is all about how to create websites that respond well to different types of screens, for both PCs and mobile devices, no matter how large or small. Responsive web design is focused around providing an intuitive and gratifying expreience for everyone.

Flexible layouts is the practice of building the layout of a webside with a flexible grid, capable of dynamically resizing to any width. CSS3 introduced some new relative length units, specifically related to the viewport size of the browser or device. These new units include `vw`, `vh`, `vmin`, and `vmax`. Overall support for these new units isn't great, but it is growing.

Flexible layouts do not advocate the use of fixed measurement units, such as pixels or inches. The key is understanding the different uses between fixed units and relative units.

Fixed units: pixels, inches
Relative units: percentages, ems

Media queries provide the ability to specify different styles for individual browsers and device circumstances, the width of the viewport or device orientation for example. There are a couple different ways to use media queries, using the `@media` rule inside of an existing style sheet, importing a new style sheet using the `@import` rule, or by linking to a separate style sheet from within the HTML document. When a media feature and value allocate to true, the styles are applied. If the media feature and value allocate to false the styles are ignored.

`@media all and (max-width: 1024px) {...}`

Within responsive design the most commonly used features include `min-width` and `max-width`. These help build responsive websites on desktops and mobile devices equally, avoiding any confusion with device features.



## Article: All About Floats
[https://css-tricks.com/all-about-floats/](https://css-tricks.com/all-about-floats/)


What is "Float"?
Float is a CSS positioning property. To understand its purpose and origin, we can look to print design. In a print layout, images may be set into the page such that text wraps around them as needed. This is commonly and appropriately called "text wrap".

In web design, page elements with the CSS float property applied to them are just like the images in the print layout where the text flows around them. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning.


## Article: Don't Overthink It Grids
[https://css-tricks.com/dont-overthink-it-grids/](https://css-tricks.com/dont-overthink-it-grids/)



## Article: CSS Floats Explained By Riding An Escalator
[https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)



## SMACSS Official Documentation
[http://smacss.com/](http://smacss.com/)


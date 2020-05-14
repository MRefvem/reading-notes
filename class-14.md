# Class 14 Reading Notes

### Transforms
Article: https://learn.shayhowe.com/advanced-html-css/css-transforms/

With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the *transform* poperty.

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

### Transform Syntax

The transform syntax is similar to a lot of other types of code, combining key/value pairs.

### 2D Transforms

Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axes. These three-dimensional transforms help define not only the length and width of an element, but also the depth.

#### 2D Rotate

The transform property accepts a handful of different values. The *rotate* value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically.

HTML:

`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`

CSS:

```.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}```

#### 2D Scale

Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore and value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

CSS:

```.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}```

It is possible to scale only the height or width of an element using the scaleX and scaleY values.

#### 2D Translate

The translate value works a bit like that of relative positioning, push and pulling an element in different directions without interrupting the normal flow of the document. Using the translateX value will change the position of an element on the horizontal axis while using the translateY will change the position of an element on the vertical axis.

#### 2D Skew

The last transform value in the group, skew, is used to distort elements on the horizontal axis, vertical axis, or both. The syntax is very similar to that of the scale and translate values. Using the skewX value distorts an element on the horizontal axis while the skewY value distorts an element on the vertical axis. To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y axis value.%p

### Combining Transforms

It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example.

### Perspective

In order for three-dimensional transforms to work the elements need a perspective from which to transform. The perspective of an element can be set in two different ways. One way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed.


### 3D Transforms

Working with two-dimensional transforms we are able to alter elements on the horizontal and vertical axes, however there is another axis along which we can transform elements. Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width.


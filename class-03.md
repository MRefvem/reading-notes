# Class 3 Reading Notes

### Duckett HTML & CSS Chapter 3: "Lists"

There are lots of occasions when we need to use lists. HTML provides us with three different types:
- **Ordered lists** are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number. `<ol>` followed by `<li>`
- **Unordered lists** are lists that begin with a bullet point (rather than characters that indicate order). `<ul>` followed by `<li>`
- **Definition lists** are made up of a set of terms along with the definitions for each of those terms. `<dl>` followed by `<dt>` followed by `<dd>`

- There are three types of HTML lists: ordered, unordered, and definitions.
- Ordered lists use numbers.
- Unordered lists use bullets.
- Definition lists are used to define terminology.
- Lists can be nested inside one another.

### Duckett HTML & CSS Chapter 13: "Boxes"

**Boxes**
- Controlling size of boxes
- Box model for borders, margin and padding
- Displaying and hiding boxes

At the beginning of this section on CSS, you saw how CSS treats each HTML element as if it lives in its own box.
You can set several properties that affect the appearance of these boxes. In this chapter you will see how to:
- Control the dimensions of your boxes
- Create borders around boxes
- Set margins and padding for boxes
- Show and hide boxes
Once you have learned how to control the appearance of each box, you will see how to position these boxes on your pages in Chapter 15 when we look at page layout.

Box dimensions `width, height`
You can set the size of your box by modifying the dimensions. Using pixels, percentages, or ems.

Limiting width `min-width, max-width`
Some pages designs expand and shink to fit the size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.

Limiting height `min-height, max-height`

Overflowing content `overflow`
The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values: `hidden` This property simply hides any extra content that does not fit in the box. `scroll` This property adds a scrollbar to the box so that users can scroll to see the missing content.

#### Border, Margin & Padding
Every box has three available properties that can be adjusted to control its appearance:
- Border. Every box has a border (even if its is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.
- Margin. Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.
- Padding. Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.

#### Centering content.
If you want to center a box on the page (or center it inside the element that it sits in), you can set the left-margin and right-margin to auto.

#### Summary: Boxes
- CSS treats each HTML element as if it has its own box.
- You can use CSS to control the dimensions of a box.
- You can also control the borders, margins and padding for each box with CSS.
- It is possible to hide elements using the display and visibility properties.
- Block-level boxes can be made into inline boxes, and inline boxes made into block-level boxes.
- Legibility can be improved by controlling the width of boxes containing text and the leading.
- CSS3 has introduced the ability to create image borders and rounded borders.

### Duckett JavaScript & JQuery Chapter 4: "Decisions and Loops"


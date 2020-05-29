### Design Web Pages With CSS

#### Duckett Chapter 10 introducing CSS

Imagine for a second that surrounding every element in an HTML file there is an invisible box. CSS, or Cascading Style Sheets, allows us to manipulate aspects of these boxes in any way we like, adding color, choosing a font (typeface), choosing the color of the font, adding a border, etc. Simply put, CSS allows us to stylize our code we set up in HTML. Web pages are made up of two files, html and css files. You get the two files to interact by putting a link to the css into your html code `<link href="css/example.css" type="text/css" rel="stylesheet" />`

Link an external CSS to your HTML using the method above or include CSS elements within your HTML file like this 

`<style type="text/css">
body {
    font-family: arial ;
    background-color: rgb(185.179.175);}
    h1 {
        color: rgb(255.255.255);}
</style>`

#### Duckett Chapter 11 Color

This chapter is all about how to set color to your pages. Its really nice being able to specify the different foreground and background colors:

##### Foreground example:

`/* color name */
h1 {
    color: DarkCyan;}
/* hex code */
h2 {
    color: #ee3e80;}
/* rgb value */
p {
    color: rgb(100.100.90);}`

##### Background example:

`body {
    background-color: rgb(200.200.200);}
h1 {
    background-color: DarkCyan;}
h2 {
    background-color: #ee3e80;}
p {
    background-color: white;}`

#### Understanding Color

> Every color on a computer screen is created by mixing amounts of red, green, and blue. To find the color your want, you can use a color picker.

RGB Values: Values for red, green, and blue are expressed as numbers between 0 and 255. Ex: `rgb (102.205.170)`

Hex Codes: Hex values represent values for red, green, and blue in dexadecimal code. Ex: `#66cdaa`

Color Names: Colors are represented by predefined names. However, they are very limited in number. Ex: `MediumAquaMarine`

We can also control more advanced features of color like Hue, Saturation and Brightness.

#### Contrast

> When picking forgrouond and background colors, it is important to ensure that there is enough contrast for the text to be legible.

#### CSS3: Opacity

> CSS3 introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between 0.0 and 1.0 (so a value of 0.5 is 50% opacity and 0.15 is 15% opacity).

#### Color Summary

> Color not only brings your site to life, but also helps convey the mood and evokes reactions.
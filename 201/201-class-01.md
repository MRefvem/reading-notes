# Class 1 Reading Notes

### Duckett HTML & CSS Chapter 1: "Structure"

Review of some basic HTML concepts and how we can use HTML to give structure to web pages. Review of elements. Review of Body, Head and Title. Learning how to write the most basic HTML site. Learning about how content management systems and ecommerce platforms help people write blogs and sell products online even if they don't know how to write web pages from scratch. Learning how to look up the source of a webpage through your browser.

### Duckett HTML & CSS Chapter 8: "Extra Markup"

Review of the different versions of HTML and how to declare the version you're using in your code (example: declaring HTML5):

`<!DOCTYPE html>`

How to add comments to your code:

`<!-- add comment here example -->`

Reveiw of id and class attributes in html and their different uses. Id attributes affect a single section of the page but class attributes can be used on multiple elements. The rules of how the attributes are supposed to work are defined in your CSS file.

Difference between block and inline elements.

We can use the `<div>` and `<span>` functions to designate CSS rules more specifically to things you want to highlight on your page.

We can use the `<iframe>` element to embed another webpage like a window into our page. The `<meta>` element lives inside the `<head>` element and contains information about the web page.

Escape codes. Sometimes we want to use symbols that are in html for their real-world use. For example, since html will make symbols like `<` invisible, if we want to use them in our text we must instead use the escape characters (in this case it is &lt;).

### Duckett HTML & CSS Chapter 17: "HTML5 Layout"

Introducing the new elements in HTML5. HTML5 kind of simplifies the use of traditional html, specifically in respect to layout elements. The `<div>` element was traditionally used to help give structure to our pages and then the `<id>` and `<class>` elements would be used to define what those sections were for. HTML5 layout elements largely do away with the extra `<div>` code and instead goes with more of a shorthand look. For example instead of `<div id="header">` it simply says `<header>`. It makes code easier to follow but also helps webpages prioritize the most important content of a site.

Examples of HTML5 elements: `<header>` <`footer>` `<nav>` `<article>` `<aside>` `<section>` `<hgroup>` `<figure>` `<figcaption>` `<div>`

The `<a>` tag can be used to turn an entire block into a link.

You can help older browsers understand your HTML5 code is meant to be displayed as blocks by inserting this line of code into your CSS file:

```header, section, footer, aside, nav, article,
figure, figcaption {
    display: block;}```

To make HTML5 elements work in Internet Explorer 8 (and older versions of IE), extra JavaScript is needed, which is available free from Google.

IE9 was the first version of Internet Explorer to allow CSS rules to be associated with these new HTML5 layout elements. In order to style these elements using earlier versions of IE, you need to use a simple JavaScript known as the **HTML5 shiv** or **HTML5 shim**:

```<!--[if lt IE 9]>
    <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->```

### Duckett HTML & CSS Chapter 18: "Process & Design"

Understanding who your website is for, why people visit your website, what your visitors are trying to achieve, what information your visitors need, how often people will visit your site.

Creating site maps to visualize how your website is built and how to organize your individual pages into sections.

Wireframes are used to help visualize a site plan and also helps coordinate the plan if the site is being build by multiple developers.

### Duckett JavaScript & JQuery Introduction

JavaScript makes your pages more interactive.
>JavaScript allows you to make web pages more interactive by accessing and modifying the content and markup used in a web page while it is being viewed in the browser.

### Duckett JavaScript & JQuery Chapter 1: "The ABC of Programming"

#### A. What is a script and how do I create one?

A script is a series of instructions that a computer can follow to achieve a goal. Scripts can run a different section of the code in response to the situation around them. To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it. You need to give computers enough details to be able to perform tasks becuase they do not learn like humans do.

Start with the big picture of what you want to achieve, and break that down into smaller steps: 1. Define the goal. 2. Design the script. 3. Code each step.

#### B. How do computers fit in with the world around them?

Computers create models of the world using data. Defining objects & properties, defining events, defining methods, and then putting it all together.

- Computers create models of the world using data.
- The models use objects to represent physical things. Objects can have: properties that tell us about the object; methods that perform tasks using the properties of that object; events which are triggered when a user interacts with the computer.
- Programmers can write code to say "When this event occurs, run that code."
- Web browsers use HTML markup to create a model of the web page. Each element creates its own node (which is a kind of object).
- To make web pages interactive, you write code that uses the browser's model of the web page.

#### C. How do I write a script for a web page?

- It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files (like HTML pages and CSS style sheets), but they have the .js extension.
- The HTML <script> element is used in HTML pages to tell the browser to load the JavaScript file (rather like the <link> element can be used to load a CSS file).
- If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.
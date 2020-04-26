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

### Duckett JavaScript & JQuery Chapter 1: "The ABC of Programming"
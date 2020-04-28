# Class 2 Reading Notes

### Duckett HTML & CSS Chapter 2: "Text"

Structural markup vs. Semantic markup:

- Structural markup: the elements that you can use to describe both headings and paragraphs.
- Semantic markup: which provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quotation (and who said it), the meaning of acronyms, and so on.

#### Structural Markup

Headings. HTML has six "levels" of headings:

`<h1>` is used for main headings
`<h2>` is used for subheadings
`<h3>` through `<h6>` is used for further sections under the subheadings

To create a paragraph, surround the words that make up the paragraph with an opening `<p>` tag and closing `</p>` tag.

Bold & Italic
`<b>` and `<i>`

Superscript & Subscript
`<sup>` and `<sub>`

White Space. Web browsers display large spaces of white as only a single space.

Line breaks and horizontal rules. If you cant to add a line break inside the middle of a paragraph you can use the line break tag `<br />`
You can add a horizontal rule to draw a line between sections with `<hr />`
These two are called "empty elements" and are written with only one tag.

Visual editors & their code views. Content management systems and HTML editors such as Dreamweaver usually have two views of the page you are creating: a visual editor and a code view.

#### Semantic Markup.

There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages - they are known as semantic markup.

Strong and Emphasis. `<strong>` indicates that the text is meant to be said strongly and `<em>` is meant to indicate that there is a special emphasis that changes the sentence meaning.

Quotations. There are two elements commonly used for marking up quotations: `<blockquote>` and `<q>`. Use `<blockquote>` for multi-line bigger quotes and `<q>` for quotes that exist within a sentence.

Abbreviations and acronyms use the same tab: `<abbr>`. Use this to highlight an acronym and a text box will give you its full form.

Citations and Definitions. When you are referencing a piece of work such as a book, film or research paper, use the `<cite>` element. Browsers will render the comment in italics. When referencing a big concept for the first time in a document, you should use the `<dfn>` tag to bookmark where the definition takes place.

Author details. `<address>` used to display the author's email or physical adress or phone number on the page. Defaults to italics.

Changes to content. `<ins>` `<del>` used to show where you've made changes in a document. Strikethrough element `<s>` is used to draw a line through words that are no longer important.

### Duckett HTML & CSS Chapter 10: "Introducing CSS"

- What CSS does
- How CSS works
- Rules, properties, and values

The key to understanding how CSS works is to imagine that there is an invisible box around every HTML element. CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented.

CSS associates style rules with HTML elements. CSS properties affect how elements are displayed.

There are two ways to use CSS: externally and internally. It's important for a programmer to know both methods. The `<link>` element is used in an HTML document to tell the browser where to find the CSS file that is referenced to style the page. Internally you can designate CSS rules within an HTML file by using the `<style>` element. When building a site with more than one page, you should use an external CSS style sheet because this allows all pages to use the same style rules. It also means you can keep the content separate from how the page looks and means you can change the styles used across all pages by altering just one file(rather than each individual page).

Review of CSS Selectors. ???

How CSS Rules Cascade. CSS will prioritize certain lines of codes over others based on **Last Rule**, **Specificity** and **Important**

Last Rule: If the two selectors are identical, the latter of the two will take precedence. Specificity: If one selector is more specific than the others, the more specific rule will take precedence over more general ones (eg. `h1` is more specific than `*` and `p#intro` is more specific than `p`). Imporant: You can add `!important` after any property value to indicate that it should be considered more important than other rules that apply to the same element.

Inheritance. Some rules, like font-families once declared are inherited by child elements.

There are several advantages to placing your CSS rules in a separate style sheet.

In the same way that there have been several versions of HTML, there have also been different versions of CSS. Browsers did not implement all CSS features at once, so some older browsers do not support every property. This is mentioned when it is likely to affect you, along with notes where CSS properties might not behave as expected.

When a CSS property does not display as expected, it is generally referred to as a **browser quirk** or **CSS bug**. You can test your new site before launching in more than one browser to see if there are slight differences.

### Duckett JavaScript & JQuery Chapter 2: "Basic JavaScript Instructions"

### Duckett JavaScript & JQuery Chapter 4: "Decisions and Loops"
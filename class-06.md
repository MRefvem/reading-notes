# Class 6 Reading Notes

### Duckett JavaScript & JQuery Chapter 3: "Object Literals"

#### Notes on Pages 100-105


#### Summary Object Literals
- An object is a series of variables and functions that represent something from the world around you
- In an object, variables are known as properties of the object; functions are known as methods of the object.
- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.

### Duckett JavaScript & JQuery Chapter 5: "Document Object Model"

#### Notes on Pages 183-242


#### Summary Document Object Model
- The browser represents the page using a DOM tree.
- DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.
- You can select element notes by their `id` or `class` attributes, by tag name, or using CSS selector syntax.
- Whenever a DOM query can return more than one node, it will always return a `NodeList`.
- From an element node, you can access and update its content using properties such as `textContent` and `innerHTML` or using DOM manipulation techniques.
- An element node can contain multiple text nodes and child elements that are siblings of each other.
- In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).
- Browsers offer tools for viewing the DOM tree.

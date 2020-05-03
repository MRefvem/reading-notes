# Class 6 Reading Notes

### Duckett JavaScript & JQuery Chapter 3: "Object Literals"

#### Notes on Pages 100-105

Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.

In an object: variables become known as properties. If a variable is part of an object, it is called a property. Properties tell us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.

In an object: functions become known as methods. If a function is part of an object, it is called a method. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from the total number of rooms.

Like variables and named functions, properties and methods have a name and a value. In an object, that name is called a key. And object cannot have two keys with the same name. This is because keys are used to access their corresponding values. The value of a property can be a string, number, Boolean, array, or even another object. The value of a method is always a function.

Programmers use a lot of name/value pairs:
- HTML uses attribute names and values.
- CSS uses property names and values.

In JavaScript:
- Variables have a name and you can assign them a value of string, number, or Boolean.
- Arrays have a name and a group of values. (Each item in an array is a name/value pair because it has an index number and a value).
- Named functions have a name and value that is a set of statements to run if the function is called.
- Objects consists of a set of name/value pairs (but the names are referred to as keys).

Creating an object: Literal notation. Literal notation is the easiest and most popular way to create objects. (There are several ways to create object.)

The object is the curly braces and their contents. The object is stored in a variable, so you would refer to everthing inside as the object. Then each key inside is separate from its value using a colon. Then separate each property and method with a comma.

Accessing an object and dot notation

You can access the properties or methods of an object using dot notation. You can also access properties using square brackets.

To access a property or method of an object you use the name of the object, followed by a period, then the name of the property or method you want to access. This is known as **dot notation**. The period is known as the **member operator**. The property or method on its right is a member of the object on its left.

You can also access the properties or methods of an object using square bracket syntax. This time the object name is followed by square brackets, with the property or method inside them.

This notations is most commonly used when:
- The name of the property or method contains special characters (such as a dash)
- The name of the property is a number (technically allowed, but should generally be avoided)
- A variable is being used in place of the property name (you will see this technique used later)

#### Summary Object Literals
- An object is a series of variables and functions that represent something from the world around you
- In an object, variables are known as properties of the object; functions are known as methods of the object.
- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.

### Duckett JavaScript & JQuery Chapter 5: "Document Object Model"

#### Notes on Pages 183-242

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:

Making a model of the HTML page
- When the browser loads a web page, it creates a model of the page in memory.
- The DOM specifies the way in which the browser should structure this model using a **DOM tree**.
- The DOM is called an object model because the model (the DOM tree) is made of objects.
- Each object represents a different part of the page loaded in the browser window.

Accessing and changing the HTML page
- The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser.
- You will hear people call the DOM an **Application Programming Interface (API)**. User interfaces let humans interact with programs; APIs let programs (and scripts) talk to each other. The DOM states what your script can ask the browser about the current page, and how to tell the browser to update what is being shown to the user.

The DOM tree is a model of a web page
As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four types of nodes.

The Document node - The starting point for all visits to the DOM tree.
The Element nodes - HTML elements describe the structure of an HTML page.
Attribute nodes - Attribue nodes are not *children* of the element that carries them; the are *part of* that element.
Text nodes - Once you have accessed an element node, you can then reach the text within that element. No further branches of the DOM tree can come off of the text nodes. 

#### Summary Document Object Model
- The browser represents the page using a DOM tree.
- DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.
- You can select element notes by their `id` or `class` attributes, by tag name, or using CSS selector syntax.
- Whenever a DOM query can return more than one node, it will always return a `NodeList`.
- From an element node, you can access and update its content using properties such as `textContent` and `innerHTML` or using DOM manipulation techniques.
- An element node can contain multiple text nodes and child elements that are siblings of each other.
- In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).
- Browsers offer tools for viewing the DOM tree.

# Read:06 - Node, Express, and APIs

## Readings: NODE.JS
## An Introduction to Node.js on sitepoint.com
Article: [What is Node and When Should I Use It? - by James Hibbard](https://www.sitepoint.com/an-introduction-to-node-js/)

### What is Node.js?
- "Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine."
- "Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google's V8 JavaScript engine and libuv library."

### Node is built on Google Chrome's V8 JavaScript Engine
The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute. Node.js is a program we can use to execute JavaScript on our computers. In other words, it is a JavaScript runtime.

### Introducing npm, the JavaScript Package Manager
Node comes bundled with a package manager called npm. In addition to being the package manager for JavaScript, npm is also the world's largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week.

### Working with the package.json File
If you look at the contents of the test directory, you'll notice a file entitled node_modules. This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn't be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project's root.

If you open the package.json file, you'll see lodash listed under the dependencies field. By specifying your project's dependencies in the way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

### What is Node.js Used For?
The process of using Node.js is all about automating the process of developing a modern JavaScript application. These build tools come in all shapes and sizes, and you won't get far in a modern JavaScript language without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

If you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you'll be expected to have a working knowledge of Node and npm (or maybe Yarn). This isn't because you need a Node back end to run these frameworks. You don't. Rather, it's because these frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.

### Node.js Lets Us Run JavaScript on the Server
The biggest case for using Node.js is that it allows you to run JavaScript on the server. Node.js is the first implementation to gain real traction.
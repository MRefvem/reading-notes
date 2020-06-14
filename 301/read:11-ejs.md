# Read:11 - EJS

## Playlist: Intro to EJS in ExpressJS
[WalkThroughCode](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)

### Overview

Series on EJS, or "Embedded JavaScript", and how to inject EJS into your code.

### Getting Started

The fastest way to setup your server.js file is with a tool called "DB" config, but for the purposes of this video, the instructor will be building it from scratch. The first thing you want to do is an `npm init`, then `npm install --s express body-parser cors ejs`. Then proceed to setup the opening lines of your server.js, with requirements for the tools you'll be using. 

`app.set('view engine', 'ejs');`

Create a simple route of:

```app.get('/', function(requre, response){
  response.render('index', {
    foo: 'bar'
    people: [
      { name: 'dave' },
      { name: 'jerry' }
    ]
  });
});```

### Injecting values into the views

`<h1>Hello <%= foo %></h1>`
`<img src="<%= foo %>" alt="">`

### For Loops and Arrays

How to iterate over an array value. 

```<ul>
  <% for (var person of people) { %>
    <% if(person.name === 'dave') { %>
  <li>This is definitely <% person.name %>!!!</li>
    <% } else { %>
    <li>This is definitely not <% person.name %>!!! This is <% person.name %></li>
    <% } %>
  <% } %>
</ul>```

### If/Else Statement



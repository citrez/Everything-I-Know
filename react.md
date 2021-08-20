---
description: >-
  React is a UI framework in Javascript. It is useful for building
  webapplications
---

# React

### Notes

In plain vanilla javascript you can access objects in an HTML document and manipulate then. You write HTML and put a &lt;script scr = index.js&gt;&lt;/script&gt; tag at the bottom and then the JS can access and change the HTML.   
React tries to be a little cleverer and lets you write Javascript within the HTML, one of the advantages is it makes it much easier to read.  
The whole core of what Javascript is about is responding to users input. We can do this a little bit with CSS, but JS allows us to do this very flexibly to a whole host of events.  
JSX syntax is very similar to HTML and is a way of writing HTML-like code within a JS file. It them needs to be transpiled into something that is javascript.   
Babel is the transpiler of choice, it takes JSX and converts in to react elements - try it out on the [babel site](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.6&spec=false&loose=false&code_lz=Q&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.15.3&externalPlugins=&assumptions=%7B%7D)  
Interpolation is putting javascript variables in JSX code so that they can be rendered dynamically as HTML. You do this with open and closed curly brakets, much like an F string in python.  
There are two things in React to know about elements and components.   
Elements are the chucks of JSX that we can put JS variables into.

```javascript
const myItem = "Ezra"
const myJSXelement = (
    <ul>
        <li>item1</li>
        <li>item3</li>
        <li>{myItem.toUpper()}</li>
    </ul>
)
```

components are for reusabiliy. Components are a Javascript function that returns a React element \(or JSX\).   
The convention, if you are using [create react app](https://reactjs.org/docs/create-a-new-react-app.html) is to make a src/components folder and put your components in there. The App\(\) component, by convention, wraps other components, much like the body tag contains everything in an HTML page. \`

#### The DOM

React uses the DOM \(Document Object Model\), The DOM connected HTML pages, which disctate how a web pages are layed out, with JavaScript, a fully functional programming language.

The DOM stores a replresentation of an HTML document in a javascript object that we can work with and manipulate. At the end of the day all react is doing, is manipulating the DOM in a smart way. 

### 

### Links

* [React Tutorial](https://reactjs.org/tutorial/tutorial.html) - as usual often the best place to learn a thing is on the website of the thing
* [React Docs](https://reactjs.org/docs/getting-started.html) - this is the place to go for docs
* [3.5 hrs of React with Mike Dane](https://www.youtube.com/watch?v=ABQLwlE8MUA&ab_channel=MikeDane) 


---
description: >-
  React is a UI framework in Javascript. It is useful for building
  webapplications
---

# React

### Notes

React is a single page application, meaning, the server only ever has to send a single page, and react bundles everyhtning up in that single page, so when the user requests something, havascrip taskes over and sends them what they need, without having to make another request to the server. This makes react websites silky smooth. 

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
The convention, if you are using [create react app](https://reactjs.org/docs/create-a-new-react-app.html) is to make a src/components folder and put your components in there. The App\(\) component, by convention, wraps other components, much like the body tag contains everything in an HTML page. 

#### The DOM

React uses the DOM \(Document Object Model\), The DOM connected HTML pages, which disctate how a web pages are layed out, with JavaScript, a fully functional programming language.The DOM stores a replresentation of an HTML document in a javascript object that we can work with and manipulate. At the end of the day all react is doing, is manipulating the DOM in a smart way. 

React doesnt want to change the UI unless it really has to. This is where hooks come in. 

#### Hooks

usestate\(\) is a hook. When we call usestate\(0\) for example, we get an array back, with 2 elements. The first is the value, 0. The second is a function.

```javascript
[CurrentCount, SetCurrentCount] = usestate(0)

handleClick = () => {
    SetCurrentCount(1)
    }
```

The above syntax sort of registers CurrentCount as a piece of state that we want react to keep track of.

Then to change the value of CurrentCount you pass the value into the setCurrentCount function

#### Prop

a prob is a value which gets passed into a component thatinforms one aspect of what it does. Should I be thinking of an argument in a function?

```javascript
    <CountButton incrementBy = {7}/>
```

incrementBy is a prop. it is a value that is passed into the component that can be accessed via the props array.

#### Styles

You can use props in your JSX stling to change the style based on the prop value

#### External Style sheets

There are probably the way to go. Take a look at [matial UI](https://material-ui.com/).



### Material UI

#### Typography Componnent

This saves you from having to write &lt;h1&gt; tags etc. Instead you use a Typeography component with props \(arguemnt you pass into components, which are basically just functions that spit out JSX\) that define the way you want it to look

#### Container

Goes around your content and applies margin/padding

#### Buttons

Buttons have button groups which applow you to format and style all the buttons in the button group consistently

There is a startIcon and endIcon prop, for icons in the button

#### makeStyles

Fucntion from the core library for custom css styling of components



### Recharts

This is a react library for making charts.

[recharts website](https://recharts.org/en-US)

### 

### Links

* [React Tutorial](https://reactjs.org/tutorial/tutorial.html) - as usual often the best place to learn a thing is on the website of the thing
* [React Docs](https://reactjs.org/docs/getting-started.html) - this is the place to go for docs
* [3.5 hrs of React with Mike Dane](https://www.youtube.com/watch?v=ABQLwlE8MUA&ab_channel=MikeDane) 
* [Net Ninja Youtube react tutorial](https://www.youtube.com/watch?v=pnhO8UaCgxg&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=4)
* [styling CSS methods in JS](https://material-ui.com/guides/interoperability/)
* [Material UI Tutorial](https://www.youtube.com/watch?v=vyJU9efvUtQ&ab_channel=TraversyMedia) - youtube video
* [Net Ninja Material UI Tutorial](https://www.youtube.com/watch?v=ha3a63YjLro&list=PL4cUxeGkcC9gjxLvV4VEkZ6H6H4yWuS58&index=2&ab_channel=TheNetNinja) - best youtube series
* [emmet cheat sheet](https://docs.emmet.io/cheat-sheet/) - emmet is built into vs code and invaluable for shortcuts 

## Material UI

The theme in material UI is a like a large javascript object that specifies the primary secondary color, font and all other things that relate to the theme. [The full theme object can be seen here](https://mui.com/customization/default-theme/).


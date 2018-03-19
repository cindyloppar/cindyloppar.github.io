---
Layout: 
Title: "Learning React"
Date: 2018-03-09 15:36
Categories:
---

Learning React

React is a tool for rendering HTML with Javascript. 

Components 

Lets you split(UI) User Interface into independent, reusable pieces and lets you think about each piece in isolation.

Concept Components 

They are like JavaScript function. They accept arbitrary inputs called 'props' and returns React elements describing what should appear on the screen.

Define a component

function welcome(props){
    return <h1>Hello, {props.name}</h1>;
}

This function accepts a single props (which is properties) object argument with data and returns a React element.

The function is called 'functional' because they are literally JavaScript functions

ES6 class to define a component

class welcome extends React.Component{
    render(){
        return <h1> hello, {props.name}</h1>;
    }
} 

Rendering a Component

const element = <div />;

const element = <Welcome name = "Sara" />;

When React sees an element representing a user-defined component, it passes JSX attributes to this component as a single object. We call this object "props"

example this code renders "Hello, Sara"

function Welcome(props){
        return <h1> hello, {props.name}</h1>;
}

const element = <Welcome name = "Sara" />;
ReactDom.render(
    element,
    document.getElementById("root")
);


Caveat:

-Always start component names with a capital letter.
-React treats component names starting with lowercase as Dom tags.


Composing Components

Components can refer to other components in their output. This lets us use the same components abstraction for any level details. A button, a form, a dialog, a screen in React apps, all those are commonly expressed as components.
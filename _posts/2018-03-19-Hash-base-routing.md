---
Layout: 
Title: "Hash based routing"
Date: 2018-03-19 14:26
Categories:
---

# Hash-based routing

Using the portion of the pages URL Start with #, i.e the hash.

Hash-based routing is by far the simpler of the two alternatives and the exception of a few specific cases, it'll usually do the job.

Implementing hash-based routing with React is simple, just choose what to render based on the string stored in window.location.hash. We will do this once on page load and again each time the browser emits the hash charge events:

** Syntax **

//Handle the initial route
navigated()
//Handle browser navigation events 
windows.addEventLister('hashChange', navigated, false);

The navigated - It calls ReactDom.render, with the passed in component depending on the value of window.location.hash

## Manage the current location

var component = window.location.hash = '#/'
?React.createElement('div',{}, 'index Page')

We've directly referenced window.location.hash when choosing what to render.

React-app don't re-render themselves because of this when window.location.hash changes value. We need to manually call ReactDom.render to update the Dom.

ReactDom.render is never called manually. Instead, it is called from within our setState function.

The setStatus function - Is used to update the current application state.

---
Layout: 
Title: "ReactElement and ReactDom"
Date: 2018-03-14 13:53
Categories:
---

How do you create ReactElement object ?

ReactElement takes three parameters and returns a ReactElement from the React documentation:

createElement(string/React class type, [object props], [children..]) --> ReactElement

Type argument lets us specify what type of HTML element to use, it also lets us specify customer elements

The props argument is a way of specifying which attributes are defined on the HTML element.

The children arguments are strings or ReactElement objects (or arrays of the same) which will be used for the returned element content.

How ReactDom.render works

The first call to ReactDom.render is simple it walks through the passed in ReactElement and creates a corresponding HTML tree under react-app.

The second and subsequent calls don't modify previously rendered HTML elements unless the corresponding ReactElement object have changed.

In order to decide what to change, React compares the new ReactElement tree with the previous one. It uses a number of rules to decide what do do:

-ReactElement with different types are trashed and re-rendered 
-ReactElement with different props or children are re-rendered
-Identical ReactElement which have been re-ordered within an array are moved to reflect the new order 
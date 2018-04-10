---
Layout: 
Title: "Camp leader board"
Date: 2018-04-06 13:40
Categories:
---

# Camp Leader Board 

## index.js

We import react and all the other files which we are using for this app. We also use the ReactDom to call the file.

## Table

We also import files which we need to use such as Axios, Axios is an API used to get the free code camp data which we were given by the free code camp.

I exported the Table class and extend it to react component which is a function and inside that function I have a constructor which is another function and inside it I have super() and a state were I store all the data, I will be using at a later stage. 


A function which I am invoking the API and setState a new state for data by using the arrow function inside the function.

A function which checks if the currentState is recent then it should set the new state to all time there get the data from the function where I am using the API.

A function which also checks if the data is sorted by all time then change it to recent by using getting the data from the function I am using the API.

Therefore I render and return the div tags and the table to be displayed on the browser. I have two button inside the table for the points for 30 days and for the all time.

## Conclusion

I invoked the data from the state and used .map to get the images, names and all the points.

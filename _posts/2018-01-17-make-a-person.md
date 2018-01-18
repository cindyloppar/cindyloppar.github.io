---
Layout:
Title: "Make a person"
Date: 2018-01-17 15:15
Categories:
---

# Make a person
In this exercise I am supposed to use these methods which I am given to make the code work and to complete the exercise.
Fill in the object constructor with the following methods below:

    getFirstName()
    getLastName()
    getFullName()
    setFirstName(first)
    setLastName(last)
    setFullName(firstAndLast)

Run the tests to see the expected output for each method.

The methods that take an argument must accept only one argument and it has to be a string.

These methods must be the only available means of interacting with the object.

## How I solved the problem

The this Keyword

In JavaScript, the thing called this, is the object that "owns" the JavaScript code.
The value of this, when used in a function, is the object that "owns" the function. when used in an object, is the object itself.
The this keyword in an object constructor does not have a value. It is only a substitute for the new object.
The value of this will become the new object when the constructor is used to create an object.

Assigned a varaible name with a function and one parameter, this method which gets a full name using a function and access it from outside the function where a new value was assigned so that a function can access it.
I had another two get function which gets the first name and the other one gets the last name. I splitted them then got them using their index.

Therefore I had three set functions I used the this function to set the first name and last name,then gave them parameters each an every set I did and splitted them then accessed them with their index.
the last one which was setting the full name I only gave it the parameter and set it by using the index.

 this.setFullName = function(firstandlast){
    firstAndLast = firstandlast;
    return firstAndLast;
  };

## Conslusion

The excise was not hard because the guideline was straigh and forward so it wasn't complicated at all and I could understand though I made a bit of mistakes with accessign them but I was assisted quickly.
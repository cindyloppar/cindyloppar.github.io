---
layout: 
title:  "querystring"
date:   2017-08-23 10:56
categories: 
---		

Accurancy = 90%
Speed = 22wmp
Duration = 01:17

QueryString

ls the part of a uniform resource locator (URL) containing data that does not fit conveniently into a hierarchical path structure.

The Querystring collection is used to retrieve the variable values in the HTTP query mark(?)

Querystrings are also generaed by form submission, or by user typing a query into the addres bar of the browser.

Window Javascript
 
It represents the browers window. All global javascript objects,functions and variables autometically become members of window object.

var querystring = location.search.slice(1)

location.search is to display the location from the querystring.

.slice(1) is to slice(remove) the first word from the querystring.

var splitQuerystring = querystring.split("&")

.split("&") we are spliting the characters to normal array on our array. 



---
Layout: 
Title: "History API routing"
Date: 2018-03-16 14:56
Categories:
---

Routing 

Routing is when doing something in response to a change in the browsers current URL. 

There are two ways:
 
1.pushState routing 

Using the HTML5 history API

HTML5 history API gives developers the ability to modify a websites URL without a full page refresh.
This is particularly useful for loading portions of a page with JavaScript. For content to be significantly different and warrants a new URL.

Example:

Let's say a person navigates from the homepage of a site to the help page. We are loading the content of that page which we again load and swap out content with Ajax.


history.replaceState(null, null, 'hello');

The replaceState method switches out the URL in the address bar with '/hello' despite no asserts being requested and the window remaining on the same page. Yet there is a problem here.

When hitting the back button we will find that we don't return to the URL of this article but instead we will go back to whatever page we were on before. This is because replaceState does not manipulate the browsers history, it simply replaces the current URL in the address bar.

We use the pushState method to fix this.

history.pushState(null, null, 'hello')

The pushState changes out history to include whatever URL we just passed into it.
The URL has to be same origin as the current one, otherwise we might risk major security flaws.

history.pushState([data], [title], [URL])

The first parameter is the data we will need if the state of the web page changes, for instance whenever someone presses the back or forward button in their browser. In firefox this data is limit to 640k characters.

title is the second parameter which can be a string, but at the time of writing, every browser simple ignores it.

This final parameter is the URL we want to appear in the address bar. 
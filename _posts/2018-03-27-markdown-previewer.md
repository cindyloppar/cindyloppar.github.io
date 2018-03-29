---
Layout: 
Title: "Markdown Previewer"
Date: 2018-03-27 15:17
Categories:
---

# Markdown Previewer

## Index.js

In this file import all the other files which we are using for this app. We also use the ReactDom to call the file.


## Layout

The most important thing when doing a react application we first import all the react class and libraries, which is React, ReactDom and ReactMarkdown.

We always make sure that we export our class which is the file name with extends to react component as a function.

We have a function inside the export class which is called constructor and under the constructor we have super and the state to store all our data which we going to use at a later stage.

I have a function called handleChange with the parameter/argument named e and in this function we are setting the state so that we can get the value of in out textarea. This function is normally called an event handler.

Then we render what needs to be displayed in our screen/browser, by returning them inside our div tags. We have the the heading tag, the textarea, the paragraph tag and our footer.

## Conclusion

We now call the ReactMarkdown for our markdown text to be changed to normal text.
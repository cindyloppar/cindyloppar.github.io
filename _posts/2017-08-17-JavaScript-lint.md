---
layout: 
title:  "single responsibility principle"
date:   2017-08-15 10:26
categories: 
---		



JavaScript lints.
JavaScript Lint holds an advantage over competing lints because it is based on the JavaScript engine for the Firefox browser. This provides a robust framework that can not only check JavaScript syntax but also examine the coding techniques used in the script and warn against questionable practices.
What It Does

Here are some common mistakes that JavaScript Lint looks for:

    Missing semicolons at the end of a line.
    Curly braces without an if, for, while, etc.
    Code that is never run because of a return, throw, continue, 		or break.
    Case statements in a switch that do not have a break statement.
    Leading and trailing decimal points on a number.
    A leading zero that turns a number into octal (base 8).
    Comments within comments.
    Ambiguity whether two adjacent lines are part of the same 		statement.
    Statements that don't do anything.

JavaScript Lint also looks for the following less common mistakes:

    Regular expressions that are not preceded by a left 		parenthesis, assignment, colon, or comma.
    Statements that are separated by commas instead of semicolons.
    Use of increment (++) and decrement (--) except for simple 		statements such as "i++;" or "--i;".
    Use of the void type.
    Successive plus (e.g. x+++y) or minus (e.g. x---y) signs.
    Use of labeled for and while loops.
    if, for, while, etc. without curly braces. (This check is 		disabled by default.)

http://www.javascriptlint.com/

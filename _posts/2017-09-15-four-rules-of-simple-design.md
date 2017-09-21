---
layout: 
title:  "four rules of simple design"
date:   2017-09-15 12:21
categories: 
---
Accuracy = 96%
speed = 26WPM
Duration = 121 seconds

Four rules of simple design

1.Passes all the tests
-This rule also means that if you write code not for satisfying a test (unit or end-to-end or functional or any other kind, it does not matter), you're not even satisfying the first of 4 requisites.

2.Express every idea we need to express
-Given that your code passes all the tests, you can explicit concepts to "show" your design. For example concrete classes or delegation of methods that do not change the implementation are acceptable for communication, even if technically they constitute a duplication and violate 3 (which is less important in this case imho).

3.Contains no duplication
-Given that the code passes the tests and expresses your design reliably, you can extract methods and classes all the way down to eliminate duplication. This rule is widely diffused and talked about, I think for its simplicity of application; it's simple to see duplication in the majority of cases: what is not so simple is instead expressing all concepts that came up during development.

4.Minimized the number of classes, methods and other moving parts
-The bar should remain green, you should not suffer from deleting useful concepts that make the code more readable and understandable, and you shouldn't introduce duplication in the process (for example inlining again a class or method).

-This rule fosters evolutionary design instead of design for tomorrow. You can choose to write code foreseeing change, and introduce complexity to handle future changes (Strtegy/Bridge). But since it's impossible to predict axis of change consistently, you end up introducing complexity for daeling with change that doesn't happen, while refactoring is needed anyway for unpredicted changes.

https://dzone.com/articles/4-rules-simple-design


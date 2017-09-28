---
layout: 
title:  "stringify method"
date:   2017-09-26 10:06
categories: 

JSON.stringify()

JSON.stringify() method it converts the javasccript value into a JSON string.

If a replacer function or array are specified it replaces the values.

String, Numbers, Boolean are converted into corresponding primitive values when you stringify.

When a function or a symbol is encounted in an object during conversion it console null.

JSON.stringify() can return undefined, when passing pure values like JSON.stringify(function(){}) or JSON.stringify"().

When using the replacer functon a symbol will be ignored.

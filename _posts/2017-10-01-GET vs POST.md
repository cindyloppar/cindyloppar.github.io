---
layout: 
title:  "GET vs POST"
date:   2017-10-01 10:42
categories: 
---

GET vs POST

HTTP POST requests supply additional data from the client (browser) to the server in the message body. In contrast, GET requests include all required data in the URL. Forms in HTML can use either method by specifying method="POST" or method="GET" (default) in the <form> element. The method specified determines how form data is submitted to the server. When the method is GET, all form data is encoded into the URL, appended to the action URL as query string parameters. With POST, form data appears within the message body of the HTTP request. 

Differences in Form Submission

The fundamental difference between METHOD="GET" and METHOD="POST" is that they correspond to different HTTP requests, as defined in the HTTP specifications. The submission process for both methods begins in the same way - a form data set is constructed by the browser and then encoded in a manner specified by the enctype attribute. For METHOD="POST the enctype attribute can be multipart/form-data or application/x-www-form-urlencoded, whereas for METHOD="GET", only application/x-www-form-urlencoded is allowed. This form data set is then transmitted to the server.

For form submission with METHOD="GET", the browser constructs a URL by taking the value of the action attribute, appending a ? to it, then appending the form data set (encoded using the application/x-www-form-urlencoded content type). The browser then processes this URL as if following a link (or as if the user had typed the URL directly). The browser divides the URL into parts and recognizes a host, then sends to that host a GET request with the rest of the URL as argument. The server takes it from there. Note that this process means that the form data are restricted to ASCII codes. Special care should be taken to encode and decode other types of characters when passing them through the URL in ASCII format.

Submission of a form with METHOD="POST" causes a POST request to be sent, using the value of the action attribute and a message created according to the content type specified by the enctype attribute. 

Pros and Cons

Since form data is sent as part of the URL when GET is used --

Form data are restricted to ASCII codes. Special care should be taken to encode and decode other types of characters when passing them through the URL in ASCII format. On the other hand, binary data, images and other files can all be submitted through METHOD="POST"
All form data filled in is visible in the URL. Moreover, it is also stored in the user's web browsing history/logs for the browser. These issues make GET less secure.
However, one advantage of form data being sent as part of the URL is that one can bookmark the URLs and directly use them and completely bypass the form-filling process.
There is a limitation on how much form data can be sent because URL lengths are limited.

Script kiddies can more easily expose vulnerabilities in the system to hack it. For example, Citibank was hacked by changing account numbers in the URL string.[1] Of course, experienced hackers or web developers can expose such vulnerabilities even if POST is used; it's just a little bit harder. In general, the server must be suspicious of any data sent by the client and guard against Insecure Direct Object References. 

For more info: http://www.diffen.com/difference/GET-vs-POST-HTTP-Requests


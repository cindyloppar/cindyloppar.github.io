---
layout: 
title:  "A Comparison of Push and Pull Techniques for AJAX"
date:   2017-09-29 10:18
categories: 
---

A Comparison of Push and Pull Techniques for AJAX

The push-based style, where the clients subscribe to their
topic of interest, and the server publishes the changes to the
clients asynchronously every time its state changes.

Introducing the push style into AJAX systems [10] can further improve the responsiveness of such applications towards end users.
However, implementing such push solution for web ap-
plications is not trivial, mainly due to the limitations of the
HTTP protocol. This research explores the fundamental limits of
browser-based applications in providing real-time data.
We explore how real-time event notification can be added to
today’s AJAX technology and compare the pull and push approaches by conducting an empirical study to find out the actual trade-offs of each approach.

 HTTP Pull

Most AJAX applications check with the server at regular user definable intervals known as Time to Refresh(TTR).This check occurs blindly regardless of whether the state of the applications has changed. In order to achieve high data accuracy and data freshness,the pulling frequency has to be high. This, in turn, induces high network traffic and possibly unnecessary messages. The
application also wastes some time querying for the completion of the event, thereby directly impacting the responsiveness to the user. Ideally, the pulling interval should be equal to the Publish Rate(PR), i.e., rate at which the state changes.
If the frequency is too low, the client can miss some updates.

This scheme is frequently used in web systems, since it
is robust, simple to implement, allows for offline operation,
and scales well to high number of subscribers 8.

HTTP Streaming
HTTP Streaming comes in two forms namely, Page and Service Streaming.

Page Streaming

This method simply consists of streaming server data in the response of a long-lived HTTP connection. Most web servers do some processing, send back a response, and immediately exit. But in this pattern, the connection is kept open by running a long loop. The server script uses event registration or some other technique to detect any state changes. As soon as a state change occurs, it streams the new data and flushes it, but does not actually close the connection. Meanwhile, the browser must ensure the user-interface reflects the new data, while still waiting for response from the server to finish.

Service Streaming

Service Streaming relies on the XMLHttpRequest object.
This time, it is an XMLHttpRequest connection that is long-
lived in the background, instead of the initial page load. This
brings some flexibility regarding the length and frequency of
connections. The page will be loaded normally (one time),
and streaming can be performed with a predefined lifetime
for connection. The server will loop indefinitely just like in
page streaming, the browser has to read the latest response
(responseText) to update its content.

For more info: https://arxiv.org/pdf/0706.3984.pdf

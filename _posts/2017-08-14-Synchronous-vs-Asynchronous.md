---
layout: 
title:  "synchronous vs asynchronous"
date:   2017-08-14 11:48
categories: 
---


# Synchronous vs Asynchronous

Synchronous, or Synchronized means "dependent" in a way. In other words, two synchronous tasks must be aware of one another, and one task must execute in a way that is dependent on the other, such as wait to start until the other task has completed.

Asynchronous means they are totally independent and neither one must consider the other in any way, either in initiation or in execution. 

callBack hell

Is a guide for writing asynchronous in JavaScript programs

callBack is a Javascript naming conversion.Functions that use callbacks take some time to produce a result. The word 'asynchronous', aka 'async' just means 'takes some time' or 'happens in the future, not right now'. Usually callbacks are only used when doing I/O, e.g. downloading things, reading files, talking to databases, etc. 

---
layout: 
title:  "javaScript encode and decode a string"
date:   2017-09-11 10:21
categories: 
---
Accuracy = 98%
speed = 28WPM
Duration = 95 seconds

Javascript encode and decode a string

Base64 is a group of similar binary-to-text encoding schemes that represent binary data in an ASCII string format by translating it into a radix-64 representation. The term Base64 originates from a specific MIME content transfer encoding.

Base64 encoding schemes are commonly used when there is a need to encode binary data that needs to be stored and transferred over media that are designed to deal with textual data. This is to ensure that the data remain intact without modification during transport. Base64 is commonly used in a number of applications including email via MIME, and storing complex data in XML.

In JavaScript there are two functions respectively for decoding and encoding base64 strings:

    atob()
    btoa()

The atob() function decodes a string of data which has been encoded using base-64 encoding. Conversely, the btoa() function creates a base-64 encoded ASCII string from a "string" of binary data.

Both atob() and btoa() work on strings.

https://developer.mozilla.org/en-US/docs/Web/API/WindowBase64/Base64_encoding_and_decoding

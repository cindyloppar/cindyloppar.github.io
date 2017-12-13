---
Layout:
Title: "Exact Change"
Date: 2017-12-11 11:03
Categories:
---

Exact Change

The activity I was given on freecodecamp it was a very difficult challenge for me and It was confusing though we did it together and explained I think it would be best to keep on doing it and get a better understanding on it.

Problem

Design a cash register drawer function checkCashRegister() that accepts purchase price as the first argument (price), payment as the second argument (cash), and cash-in-drawer (cid) as the third argument.
cid is a 2D array listing available currency
Return the string "Insufficient Funds" if cash-in-drawer is less than the change due. Return the string "Closed" if cash-in-drawer is equal to the change due.
Otherwise, return change in coin and bills, sorted in highest to lowest order.

Approach

Created an object which hold the denominations and their values,had a reduce function which transform CID array into drawer object and an if statement which handle exact change another if statement handling obvious insufficent funds.
A while loop which loops through the denomination array
While there is still money of this type in the drawer, and while the denomination is larger than the change reminaing and round change to the nearest hundreth deals with precision errors an if statement which will push this denomination to the output only if any was used and return the current Change Array.
An if statement initializing value of empty array for reduce If there are no elements in change_arr or we have leftover change, return the string "Insufficient Funds"

Conclusion

As I said above that it was challenging and confusing and I am willing to work hard and keep on doing it time to time so that I am able to get a better understanding and about the activity.
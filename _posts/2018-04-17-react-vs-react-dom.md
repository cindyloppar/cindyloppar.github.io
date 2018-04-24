---
Layout: 
Title: "React vs ReactDom"
Date: 2018-04-17 11:53
Categories:
---
# React vs ReactDom

When building web applications in React, you use two packages—react and react-dom.

## The difference between react and react-dom

The react package holds the react source for components, state, props and all the code that is react.

The react-dom package as the name implies is the glue between React and the DOM. Often, you will only use it for one single thing: mounting your application to the index.html file with ReactDOM.render().

Mounting and Unmounting

Mount - Mounting and Unmounting File Systems. Before you can access the files on a file system, you need to mount the file system. Mounting a file system attaches that file system to a directory (mount point) and makes it available to the system. The root ( / ) file system is always mounted.

Unmounting - Unmounting a disk makes it inaccessible by the computer. Of course, in order for a disk to be unmounted, it must first be mounted. When a disk is mounted, it is active and the computer can access its contents. Since unmounting a disk prevents the computer from accessing it, there is no risk of the disk being disconnected in the middle of a data transfer.

## Why separate them?

The reason React and ReactDOM were split into two libraries was due to the arrival of React Native (A react platform for mobile development).

## Conclusion

React components are such a great way to organize UI that it has now spread to mobile to react is used in web and in mobile. react-dom is used only in web apps.

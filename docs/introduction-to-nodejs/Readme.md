# Introduction to Node js 

Welocme all to world of NodeJS . Node js is Server Side Javascript.
I will be introducing you all to fundamental concepts of Nodejs and how you can utilise it fully to Enhance your Web Development Skills s
1. [What is Node.js](#what-is-nodejs "Basic About Node.js")
2. [Key Features of Node.js](#key-features-of-nodejs "Key Features of Node.js")
3. [Installation of Node.js](#installation-of-nodejs "Installation of Node.js")
4. [Writing Hello World program](#writing-a-hello-world-program "Hello World Program")
6. [Next Steps](#next-steps "Next Steps") 
 
## What is Node.js 
Node JS is Server Side JavaScript 
Node.js is an open-source, cross-platform runtime environment that allows us to run JavaScript code on the server-side. It uses the V8 JavaScript engine, originally created for Google Chrome.
Node.js runs on various platforms (Windows, Linux, Unix, Mac OS X, etc.)



## Key Features of Node.js
Node.js offers several key features that make it popular among developers. First, it's non-blocking and event-driven, which means it can handle multiple concurrent requests efficiently without blocking other operations.
Node.js is commonly used for building real-time applications like chat servers, collaborative tools, and streaming services. Its ability to handle a large number of simultaneous connections makes it ideal for such scenarios.

## Installation of Node.js
To get started with Node.js, you'll need to install it on your machine. If you have already installed it on your machine then skip this
Visit the [official Node.js website](https://nodejs.org/en/download) and download the installer for your operating system. Follow the installation instructions, and you'll be ready to go. I will be covering Intsallation in Detail in further [Section](../installing-nodejs-and-npm/) 
```shell
node --version
```
Should give Nodejs Version which you have installed. Mine is **v18.16.1**
```shell
npm --version
```
Should give npm version installed. Mine is **9.5.1**

## Writing a Hello world program
Simple code to print Hello World on Console 
Create a simple file *hello-world.js* in a folder and write Below code in it 
```js
console.log("Hello World!")
```
open the folder in your terminal and run below command 
```shell
node hello-world.js
```
Output of Below Program is 
```shell
Hello World!
```
You can find above code in ***[this](https://github.com/siddhirajpantoji/nodejs-beginner-guide/blob/main/src/introduction-to-nodejs/hello-world.js)*** file 


## Next Steps 
This was just a basic introduction to Node.js, but there's so much more to explore! You can dive deeper into modules, asynchronous programming, building APIs, and integrating databases. Keep learning and experimenting to unlock the full potential of Node.js.
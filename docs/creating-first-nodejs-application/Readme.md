# Creating first Nodejs Application 

Lets create a Simple HTTP Endpoint which says hello world in response when we hit it with Browser 

1. [Write the simple applicatiom](#write-a-simple-application)
2. [Understand the code](#understand-the-code)
2. [Run the application](#run-the-application) 
3. Test simple application 

## Write a Simple Application
Create a new File named ```hello-world-app.js``` and copy below code into it 

```js
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});

```
You can find the file **[here](https://github.com/siddhirajpantoji/nodejs-beginner-guide/blob/main/src/creating-first-nodejs-application/hello-world-app.js)** which you can easily copy in your local machine 

## Understand the code 
lets understand whats written in above code. 
```js
const http = require('http');
```
The line const http = require('http') is a statement in Node.js that imports the built-in http module, making it available for use in your code.

In JavaScript, the require() function is used to import modules. Modules are reusable blocks of code that encapsulate related functionality. The http module, in particular, provides the necessary functionality to create HTTP servers and make HTTP requests.

By assigning the result of require('http') to the constant variable http, we can access the functionalities exposed by the http module in our code.

Once the http module is imported, we can use it to create an HTTP server by calling the createServer() method provided by the module. This method takes a callback function as an argument, which will be executed whenever a request is received by the server.

Overall, the const http = require('http') statement imports the http module, allowing us to leverage its capabilities and create an HTTP server within our Node.js application.

```js
const hostname = '127.0.0.1';
const port = 3000;
```
We have declared two constant variables by hostname and port and assigned values to it 

```js
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!');
});

```

The code snippet `const server = http.createServer((req, res) => { ... });` creates an instance of an HTTP server using the `createServer()` method provided by the `http` module.

The `createServer()` method takes a callback function as an argument. This callback function will be invoked whenever an HTTP request is made to the server. The function has two parameters: `req` (short for request) and `res` (short for response), which represent the incoming request and the outgoing response, respectively.

Within the callback function, we can define how the server should handle the request and construct the response to send back to the client. In this example, the following actions are taken:

1. `res.statusCode = 200;` sets the status code of the response to `200`, indicating a successful response.

2. `res.setHeader('Content-Type', 'text/plain');` sets the `Content-Type` header of the response to `text/plain`, indicating that the response will contain plain text content.

3. `res.end('Hello, World!');` sends the response body with the content `'Hello, World!'`. The `end()` method is used to send the response and terminate the response process.

By assigning the result of `http.createServer()` to the constant variable `server`, we create an instance of the HTTP server that is ready to listen for incoming requests and respond accordingly.

You can customize the logic inside the callback function to handle different types of requests, perform database operations, or serve dynamic content based on the request. The `createServer()` method provides a flexible way to build server applications in Node.js.

```js
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

The code snippet `server.listen(port, hostname, () => { ... });` starts the HTTP server and makes it listen for incoming requests on a specified port and hostname.

The `listen()` method is called on the `server` object, which represents the instance of the HTTP server created using `http.createServer()`. It takes the following arguments:

- `port`: The port number on which the server will listen for incoming requests.
- `hostname`: The hostname or IP address on which the server will listen.
- The callback function: An optional parameter that gets executed once the server starts listening.

Inside the callback function, the code `console.log(`Server running at http://${hostname}:${port}/`);` is executed. This line logs a message to the console, indicating that the server has started successfully, along with the URL where the server is running.

By calling the `listen()` method on the `server` object with the appropriate arguments, we instruct the server to start listening for incoming requests on the specified port and hostname.


## Run the application 
Open your terminal and go to the folder where this js file is located and type below command 

```shell
node hello-world-app.js
```

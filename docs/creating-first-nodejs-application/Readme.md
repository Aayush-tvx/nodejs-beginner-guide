# Creating first Nodejs Application 

Lets create a Simple HTTP Endpoint which says hello world in response when we hit it with Browser 

1. [Write the simple application](#write-a-simple-application)
2. [Run the application](#run-the-application) 
3. [Test simple application](#test-the-application)

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

We will be understanding all concepts one by one in Further Sections 
## Run the application 
Open your terminal and go to the folder where this js file is located and type below command 

```shell
node hello-world-app.js
```

## Test the application 
Open your browser and enter in url ```http://localhost:3000/```
Your browser will display 
```shell
Hello, World!
```
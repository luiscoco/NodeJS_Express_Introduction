# Node.js Express: A brief introduction

I'd be happy to give you a crash course on **Node.js Express**!

**Node.js Express** is a minimal and flexible **Node.js web application framework** that provides a robust set of features to develop **web** and **mobile** applications

It facilitates the rapid development of **Node-based web applications**

## 1. Getting Started

To get started with **Express**, you first need to have **Node.js** installed on your computer

https://nodejs.org/en

![image](https://github.com/luiscoco/NodeJS_Express_Introduction/assets/32194879/0e3c91c4-9a38-4f2a-affe-789a39aa6033)

Once you have **Node.js** installed, you can install **Express** in your project directory using **npm** (Node Package Manager).

**Create a new directory** for your project and navigate into it:

```
mkdir myExpressApp
cd myExpressApp
```

**Initialize a new Node.js project**:

```
npm init -y
```

This command creates a **package.json** file in your project directory, which will keep track of all the packages that your project depends on

**Install Express**:

```
npm install express
```

This command downloads the **Express** library and adds it as a dependency in your **package.json** file

## 2. Creating Your First Express Server

Let's start with a very basic **Express server** that listens for requests on **port 3000** and responds with "Hello World"

Create a file named app.js in your project directory and add the following code:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => res.send('Hello World!'));

app.listen(port, () => console.log(`Example app listening at http://localhost:${port}`));
```

**To run your server**, navigate to your project directory in the terminal and execute:

```
node app.js
```

If you go to http://localhost:3000 in your browser, you should see "Hello World!" displayed.

## 3. Understanding the Basics

In the code above:

- We require the express module

- We create an instance of an express application using express()

- We define a route handler for the GET request to the root URL (/). This handler sends back 'Hello World!' as a response

- We tell the app to listen on a specific port (3000 in this case) and log a message once the server starts

- Adding more Routes

You can define routes for different HTTP methods and paths. Here's how you can add a new route:

```javascript
app.get('/about', (req, res) => res.send('About Page'));
```

This code adds an about page that's accessible at **http://localhost:3000/about**

## 4. Serving Static Files

Express can serve static files like HTML, CSS, and JavaScript. Create a directory named public in your project directory and put some static files in it (e.g., index.html, style.css)

Then, use the following code to serve the static files:

```javascript
app.use(express.static('public'));
```

Now, if you place an index.html file inside the public directory, it will be served at the root URL (http://localhost:3000/).

## 5. Conclusion

This is a very basic introduction to Express

There's a lot more you can do, including setting up middleware for more complex request processing, handling form data, using template engines like EJS or Pug, and much more

Start experimenting with these basics, and you'll be on your way to developing full-fledged web applications with Node.js and Express!


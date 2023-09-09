![Node Js](https://www.google.com/imgres?imgurl=https%3A%2F%2Fres.cloudinary.com%2Fpracticaldev%2Fimage%2Ffetch%2Fs--u9yx6diw--%2Fc_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_500%2Cq_auto%2Cw_1000%2Fhttps%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fanuqor6vk1ibmhq8ntrf.png&tbnid=R2Si29gvzbPxIM&vet=12ahUKEwicq5q9sp2BAxUr47sIHRJOBfIQMygCegQIARB4..i&imgrefurl=https%3A%2F%2Fdev.to%2Fmidnqp%2Fnotes-advanced-nodejs-concepts-by-stephen-grider-4pp7&docid=Y7_nkkSjKgnrhM&w=1000&h=500&q=node%20js&ved=2ahUKEwicq5q9sp2BAxUr47sIHRJOBfIQMygCegQIARB4)

# Creating a Node.js Server with CMD/Vim: A Step-by-Step Guide

## Introduction

Node.js has emerged as a preferred platform for developing server-side applications, thanks to its speed and versatility. In this guide, we'll demonstrate how to set up a Node.js server using the command line interface (CMD) and the Vim text editor. This approach offers a minimalistic, yet powerful, development environment.

## Prerequisites

Before we begin, ensure that you have the following prerequisites in place:

1. **Node.js**: You must have Node.js installed on your system. Download it from the official website: [Node.js Official Website](https://nodejs.org/).

2. **A Text Editor**: We will be using Vim for this tutorial, but you can opt for any text editor you are comfortable with.

## Creating a Node.js Project Directory

Let's initiate the process by creating a directory for your Node.js project. Open CMD and navigate to the location where you intend to create your project folder.

```bash
mkdir my-node-server
cd my-node-server
```

## Initializing a Node.js Project

With your project folder in place, initialize it as a Node.js project by executing the `npm init` command. This will guide you through the setup and generate a `package.json` file.

```bash
npm init
```

You can accept the default options for most prompts by pressing Enter or run this code below:

```bash
npm init-y
```

## Installing Node.js Modules

To build our server, we'll utilize the built-in `http` module provided by Node.js. Additionally, we'll employ the popular `express` package to simplify server creation. Install these packages using npm:

```bash
npm install express --save
```

## Creating the Server Script

Now, let's create a JavaScript file for your server, naming it `server.js`, using Vim or your preferred text editor:

```bash
vim server.js
```
To edit a file with vim, press `i`.

Within `server.js`, establish a basic Node.js server using the following code:

```javascript
const express = require('express');
const app = express();
const port = 8080;

app.get('/', (req, res) => {
  res.send('Hello, Node.js!');
});

app.listen(port, () => {
  console.log(`Server is running on http://localhost:${port}`);
});
```

Save the file and exit Vim (if used) by pressing `Esc`, then typing `:wq` and hitting Enter.

## Running the Node.js Server

With the server script in place, launch your Node.js server from the command line:

```bash
node server.js
```

Your server is now active, accessible through a web browser at `http://localhost:8080`. You should observe the message "Hello, Node.js!" displayed in your browser.

## Conclusion

In this tutorial, we've guided you through the process of creating a rudimentary Node.js server using CMD and Vim. You learned how to initialize a Node.js project, install necessary packages, write a simple server script, and run the server. While this is just the beginning of what you can do with Node.js, it provides a solid foundation for building more complex server applications in the future. Feel free to explore Node.js further and expand your server-side development skills.

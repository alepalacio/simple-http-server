# SIMPLE HTTP SERVER. NODEJS.
---
If you are trying to understand how a server works, how internet works, how a HTTP request works, you have found the right place.  

In some few words we could be able to build a simple server and send a response.  

Then, let's take another challenges!

1. What is a server? 

    https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Introduction

2. What is internet, and how it works? 

    https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work

3. What is HTTP? 

    https://developer.mozilla.org/en-US/docs/Web/HTTP

4. What is HTTP request methods? 

    https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods

Being clear about these basics, we could be able to build our first simple http server.

**First: let's create a `index.js` file on your folder:**

**Second: let's code!**

    
        const http = require('http');
        const port = 3000;

        const server = http.createServer((req, res) => {
            res.write('Response from a simple HTTP server');
            res.end();
        });

        server.listen(port, () => {
            console.log('Server running on port ' + port);
        });
    

### By default, http module is in NodeJS, that's to say, it's not necessary to install it, only require.

### Set a port.  We are using a local server which will run on port 3000, but could be 4000, 5000, 8080, etc.

### Then, we set our function with two parameters: `req` = request, and `res` = response, which will let us to handle our requests from a navigator, for example.

### Use `res.write()` to send plain text on our navigator, and `res.end()` to end our request.

### Then, we set our "listening" where our server is going to run.

### To check if it is working, we send a `console.log`.

To run this server, open your terminal, place on your workspace folder and type:

    
    node index.js
    

or, let's initialize a little project, to run easily this server.  Then type on your terminal:

    
    npm init --y
    

modify your scripts on your package.json:

    
        "scripts": {
        "start": "node index.js"
        },
    

and, to run your server type:

    
    npm start
    

### ...and this is it! A very simple and basic http server is running locally on your machine. 

### This is the beginning!
---

## ALEPALACIO </> STEP-BY-STEP

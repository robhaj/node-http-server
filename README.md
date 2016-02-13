# Creating an HTTP server with Node.

- Node.js is a perfect choice for creating a web server.
- Node.js is shipped with several core modules out of the box, which we       will be using to set up our own http server.
  - This module makes it simple to create an http server via its simple but powerful api.

## Step 1

Create a new file called app.js

## Step 2

```js
// Require/import the HTTP module
var http = require('http');
```

## Step 3
```js
//Define a port we want to listen to
const PORT=8080;
```

## Step 4

```js
//Create a server
var server = http.createServer(handleRequest);
```

## Step 5

```js
//Function which handles requests and send response
function handleRequest(request, response){
    response.end('It Works!! Path Hit: ' + request.url);
}
```

## Step 6

```js
// Start our server
server.listen(PORT, function(){
    //Callback triggered when server is successfully listening. Hurray!
    console.log("Server listening on: http://localhost:%s", PORT);
});
```

```
node app.js
> Server listening on: http://localhost:8080
```

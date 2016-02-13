# Creating an HTTP server with Node.

- Node.js is a perfect choice for creating a web server.
- Node.js is shipped with several core modules out of the box, which we       will be using to set up our own http server.
  - This module makes it simple to create an http server via its simple but powerful api.

## Step 1

Create a new file called app.js

## Step 2

```js
// Import the HTTP module
var http = require('http');
```

## Step 3
```js
//Define a port we want to listen to
var port=8080;
```

## Step 4

```js
//Create a server
var server = http.createServer(requestHandler);
```

## Step 5

```js
//Function handling requests and response
function requestHandler(request, response){
    response.end('Success! You browsed to: ' + request.url);
}
```

## Step 6

```js
// Start our server
server.listen(port, function(){
    //Callback fires on success
    console.log("Server listening on: http://localhost:%s", port);
});
```

### Run the server with node
```
node app.js
> Server listening on: http://localhost:8080
```

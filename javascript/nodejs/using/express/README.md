# README.md

Based on "How to configure Rollbar.js to work with your Node.js app" at https://docs.rollbar.com/docs/nodejs

Rollbar with Node.js using Express

## Server Configuration

```
var express = require('express');
var Rollbar = require('rollbar');
var rollbar = new Rollbar('POST_SERVER_ITEM_ACCESS_TOKEN');

var app = express();

app.get('/', function(req, res) {
  // ...
});

// Use the rollbar error handler to send exceptions to your rollbar account
app.use(rollbar.errorHandler());

app.listen(6943);
```

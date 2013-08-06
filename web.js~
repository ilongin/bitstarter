var express = require('express');
fs = require('fs');

var app = express.createServer(express.logger());

app.get('/', function(request, response) {
  readFromIndex(function(data){
     response.send(data);
  });
  //response.send('Hello World 2!');
});

var port = process.env.PORT || 8080;
app.listen(port, function() {
  console.log("Listening on " + port);
});


function readFromIndex(callback){
fs.readFile('./index.html', 'utf8', function (err,data) {
  if (err) {
    return console.log(err);
  }
  callback(data);
});
}

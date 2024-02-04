# NodeJS-FileSystem-Operations

This repository contains Node.js code examples demonstrating various file system operations. Explore how to work with URLs using the URL module, read and create files, update, delete, and rename files. Additionally, delve into debugging techniques in Node.js. Each code snippet is well-commented, providing insights into the implementation details. Use these examples as a reference for your Node.js file system projects.



#### 1. Working With URL Module

```sh
const url = require("url"); // ES5
const myURL = "http://ostad.app/api/v1/product/delete?userID=1&productID=2"; // Base + path + query
const a = url.parse(myURL, true);

console.log(a.host);
console.log(a.pathname);
console.log(a.search);
console.log(a.slashes);
console.log(a.auth);
```

#### 2. Read File

```sh
const http = require('http');
const fs = require('fs');

http.createServer(function(req, res){
    fs.readFile('demo.txt', function(err, data){
        res.write(data);
        res.end();
    })


}).listen(5000, function(){
    console.log("Server is Running...");
})
```

#### 3. Create File

```sh
const http = require('http');
const fs = require('fs');

http.createServer(function(req, res){
    fs.writeFile('demo3.txt',"Hello From Demo2", function(err){
        if(err){
            res.end('File writing failed');
        } else{
            res.end('File write successfully');
        }
    })
}).listen(5000, function(){
    console.log("Server Running...");
})
```


#### 4. Update File

```sh
const http = require("http");
const fs = require("fs");
http
  .createServer(function (req, res) {
    fs.appendFile("demo3.txt", "Hello From Demo4 to update", function (err) {
      if (err) {
        res.end("File update failed");
      } else {
        res.end("File update successfully");
      }
    });
  })
  .listen(5000, function () {
    console.log("Server Running for Update");
  });
```


#### 5. Delete File

```sh
const http = require("http");
const fs = require("fs");
http.createServer(function (req, res) {
    fs.unlink("demo2.txt", function (err) {
      if (err) {
        res.end("File delete failed");
      } else {
        res.end("File delete successfully");
      }
    });
  })
  .listen(5000, function () {
    console.log("Server Running for delele operation");
  });
```


#### 6. Rename File

```sh
const http = require("http");
const fs = require("fs");
http.createServer(function (req, res) {
    fs.rename("old_file.txt", "new_file.txt", function (err) {
      if (err) {
        res.end("File Rename failed");
      } else {
        res.end("File Rename successfully");
      }
    });
  })
  .listen(5000, function () {
    console.log("Server Running for rename operation");
  });
```


#### 7. Node JS Debugging
```sh
const http = require("http");
const fs = require("fs");
http.createServer(function (req, res) {
    let a=20;
    let b=30;
    let c=40;
    let d=50;

    try{
        let sum = a+b+c+d+f;
    } catch(error){
        console.log(error);
    }

    res.end(sum);
  })
  .listen(5000, function () {
    console.log("Server Running ");
  });

```

#### Happy Coding






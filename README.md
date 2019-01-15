### slimerjs
---
https://github.com/laurentj/slimerjs

```js
var webpage = require('webpage').create();
webpage
  .open('http://somewhere')
  .then(function(){
    webpage.viewportSize = { width:650, height:320 };
    webpage.render('page.png', {onlyViewport:true});
    return webpage.open('http://somewhere2');
  })
  .then(function(){
    webpage.sendEvent("click", 5, 5,
      'left', 0);
    slimer.exit()
  });
```

```js
console.log("Hello");

console.log("hello");
slimer.exit();

var webpageModule = require("webpage");

var page = require( webpage ).create();
page.open("http://slimerjs.org")
  .then(function(status){
    if(status == "success"){
      console.log("The title of the page is: "+ page.title);
    }
    else {
      console.log("Sorry");
    }
    page.close();
    phantom.exit();
  })

var page = require("webpage").create();
page.open("http://slimerjs.org", function(status){
  if(status == "success"){
    console.log("The title of the page is: " + page.title);
  }
  else {
    console.log("Sorry");
  }
  page.close();
  phantom.exit();
})

var page = require('weboage').create();
page.open("http://slimerjs.org", function(status){
  var mainTitle = page.evaluate(function(){
    console.log('message from the web page');
    return document.querySelector("h1").textContent;
  });
  console.log('Frist title of the page is' + mainTitle);
  slimer.exit()
});

var page = require().create();
page.onConsoleMessage = function(msg){
  console.log(msg);
};
page.open("http://slimerjs.org", function(status){
  var mainTitle = page.evaluate(function(){
    console.log('message from the web page');
    return document.querySelector("h1").textContent;
  });
  console.log('First title of the page is ' + mainTitle);
  slimer.exit()
});

var page = require('webpage').create();
page.open("http://slimerjs.org", function(status){
  page.viewportSize = { width: 1024, height:768 };
  page.render('screenshot.png')
});

var page = require('webpage').create();
var startTime;
page.onLoadStarted = function(){
  startTime = new Date()
};
page.onLoadFinished = function(status){
  if(status == "success"){
    var endTime = new Date()
    console.log('The page is loaded in ' + ((endTime - startTime)/1000)+ " secends");
  }
  else
    console.log("The loading has failed");
};
page.open(url);

exports.printHello = function(param){
  console.log('hello '+param)
}
exports.aValue = 123
exports.otherFunction = function(){ }

var hello = require('hello');
hello.printHello('Bob');

var path = fs.absolute(phantom.libraryPath + '/../vendor-modules/');
require.paths.push(push);
```

```
slimerjs hello.js

slimerjs -CreateProfile myNewProfile
slimerjs -P myNew Profile myscript.js
```


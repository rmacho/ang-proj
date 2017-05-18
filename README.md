# AngularJS guide for beginners

One Paragraph of project description goes here

## AngularJS Styleguides

Some famous styleguides:

* [Todd Motto Styleguide](https://github.com/toddmotto/angularjs-styleguide/) - The angularJS styleguide
* [John Papa](https://github.com/johnpapa/angular-styleguide/) - Angular styleguide

## AngualrJS tools

Here some tools that can help your workflow

### Text editors

| [WebStorm](https://www.jetbrains.com/webstorm/) | [Aptana](http://www.aptana.com/) **Free** | [Sublime Text](http://www.sublimetext.com/) | [IntelliJ](https://www.jetbrains.com/idea/) | [Visual Studio code](https://code.visualstudio.com/) **Free** |
| --- | --- | --- | --- | --- |
|<img src="https://www.jetbrains.com/webstorm/img/screenshots/webstorm-main.png" width="100"> | <img src="http://www.aptana.com/images/product/S3-1-lrg.png" width="100"> | <img src="https://www.sublimetext.com/blog/images/build_error.png" width="100"> | <img src="https://www.jetbrains.com/idea/img/screenshots/idea_overview_5_1.png" width="100"> | <img src="https://code.visualstudio.com/home/home-screenshot-win.png" width="100"> |

## JavaScript style guide and linting tools

Some useful JavaScript style guides:

### Linting tools
| [JSLint](http://www.jslint.com/) | [JSHint](http://jshint.com/) | [JSCS](http://jscs.info/) | [ESLint](http://eslint.org/) |
| --- | --- | --- | --- |

This is a good [article](https://www.sitepoint.com/comparison-javascript-linting-tools/) that shows the differences between the linting tools

### Standard style guide
[standardJS](https://standardjs.com) : Javascript Standard Style
read this article if you want to know why use standardJS:
[Why I Use a JavaScript Style Guide and Why You Should Too](https://www.sitepoint.com/why-use-javascript-style-guide/) - Mark Brown

### which one can I use?

> One Style to Rule Them All

In Order to help you make a choice, I collected some good articles for you:
* [A Comparison of JavaScript Linting Tools](https://www.sitepoint.com/comparison-javascript-linting-tools/) - Jani Hartikainen
* [Why to use JavaScript Standard Style?](https://www.linkedin.com/pulse/why-use-javascript-standard-style-miguel-angel-dur%C3%A1n-garc%C3%ADa) - Miguel Angel Durán García
* [An Open Letter to JavaScript Leaders Regarding Semicolons](http://blog.izs.me/post/2353458699/an-open-letter-to-javascript-leaders-regarding) - Isaac Z. Schlueter

## Glossary

### Callback

- is just a function
- passed as an argument in other functions
- get called back later, mostly to be executed after another function is executed

From callbackhell.com: 
> Callbacks are just the name of a convention for using JavaScript functions. There isn't a special thing called a 'callback' in the JavaScript language, it's just a convention. Instead of immediately returning some result like most functions, functions that use callbacks take some time to produce a result. The word 'asynchronous', aka 'async' just means 'takes some time' or 'happens in the future, not right now'. Usually callbacks are only used when doing I/O, e.g. downloading things, reading files, talking to databases, etc.

```
function funcA(callback) {
    if (typeof callback === "function") {
        callback()
    }
}

funcA(function() {
    console.log('callback called')
})
// 'callback called'
```

### Callback hell

This is the situation when callbacks are nested within other callbacks several levels deep.

> Avoid the constantly growing indentation lever, produce readable and clean code. [callbackhell.com](http://callbackhell.com/) has a nice guide to writing asynchronous JavaScript programs

```
funcA(param, function(a, b){
    funcB(param, function(a, b) {
        ...
    })
})
```

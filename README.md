## Website Performance Optimization - P4
# Udacity front-end nanodegree

* <a href="https://frontend-nanodegree-mobile-portfoli.netlify.com/" target="_blank">Live Link</a>


HOW TO INSTALL
==============
- Clone Repo or download the zip file
- Open index.html for the main website
- Navigate to views/pizza.html for the pizza page.

GENERAL OPTIMIZATIONS
=====================
Shortening the Critical Rendering Path (unblock critical rendering path):
- Used the async google analytics script
- Added media="print" to the css/print link
- Inlined & minified perfmatters.js
- Inlined & minified style.css
- Google fonts moved to footer area

Image Optimization:
- Optimized all the images in img/ further using ImageOptim app, helps strip its meta info
- Resized pizzeria.jpg, created a new 100x100 pizza image and resized/cropped pizza.png. Also optimized using ImageOptim app.

PIZZA PAGE OPTIMIZATIONS
========================
Overview of changes:
- Replaced document.querySelectorAll with getElementById & getElementsByClassName respectively.

Render consistent frame-rate at 60fps when scrolling:
- var movingPizzas1 = document.getElementById("movingPizzas1"); moved outside the updatePositions function since it doesn't need to be called every time we scroll.
- Implemented requestAnimationFrame to updatePositions function

Resize pizzas is less than 5 ms:
- Created a new width array and pushed new with generated from the for loop
- Separated the original loop into 2 for loops
- The second for loop to updates the new widths and applies it to the pizza container.
- minifed main.js

Details of optimization are commented out in the main.js file.

CodeKit
=======

- I used codekit to minify all my files and changed the routing for the tags respectively to target the -min.css or -min.js files.
- The files are set to run on the minified files for maximum load / render speed.

-----------------------------------------------------
### Course requirements below
-----------------------------------------------------

## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

# Website Performance Optimization Portfolio Project

## Getting started
### View Offline
[Clone the repository](https://github.com/22guille/Optimizations.git) and open index.html in your web browser.

### View Online
View the portfolio page: [Cam's Portfolio](https://22guille.github.io/Optimizations/)

View the pizza page: [Pizzeria Mama Mia](https://22guille.github.io/Optimizations/views/pizza.html)

## Updates and Bug Fixes
### General Fixes
* Pages were stripped of superfluous styles
* All styles were minified and then placed inline in the head of each html file
* Print style link tags were given ```media="print"``` attribute
* Non-critical scripts like google analytics were given ```async``` attribute
* Images were optimized for intended width and then compressed with gulp-imagemin

### Fixes to main.js for pizza.html
* Replaced all instances of ```document.querySelectorAll()``` with ```document.getElementById()``` or ```document.getElementsByClassName()```
* All variables that do calculations had definitions moved outside 'for loops' (thus caching this value instead of calculating value repeatedly)
* Refactored ```changePizzaSizes()``` using switch statement and move randomPizzas array definition outside of the 'for loop' to fix pizza slider
* Refactored ```updatePositions()``` to do calculations for pizza positions in a second outside 'for loop' to improve moving background pizzas
* Reduce number of moving pizzas generated so that only the amount needed to fill the screen will be created
* Minify main.js script with gulp-uglify

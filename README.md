## Website Performance Optimization portfolio project

### How to run

####Part 1: Optimize PageSpeed Insights score for index.html

http://huylllooo.github.io/P4-Website-Optimization/

Copy the URL and running it through PageSpeed Insights!

####Part 2: Optimize Frames per Second in pizza.html

Here's the url to test FPS

http://huylllooo.github.io/P4-Website-Optimization/views/pizza.html

### Optimizations made

####1: CRP for index.html

Added fonts by JavaScript, then added 'async' attribute together with some other scripts(minimize the use of parser blocking resources).

Inlined minified-style.css, added media="print" for print.css.

Resized and compressed "views/images/pizzeria.jpg" by Grunt.

The page has scored 92-93 for mobile and desktop on PageSpeed Insights

####2: Framerate for pizza.html

Changed the number of moving-pizzas to 40(from 200), avoid drawing to much unnecessary pizzas.

Modified updatePositions() function:
	- Cached List of moving-pizzas
	- Use getELementByClassName to get elements faster.
	- Avoided calculations in loop.
	- Used 'transform' to move pizza instead of 'left' (also edited pizza.html thanks to Safadurimo's solution for the problem using transform: https://discussions.udacity.com/t/replace-left-with-transform/20093).
	- Disable logAverageFrame() function.

####3: Computational Efficiency for pizza.html

Avoided calculations in loop.

Modified to calculate newWidth without calling another function.

Time to resize pizzas: ~ 1ms
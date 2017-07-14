## Improving PageSpeed Score  ##


1. Optimized photos for smaller files increasing page load.  

2. Move the @media css code to print to its own css file to load only when print is chosen.

3. Eliminated the __style.css__ code to inline in the __index.html__ file for less calls when loading.

4. Links for google-analytics added __async__ to their tag to load them asynchronously.  

## Optimizing Performance ##

1. Restructured the __changePizzaSlices__ function eliminating repetitive information gathering from the DOM to reduce time taken to resize pizzas using slider in __pizza.html__.

2. created a new variable __items__, moving the line of code __document.querySelectorAll('.mover');__ to this variable to gather information once from the DOM, storing it in the variable to use in the for loop in the function __updatePositions__.

Create a new variable __scroll_top__ to hold the value of the line of code- document.body.scrollTop/1250;

Call the variable for __phase__ in the initialization of the for loop within updatePositions so the variable is created once.

3. The __for__ loop in __document.addEventListener('DOMContentLoaded', function() {__ , I reduced the number of times the loop iterates from 200 to 24. 24 iterations produces same effect as 200 with less runs of the loop. Called the variable __elem__ in the initialization of the for loop so it is created once.

Exchanged getElementById for querySelector.  

4. In the changePizzaSizes function, moved declaration of pizzasDiv outside the for loop for only one DOM call. Not needed to iterate it.

5. In resizePizzas function, exchange querySelector()for getElementById().

6. In changePizzaSizes function exchange querySelector for getElementsByClassName.

7. In changePizzaSizes function, create variable for lenght of the object array in the initialization of the for loop.

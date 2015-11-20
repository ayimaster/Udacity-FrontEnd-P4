# Udacity-FrontEnd-P4
Part 1
Page Load Speed Optimization
- Minimized CSS, JS files (Used gulp to automatically minimize the files and images)
- Compressed and resized images
- Inline critical CSS
- Media attribute added to CSS links
- Added asynch attribute to certain JS scripts
- Ran the URL through PageSpeed Insights

![portf1](https://cloud.githubusercontent.com/assets/10465533/11296403/369fddcc-8f72-11e5-991e-75cae00481b9.png)

![portf2](https://cloud.githubusercontent.com/assets/10465533/11296405/37df6d1a-8f72-11e5-91f5-6c35b4abeb3c.png)



Part 2
Frame Rate Optimization

- Analyzed critical rendering path of pizza.html
- Optimized loops in js/main.js
- Optimized scroll events
- Optimized layer compositing
- Optimized images
- Changed access to DOM elements
- Minimized CSS and JS files
- Used gulp to automatically minimize the files and images
- Added 'use strict' to function definitions, based on suggestions in the code review
- Changed document.querySelector, document.querySelectorAll to document.getElementByID and document.getElementByClassName respectively, based on suggestions in the code review
- Optimized 'for loops' by declaring the index and array length outside the for loop declaration, as per code review suggestions. Specifically in the updatePositions(), 'variable phase' was declared outside of the loop, to avoid being created every time the loop runs. Also, as suggested, a better approach to dynamically calculate the number of pizzas needed to fill the screen was changed, based on browser window resolution: 'window.screen.height'.
References
https://developer.mozilla.org/en-US/docs/Web/API/Screen/height
http://www.w3schools.com/jsref/prop_screen_height.asp
https://developer.mozilla.org/en-US/docs/Web/API/Screen/width
http://tripleodeon.com/2011/12/first-understand-your-screen/
http://ryanve.com/lab/dimensions/ 


![pizza_js1](https://cloud.githubusercontent.com/assets/10465533/11296401/34017e72-8f72-11e5-8cef-24e6fb34b44f.png)

![pizza_js2](https://cloud.githubusercontent.com/assets/10465533/11296402/3519fb72-8f72-11e5-8bdd-bf9c403a5fd2.png)



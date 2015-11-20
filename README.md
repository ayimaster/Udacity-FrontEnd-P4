# Udacity-FrontEnd-P4
Summary

This project was completed as part of Udacity Front-End Web Developer Nanodegree. The projects involves improving the performance of loading and rendering of an existing portfolio site and a pizza recipe site. 
Source code for the portfolio site in this repository is in original_portfolio/ and production code in production_portfolio/
Source code for the pizza recipe site in this repository is in original_pizza/ and the production code in production_pizza/

Steps to launch Portfolio Site: 
1. Clone the repository to your local machine
2. Launch local http server to test using command line: python -m SimpleHTTPServer 8080
3. In a browser open localhost:8080
4. In the same directory of this repo in your local machine install and run ./ngrok http 8080 to access a secure public URL to the site.
5. Copy the public URL given by ngrok in the terminal and paste in PageSpeed Insights to view the score of the page
6. If necessary, follow PageSeed Insights suggestions to improve the site

Part 1
Page Load Speed Optimization
Steps to launch Pizza Recipe site: 
1. Clone this repository to your local machine
2. Click to open pizza.html in production_pizza/js folder of this repo
3. To find more information, such as comments and instructions please see original_pizza/main.js 

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

Optimization of pizza.html/ main.js files
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

For more information please refer to Udacity Nanodegree Mobile Portfolio: https://github.com/udacity/frontend-nanodegree-mobile-portfolio

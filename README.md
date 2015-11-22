# Udacity-FrontEnd-P4
## Summary

This project was completed as part of Udacity Front-End Web Developer Nanodegree. The project involves improving the performance of loading of an existing portfolio site and rendering of a pizza recipe site. 

The source code for the portfolio site in this repository is in *original_portfolio/* and production code in *production_portfolio/*
The source code for the pizza recipe site in this repository is in *original_pizza/* and the production code in *production_pizza/*

##Part 1
###Page Load Speed Optimization
#### Steps to launch Portfolio Site
##### Option 1
1. Using command line clone the repository to your local machine
   ```
   git clone https://github.com/ayimaster/Udacity-FrontEnd-P4/tree/master/production_portfolio
   ```

2. Launch local http server to test. In your terminal write `python -m SimpleHTTPServer 8080`

3. Once the server is running open a browser and type in url  `localhost:8080`
 
4. In the same directory of this repo on your local machine install ngrok to access a secure public URL to the site. To install ngrok, visit: https://ngrok.com/
In the terminal run `./ngrok http 8080`
 
5. Copy the public URL given by ngrok and paste in [PageSpeed Insights API!](https://developers.google.com/speed/pagespeed/insights/) to view the score of the page. The higher the score the less room for improvement is required. 

6. If necessary, follow PageSeed Insights suggestions to improve the site

##### An alternative option is to visit my Github page and follow optimization techniques below:

```
https://github.com/ayimaster/Udacity-FrontEnd-P4/tree/master/production_portfolio
```

- Minimized CSS, JS files (Used gulp to automatically minimize the files and images)
- Compressed and resized images
- Inline critical CSS
- Media attribute added to CSS links
- Added asynch attribute to certain JS scripts
- Ran the URL through PageSpeed Insights

![portf1](https://cloud.githubusercontent.com/assets/10465533/11296403/369fddcc-8f72-11e5-991e-75cae00481b9.png)

![portf2](https://cloud.githubusercontent.com/assets/10465533/11296405/37df6d1a-8f72-11e5-91f5-6c35b4abeb3c.png)


## Part 2
###Frame Rate Optimization
#### Steps to launch Pizza Recipe Site
#####To see the source (original) code:
1. Clone this repository to your local machine: 
```git clone https://github.com/ayimaster/Udacity-FrontEnd-P4/tree/master/original_pizza```

2. Open pizza.html in Chrome or in any other browser and main.js in any text editor. 
   To see the site's rendering and performance open Chrome Developer Tools. 

######To see the optimization made by me (production code):
1. Clone this repository to your local machine
```git clone https://github.com/ayimaster/Udacity-FrontEnd-P4/tree/master/production_pizza```

2. Open pizza.html an a browser and main.js in a text editor.

#### Alternatively visit my [Github page!](https://github.com/ayimaster/Udacity-FrontEnd-P4/tree/master/production_pizza) to see commits made and follow optimization techniques below. 
- Analyzed critical rendering path of pizza.html
- Optimized loops in js/main.js
- Optimized scroll events
- Optimized layer compositing
- Optimized images
- Changed access to DOM elements
- Minimized CSS and JS files
- Used gulp to automatically minimize the files and images
- Added 'use strict' to function definitions, based on suggestions in the code review
- Changed ```document.querySelector, document.querySelectorAll``` to ```document.getElementByID and document.getElementByClassName``` respectively, based on suggestions in the code review
- Optimized 'for loops' by declaring the index and array length outside the for loop declaration, as per code review suggestions. Specifically in the updatePositions(), 'variable phase' was declared outside of the loop, to avoid being created every time the loop runs. Also, as suggested, a better approach to dynamically calculate the number of pizzas needed to fill the screen was changed, based on browser window resolution: ```window.screen.height```.
References
https://developer.mozilla.org/en-US/docs/Web/API/Screen/height
http://www.w3schools.com/jsref/prop_screen_height.asp
https://developer.mozilla.org/en-US/docs/Web/API/Screen/width
http://tripleodeon.com/2011/12/first-understand-your-screen/
http://ryanve.com/lab/dimensions/ 


![pizza_js1](https://cloud.githubusercontent.com/assets/10465533/11296401/34017e72-8f72-11e5-8cef-24e6fb34b44f.png)

![pizza_js2](https://cloud.githubusercontent.com/assets/10465533/11296402/3519fb72-8f72-11e5-8bdd-bf9c403a5fd2.png)

For more information please refer to Udacity Nanodegree Mobile Portfolio: https://github.com/udacity/frontend-nanodegree-mobile-portfolio

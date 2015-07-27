Introduction
============
This is my submission for project 4 of [Udacity's Nanodegree in Front-End Web Development](https://www.udacity.com/course/front-end-web-developer-nanodegree--nd001). It contains several web page documents (HTML, JS, CSS) that I have edited for page speed and render optimization.


###Version number and release date
This is version 1.0, published on 28 July 2015.


###Credits and contact
The original assets were created by Udacity.

I (Said Khalid Scharaf) have made minor edits to optimize the pages so that they meet the project's success criteria. You can reach me at sks@posteo.de


###Where to get the project files from
You can find my project submission at https://github.com/khalito/Project-4-Web_Site_Optimization/

The original assets can be found here: https://github.com/udacity/frontend-nanodegree-mobile-portfolio


How to run the web pages
========================

###View the pages locally on your desktop
1. Download my git repository (see link above) as a zip file and unzip it to your favorite local folder
2. Open the index.html in that folder with your favorite web browser
3. If you are using Chrome, you can use its Developer Tools to record a timeline and review the performance of the web pages.


###View the pages on your mobile device or any remote computer
1. Download my git repository (see link above) as a zip file and unzip it to your favorite local folder
2. Run a local server using python

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

3. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok http 8080
  ```

4. Copy the public URL ngrok gives you and access it with your mobile device's or a remote computer's browser.


Optimizations I have applied as part of the project goals
=========================================================

###Optimizations applied to increase Google Page Speed ratings of index.html to at least 90/100 on mobile and desktop (Part 1 of the project)

* Move all CSS from style.css inline into index.html
* Load Google Web Font in index.html through a JavaScript script instead of a CDN link
* Load Google Analytics in index.htmls asynchronously
* Add a media="print" property to the print.css stylesheet hyperlink in index.html

###Optimizations applied to improve the performance of views/pizza.html to at least 60 frames per second (Part 2 of the project)

* Replace two instances of querySelectorAll() with getElementsByClassName() in views/js/main.js at 515 and 454
* Move all variables used inside changePizzaSizes() and updatePositions() outside of the function's for loop
* Reduce the number of pizzas used in the event listener at 539 to 35 because we do not see all 200 pizzas all the time.
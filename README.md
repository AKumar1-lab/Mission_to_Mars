## Mission to Mars - Webscraping with HTML/CSS

Module 10

Completed by Angela Kumar

## Purpose

Build an app to scrape websites for data pertaining to the Mission to Mars, and then create an HTML page to display the findings.

## Overview

Web scraping is a method used by organizations worldwide to extract online data for analysis. Web scraping automates tedious tasks for personal projects.
Instead of visiting each website and copying an article, a web scraping script will perform those actions and save the scraped data for later analysis.

## Resources

 Files: Mission_to_Mars.ipynb converted to Mission_to_Mars_Challenge.ipynb;Mission_to_Mars_Challenge_starter_code.ipynb; 
 Mission_to_Mars_Challenge.py converted to scraping.py. updated index.html
 
 Software: Jupyter Notebook; VSCode; Beautiful Soup; Flask; Flask_Pymongo; Splinter; MongoDB; MongDBCompass; Webdriver_Manager; HTML/CSS; Bootstrap 
 
## Background

Robin's web app is looking good and functioning well, but she wants to add more polish to it. She had been admiring images of Mars’s hemispheres online and realized that the site is scraping-friendly. She would like to adjust the current web app to include all four of the hemisphere images. To do this, you’ll use BeautifulSoup and Splinter to scrape full-resolution images of Mars’s hemispheres and the titles of those images, store the scraped data on a Mongo database, use a web application to display the data, and alter the design of the web app to accommodate these images.

## Deliverables

* Deliverable 1: Scrape Full-Resolution Mars Hemisphere Images and Titles
1. Make a copy of the Mission_to_Mars.ipynb file, and rename it Mission_to_Mars_Challenge.ipynb.
2. Download the Mission_to_Mars_Challenge_starter_code.ipynb, copy the starter code, and paste at the end of your Mission_to_Mars_Challenge.ipynb file.
3. In Step 1, use the browser to visit the Mars Hemispheres (https://marshemispheres.com) website to view the hemisphere images.

<img width="734" alt="Mars Image results" src="https://user-images.githubusercontent.com/85860367/131446357-f91903b2-f705-4e27-9b45-be26a7dc4e5f.PNG">

4. Use the DevTools to inspect the page for the proper elements to scrape. You will need to retrieve the full-resolution image for each of Mars's hemispheres.
5. In Step 2, create a list to hold the .jpg image URL string and title for each hemisphere image.
6. In Step 3, write code to retrieve the full-resolution image URL and title for each hemisphere image. The full-resolution image will have the .jpg extension.
7. Loop through the full-resolution image URL, click the link, find the Sample image anchor tag, and get the href.
8. Save the full-resolution image URL string as the value for the img_url key that will be stored in the dictionary you created from the Hint.
9. Save the hemisphere image title as the value for the title key that will be stored in the dictionary you created from the Hint.
10. Before getting the next image URL and title, add the dictionary with the image URL string and the hemisphere image title to the list you created in Step 2.
11. In Step 4, print the list of dictionary items. The list should look like the following image:

<img width="543" alt="hemisphere image urls" src="https://user-images.githubusercontent.com/85860367/131447042-991eecd5-8e05-4569-aaaa-655e6150c72a.PNG">

12. After you have confirmed that you have the image URLs and titles for all four hemisphere images, quit the browser by executing Step 5.

* Deliverable 2: Update the Web App with Mars Hemisphere Images and Titles
1. Export the Mission_to_Mars_Challenge.ipynb file as a Python file, and save it as Mission_to_Mars_Challenge.py.
2. In the def scrape_all() function in your scraping.py file, create a new dictionary in the data dictionary to hold a list of dictionaries with the URL string and title of each hemisphere image.
3. Below the def mars_facts() function in the scraping.pyfile, create a function that will scrape the hemisphere data by using your code from the Mission_to_Mars_Challenge.py file. At the end of the function, return the scraped data as a list of dictionaries with the URL string and title of each hemisphere image.
4. Run the app.py file, then check your Mongo database to make sure that you are retrieving all of the data.

<img width="660" alt="Scrape Web Page" src="https://user-images.githubusercontent.com/85860367/131449901-a183efc8-dbf0-4f08-abdc-1989c1b4af3e.PNG">

6. Modify the index.html file to access your database, and retrieve the img_url and title as you loop through the dictionary in the database using {% for hemisphere in mars.hemispheres %}. The dictionary in the mars hemispheres database is the dictionary that was created from the Hint after Step 3 in Deliverable 1.
7. Run the app.py file, open the index.html file, and click the "Scrape New Data" button.
8. After you have scraped the data, confirm that your webpage has the full-resolution images and the titles of the four hemisphere images, like the image below.

<img width="587" alt="screenshot after hemisphere add" src="https://user-images.githubusercontent.com/85860367/131449784-ce05588e-1ec5-4f2f-93fa-ef2f0aead90e.PNG">
<img width="574" alt="Hemisphere Row 1" src="https://user-images.githubusercontent.com/85860367/131449804-81d6c83a-42dd-4f5f-afd0-cd037420a3c1.PNG">
<img width="567" alt="Hemisphere Row 2" src="https://user-images.githubusercontent.com/85860367/131449846-2f9a3f31-025c-4185-8ae2-e9204f20ebcd.PNG">


* Deliverable 3: Add Bootstrap 3 Components

For this part of the Challenge, update your web app to make it mobile-responsive, and add two additional Bootstrap 3 components to make it stand out.

<img width="365" alt="Responsive header" src="https://user-images.githubusercontent.com/85860367/131454941-ddcebfae-f4ad-4214-bf18-aa106afb75d8.PNG">
<img width="342" alt="Responsive Mars Facts" src="https://user-images.githubusercontent.com/85860367/131455008-d7b9173f-a851-474a-b4e9-6b2976771a6c.PNG">
<img width="342" alt="Responsive Cerberus" src="https://user-images.githubusercontent.com/85860367/131455065-cf1df69b-56e4-443e-8bbb-a2e90ebcabc8.PNG">
<img width="342" alt="Responsive Schiaparelli" src="https://user-images.githubusercontent.com/85860367/131455102-e8ec754e-2d5e-4fce-a46e-d1e47e56780d.PNG">
<img width="342" alt="Responsive Syrtis" src="https://user-images.githubusercontent.com/85860367/131455150-e984f28d-2f86-467d-90f4-6b1ee8784a63.PNG">
<img width="342" alt="Responsive Valles Marineris" src="https://user-images.githubusercontent.com/85860367/131455319-f5eca54b-a696-4c85-80b8-47c9b72d5d1b.PNG">

![image](https://user-images.githubusercontent.com/85860367/131454762-b80b74c7-a7af-4d57-9ef1-bf664ce4c6ad.png)

## Summary  
This was supposed to be a fun exercise; however there are many tasks to set up the script for web scraping, and if one is unfamiliar it can be tedious upfront.  In the long run reviewing the webpage was exciting to look at.  It was well worth the effort, and I could not stop looking at the webpage that was created.  Mars is usually a fiery planet; however looking at the hemispheres gave me a different perspective and hope.  

## Completed by Angela Kumar

# hospitalization-pricing-tool

DESCRIPTION - Describe the package in a few paragraphs
The app for New York State Health Costs Recommendations is a Node.js app that displays projected costs per county, and per hospital in the state of New York. The main idea is for the user to be able learn more about costs for a potential health procedure done in the hospital. 
Unlike many commercial products where the user is able to find out the cost before purchasing, health services may very in costs depending on area of the hospital, type of procedure and other factors leaving the customers in the unknown on how much they will pay at the end of the services.
With easy to navigate user interface, our team gives the user an opportunity to filter on their condition, age and gender to find the cost of the procedure and able to choose the hospital.

This package is running on http server, which contains Leaflet(an open-source JavaScript library for interactive maps) and D3 (D3 is a JavaScript library for visualizing data with HTML, SVG, and CSS)
The data folder contains the data used in the app which are the projections received from the machine learning output. The data for prediction came from http://ace.iime.cloud/sparcs/drg/194. And the NYC hospital data came from https://www.arcgis.com/home/item.html?id=c012aabe95f74f1c978b6b131a6a4d4e. 
The js forlder contains the javacsript that runs the interactives on the map.
The css and img are decorative images and styles used in the app.
The index.html contains the html to display the content of the app.
The predict folder contains the jupyter notebook that analyzes data, runs the algorithms and outputs the predict.csv located in data folder.



INSTALLATION - How to install and setup your code

The Jupyter notebook used to ran all the modeling and cleaning of the data was run on Google Cloud in order to avoid large data processing on local machine, increasing the speed of processing. Notebook can be exported to Google Cloud and ran there. 


To run the Jupiter notebook locally, navigate to the folder:

```cd /predict```

If python is installed on laptop ( if not, download Anaconda for Python):

 ```jupyter notebook```

Run the commands there to product predict.csv file with the correct paths to data specified.




To display the data and run the D3.JS scripts on your machine you must download a few dependecies.
D3.JS requires you download node.js and npm (if not already installed) before you can do anything.
Check that node.js is installed:

```node -v```

Check that npm is installed:

```npm -v````

If node and npm are not installed, go here (https://nodejs.org/en/download/)


Now, navigate to root of the folder: 

```cd /team_056_final_code```

Run npm install:

```npm install npm@latest -g```

To install whats needed to run d3.js run:

```npm install -g http-server```

To Run Server:

```http-server & ```

If port 8080 is not busy, navigate to (check terminal output to see where the app is hosted): 

http://127.0.0.1:8080

Voila, you are done!


EXECUTION - How to run a demo on your code

Once you open the demo, the screen on the left displays 3 different filters: condition, gender, age group.
The first selection is made for condition. Once the condition is choosen, the map will change the color according to the cost for the county for that condition. 
Once the the age group selected, hoover over a hospital to see the projected cost for the condition and that age group.
Lastly, if you choose the gender and hoover again over a hospital, it will show projected cost for condition, age group and gender.
To reset everything, click the Reset button.
Explore different conditions and filtering on your own.

FINAL DEMO : https://youtu.be/9KseNwZ8WUo

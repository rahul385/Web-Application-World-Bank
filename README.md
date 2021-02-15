# Web-Application-World-Bank

<p align = 'center'><img src = 'logo.png', height=200, width =320></p>

### Table of Contents
1. [Project Overview](#project)
2. [File Description](#file)
3. [Visualizations](#image)
4. [Licensing, Authors, and Acknowledgements](#licensing)


## Project Overview <a name="project"></a>
The objective of this web application is to create a data dashboard to track key metrics and trends using real data from World Bank website. This web application has been deployed on Heroku using Flask (see the link below).

[World Bank Web-Application](https://web-app-worldbank.herokuapp.com/)

## File Description <a name="file"></a>

* **data**: This folder contains data from [World Bank](https://data.worldbank.org/indicator/SP.RUR.TOTL.ZS?view=chart) in csv format.
       
* **worldbankapp**: This folder contains the package files.
    * `routes.py` : Python module for rendering html pages.
    * `__init__.py` : Package initilization file.
    * `static` : Folder containing images.
    * `templates` : Folder containing html file.
    
* **wrangling_scripts**: Folder contaning a python module.
    * `wrangle_data.py` : Python module for wrangling data in order to generate plots for visualization

* **Procfile**: file that specifies the commands that are executed by the app on startup.

* **Visualizations**: This folder contains the plots generated using Plotly. These images are also displayed in the web application deployed on Heroku. 
    * `Arable_Land_Per_Person_in_2015.png`
    * `Arable_Land_Per_Person_1990_to_2015.png`
    * `Change in Rural Population.png`
    * `Rural Population Vs Forested Area.png`

* **requirements.txt**:  This file contains the list of python libraries needed to run this web application.

* **worldbank.py**: Python module that is called to run the application.

### Instructions:
Run the following commands in the project's root directory to set up your database and model.

    # To run ETL pipeline that cleans data and stores in database
      python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
      
    # To run ML pipeline that trains classifier and saves the model
      python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl

## Screenshots <a name="image"></a>

***Screenshot 1: Arable Land Per Person - 1990 to 2015***

![Screenshot 1](https://github.com/rahul385/Web-Application-World-Bank/blob/master/Visualizations/Arable_Land_Per_Person_1990_to_2015.png)

***Screenshot 2: Arable Land Per Person In 2015***

![Screenshot 2](https://github.com/rahul385/Web-Application-World-Bank/blob/master/Visualizations/Arable_Land_Per_Person_in_2015.png)


## Licensing, Authors, Acknowledgements <a name="licensing"></a>
This web application was developed as part of the [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025).

Author: Rahul Gupta Copyright 2020

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

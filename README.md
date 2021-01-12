# Web-Application-World-Bank

### Table of Contents
1. [Project Overview](#project)
2. [File Description](#file)
3. [Visualizations](#image)
4. [Licensing, Authors, and Acknowledgements](#licensing)


## Project Overview <a name="project"></a>
The objective of this web application is to create a data dashboard to track key metrics and trends using real data from World Bank [website](https://data.worldbank.org/indicator/SP.RUR.TOTL.ZS?view=chart).

## File Description <a name="file"></a>

* **data**: This folder contains real messages received during a natural disaster in csv format.
    * `API_AG.LND.ARBL.HA.PC_DS2_en_csv_v2`
    * `API_AG.LND.FRST.K2_DS2_en_csv_v2_9910393.csv`
    * `API_SP.RUR.TOTL.ZS_DS2_en_csv_v2_9948275.csv` : This python module takes csv files as input containing messages and categories (labels), cleans and processes the data and then exports it into a database table.
    * `API_SP.RUR.TOTL_DS2_en_csv_v2_9914824.csv` : The database file generated and saved after running python module "process_data.py"
    
* **worldbankapp**: This folder contains real messages received during a natural disaster in csv format.
    * `static` : This file imports the data from database table and trains a Machine Learnin model to classify messages among 36 different categories.
    * `templates` : The model generated and saved after running python module "train_classifier.py"
    * `__init__.py` : Python module to clean, normalize and tokenize the text.
    * `routes.py` : Python module to clean, normalize and tokenize the text.

* **wrangling_scripts**: This folder contains real messages received during a natural disaster in csv format.
    * `wrangle_data.py`

* **Procfile**: This folder contains real messages received during a natural disaster in csv format.

* **Visualizations**: This folder contains the images generated as part of analysis. These images are also displayed in the web application deployed on Heroku. 
    * `Arable_Land_Per_Person_in_2015.png`
    * `Arable_Land_Per_Person_1990_to_2015.png`
    * `Change in Rural Population.png`
    * `Rural Population Vs Forested Area.png`

* **requirements.txt**:  Jupyter notebook for process_data.py

* **worldbank.py**: Jupyter notebook for train_classifier.py

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves the model
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. The web application deployed on Heroku can be accessed through the below URL
https://web-app-worldbank.herokuapp.com/

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

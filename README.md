# Disaster-Response-Project
NLP (natural language processing) project to categorize types of disaster messages

The way to run this project is as follows:

1. Run process_data.py to export data to a database file
  - Give locations of messages and 
2. Run train.py to export machine learning model to pickle file
  - Give location of database file from process_data output
3. Run run.py to get web application 
  - Point location of pickle file from train.py output
  - Open separate terminal window and run env|grep WORK
  - From the output of that, put in the URL that will replace https://SPACEID-3001.SPACEDOMAIN

## Overview
The bassis of this project is to look at data provided by FigureEight. The data are tweets and texts that were sent during real world disasters and can be labeled into at least one of 36 categories. 

This project required 3 steps:
  1. Create ETL of data from CSV files and upload cleansed data to a database
  2. Write an ML algorithm to analyze messages and optimize model to correctly classify labels for that text
  3. Create web application that can show 3 graphs of overviews of the messages, as well as an input bar that could read a message and correctly classify what label it would fall under.
  
## Categories of messages (disaster_categories.csv)
CSV of categories of all messages (36 possible categories)

## Messages (disaster_messages.csv)
CSV of all disaster messages

## Database file (DisasterResponse.db)
Database file that is the output of the ETL section
  
  
## ETL Section (etl_pipeline.py)

The ETL section is the extract - transform - load process. Data were provided in CSV's that were read and merged together, then cleaned. 


## Machine Learning Pipelines (train.py)

After loading the data into a pandas dataframe, the data were broken up into the feature columns and the response columns, since there are 36 different response variables. 



## Web Application (run.py)

The web application shows 3 different bar charts: Genre frequency, top 5 response features, and the top 5 words most frequently used in the messages.

If you put in a message into the text bar, you can see what my model would predict of the 36 different feature variables. An easy one to use is "I really need some help!", which gets classified as Related, Request, and Aid Related.


## Project Proposal
We plan to use cannabis data from 2 sources on Kaggle -- one is a csv scraped from leafly.com (community ratings, descriptions, flavors) and another is sqlite database with multiple tables (Strains, Breeder, Medical info). 
We want to load selected data into a postgres database.
The resulting database could be used by casual smokers and cannabis patients / people in pain who want to explore different solutions to their conditions. 
Putting the medical ratings and casual smoker feedback side by side can also enable users to leverage our database to draw comparisons.


## Data Cleanup & Analysis

* Sources that we will extract from
    * [Cannabis CSV Data](https://www.kaggle.com/kingburrito666/cannabis-strains/downloads/cannabis-strains.zip/9)
    * [Cannabis Lineage, Growth, and Psych. Effects] https://www.kaggle.com/tictactouka/cannabis

* The type of transformation needed for this data (cleaning, joining, filtering, aggregating, etc): cleaning, joining

* Type of final production database to load the data into: Relational PSQL Database

* The final tables or collections that will be used in the production database: TO-DO


## Project Report

At the end of the week, your team will submit a Final Report that describes the following:

* **E**xtract: your original data sources and how the data was formatted (CSV, JSON, pgAdmin 4, etc).

* **T**ransform: what data cleaning or transformation was required.

* **L**oad: the final database, tables/collections, and why this was chosen.

Please upload the report to Github and submit a link to Bootcampspot.

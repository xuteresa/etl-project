## Project Report

### Overview and Guiding Questions
* Goals: 
   * Create an easy way for both patients / people in pain and casual marijuana smokers to explore different solutions to their conditions. 
   * Present medical rating data and casual smoker feedback side by side so that people can draw comparisons across the data in their search.
   
### Data Cleanup & Analysis Process
* **E**xtract: 
* Our original data came from two sources, one in a CSV file and another was a SQLite database with multiple tables.
    * [Cannabis CSV Data](https://www.kaggle.com/kingburrito666/cannabis-strains/downloads/cannabis-strains.zip/9)
    *   The data in this CSV came from Leafly.com, a cannabis supply website with educational content and reviews for various strains
    * [Cannabis Lineage, Growth, and Psych. Effects](https://www.kaggle.com/tictactouka/cannabis)

* **T**ransform: what data cleaning or transformation was required.
* From the SQLite database, we selected data that pertained to medical effects and medical rating
   * We grouped the effects by strain name and took an average of the medical rating to help reshape the dataset
* From the CSV file, we selected community-sourced effect descriptions and community ratings
* These selected columns were fitted into two summary tables, one for community vs. medical effects, one for community vs. medical ratings and filtered the dataset so that only strain names represented in both sources would be included in the final tables.
* Due to the filtering and joining process, our strain count dwindled down from 1000+ to 84
   * To provide additional value for users of this database, we created a third table with more descriptive columns from the community data source that included strain type, flavor, and description

* **L**oad: the final database, tables/collections, and why this was chosen.
* As mentioned above, our final tables consisted of the following:
   * Description (strain_name, type, flavor, description)
   * Effects (strain_name, community_effect, medical_effect)
   * Ratings (strain_name, community_rating, medical_rating)
* We chose to use a postgreSQL database to load our final tables to easily load the data.

### Learnings and Future Exploration
* Despite the original sources being quite vast with 1000+rows in each, the intersection between the two was much smaller, resulting in a smaller subset of comparable metrics.
* As a result, we created a third table for textual descriptions of a larger subset of cannabis strains so that in absence of comparison metrics, users can still explore the vast selection of strain
* If given more time, we would perform a more advanced analysis of the textual data available from our sources to draw comparisons between casual smoker descriptions of medical benefits and the actual medical effects of cannabis strains.


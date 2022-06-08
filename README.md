# Movies - ETL

## Overview

Amazing Prime Video is a platform for streaming movies and tv shows. The Amazing Prime Video team would like to develop an algorithm to predict which low budget movie being released will become popular so that they can buy the streaming rights at a bargain. Britta, a member of the Amazing Prime Video Team, has been tasked with creating the datasets for a hackathon. There are two data sources we will be looking at: 

* a scrape of Wikipedia for all the movies released since 1990
* rating data from the Movie Land's website

She'll need help with extracting the data from the two sources, transforming it into one clean data set, and loading that data set into a SQL table. The results of our data set can be seen in our ETL.ipynb file.

Once the dataset has been Extracted, Transformed, and Loaded, Britta would like us to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We have refactored the code from  our ETL.ipynb file in order to create one function that takes in three files - Wikipedia data, Kaggle metadata, and the MovieLens rating data - and performs the ETL process by adding the data to a PostgreSQL database. The results of our analysis can be seen below.

## Results

The focus of this assignment was to create a function that extracts, transforms, and loads data files into a SQL databse. This was accomplished by 

1. Importing our CSV & JSON files into DataFrames
2. Cleaning up the DataFrames by removing unnecessary columns / rows and reordering & renaming columns for ease of readibility
4. Using regular expressions to extract any necessary data
5. Merging our data into one dataset
6. Exporting our dataset into a PostgreSQL table

The two tables we exported into SQL were the _movies_ table and the _ratings_ table. Both tables were evaluated to ensure the correct number of rows were extracted into SQL. The _movies_ table successfully yielded 6075 rows of data while the _ratings_ table produced 26,024,289 rows of data. 

<img width="337" alt="movies_query" src="https://user-images.githubusercontent.com/101564349/172661224-ee558ce1-34a8-4c78-bfc4-b3ce33dcc2bf.png">

<img width="342" alt="ratings_query" src="https://user-images.githubusercontent.com/101564349/172661433-b74cfcd1-2f5a-458b-abd8-12d9f2dfe1f4.png">

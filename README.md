# Movies-ETL
In this git, I have created an automated pipeline that takins in new data, performs the appropriate transformations, and loads the data into existing tables. For this I used three files from Wikipedia, kaggle, and MovieLens and performed the ETL process. 

## Step 1: 
-- ETL_function_test file step by step: 
1. Created a function to read in three seperate files
2. Read in the Kaggle metadata and MovieLens ratings CSV files as Pandas DataFrames.
3. Opened the Wikipedia JSON file and use the json.load() function to convert the JSON data to raw data.
4. read in the raw Wikipedia movie data as a Pandas DataFrame.
5. use the code provided to return the three DataFrames.
6. use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
7. set the three variables in Step 6 equal to the function created in Step 1.
8. set the DataFrames from the return statement equal to the file names in Step 6. In this step, you are reassigning the variables created in Step 6 to the variables in the return statement.
Now to view that all our dataframes are correct use the .head() method to make sure your dataframes look correct(example below):
![image](https://user-images.githubusercontent.com/95777297/181646577-990639e0-058f-4684-a03c-bb3e604d9b7d.png)

## Step 2: 
-- Taking the Wikipedia Data and using the ETL_clean_wiki_movies.ipynb to Extract and Transform: 
1. Create the code for the clean movie function that takes in the argument "movie".
2. Add the function you created in step 1 that reads in the three data files.
3. Inside the function you created in step 1's python file, remove the code that creates the wiki_movies_df DataFrame from the wiki_movies_raw file, then write a list    comprehension that filters out TV shows from the wiki_movies_raw file.
4. Write a list comprehension to iterate through the cleaned wiki movies list that you created in Step 3.
5. Read in the cleaned movies list from Step 4 as a DataFrame.
6. Write a try-except block that will catch errors while extracting the IMDb IDs with a regular expression string and dropping any imdb_id duplicates. If there is an      error, capture and print the exception.
7. Write a list comprehension to keep the columns that have non-null values from the DataFrame created in Step 5, then create a wiki_movies_df DataFrame from the list.
8. Create a variable that will hold all the non-null values from the "Box office" column.
9. Convert the box office data created in Step 8 to string values using the lambda and join functions.
10. Write a regular expression to match the six elements of form_one of the box office data.
11. Write a regular expression to match the three elements of form_two of the box office data.
12. Add the parse_dollars() function.
13. Add the code that cleans the box office column in the wiki_movies_df DataFrame using the form_one and form_two lists created in Steps 10 and 11, respectively.
14. Add code that cleans the budget column in the wiki_movies_df DataFrame.
15. Add code that cleans the release date column in the wiki_movies_df DataFrame.
16. Add code that cleans the running time column in the wiki_movies_df DataFrame.
17. Use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
18. Set the three variables in Step 17 equal to the function created in Deliverable 1.
19. Set the wiki_movies_df equal to the wiki_file variable.
20. Add the columns from wiki_movies_df DataFrame to a list, and confirm that they are the same as this image:



# nosql-challenge

Part 1: Database and Jupyter Notebook Set Up

I used NoSQL_setup_starter.ipynb for this section of the challenge.

1. I imported the data provided in the establishments.json file from my terminal. I named the database uk_food and the collection establishments. 

2. Within my notebook, I imported the libraries you need: PyMongo and Pretty Print (pprint).

3. I created an instance of the Mongo Client.

4. I confirmed that I created the database and loaded the data properly:
        - I listed the databases in MongoDB and confirmed that uk_food is listed.
        - I listed the collection(s) in the database to ensure that establishments is there.
        - I found and displayed one document in the establishments collection using find_one and display with pprint.

5. I assigned the establishments collection to a variable to prepare the collection for use.



Part 2: Update the Database

I used NoSQL_setup_starter.ipynb for this section of the challenge.

The magazine editors have some requested modifications for the database before I can perform any queries or analysis for them. I made the following changes to the establishments collection:

1. I added the information for an exciting new halal restaurant that just opened in Greenwich to the database:

2. I found the BusinessTypeID for "Restaurant/Cafe/Canteen" and diplayed only the BusinessTypeID and BusinessType fields.

3. I updated the new restaurant with the BusinessTypeID I found.

4. The magazine is not interested in any establishments in Dover, so I checked how many documents contain the Dover Local Authority, and then removed any establishments within the Dover Local Authority from the database. I then checked the number of documents to ensure they were deleted.

5. Some of the number values are stored as strings, when they should be stored as numbers. I used update_many to convert latitude and longitude to decimal numbers.



Part 3: Exploratory Analysis

Eat Safe, Love has specific questions they wanted me to answer, which will help them find the locations they wish to visit and avoid.

I used NoSQL_analysis_starter.ipynb for this section of the challenge.

I answered the following questions:

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?

3. What are the top 5 establishments with a RatingValue of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0? 

For each question, I followed the guidelines below:

    - Use count_documents to display the number of documents contained in the result.

    - Display the first document in the results using pprint.

    - Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

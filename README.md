# noSQL-challenge

## Project
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, "Eat Safe, Love", to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles. 

## Project Tools
In this project, you will use your knowledge of noSQL databases to perform your activities. You will use Visual Studio Code, MongoDB (noSQL), and Jupyter Notebooks. In the analysis part of the project, use count_documents, pprint, and display the first 10 rows of a dataframe.

## Project Structure
This project is divided into three parts:

Part 1: Database and Jupyter Notebook set up
    * Import the data provided in the establishments.json file (found in the Resources folder)
    * Import the required libraries
    * Create an instance of Mongo Client
    * Confirm the database has been created correctly, and verify the data properly loaded
    * Assign the establishments collection a variable to prepare the collection for use

Part 2: Update the Database

 -- The magazine editors have requested some modifications to the database before you can perform any queries or analysis for them. Make the following changes to the establishments collection. 
    * An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis. 
        * Add the information listed in the Resources section to the database.
    * Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
    * The magazine is not interested in any establishments in Dover.
        * Check how many documents contain the Dover Local Authority.
        * Remove any establishments within the Dover Local Authority from the database.
        * Repeat the document c heck to verify the documents were removed.
    * Convert the appropriate fileds from string to decimals, using the Update_Many function.
    
Part 3: Exploratory Analysis

 -- "Eat Safe, Love" has requested specific information to help them identify those locations they wish to visit, and those they wish to avoid. Answer the following questions to provide them the require information. 

*Note 1* - Food Authority overall rating values range from 1-5. The higher the value, the better the rating. 
*Note 2* - The individual Hygiene, Structural, and Confidence in Management scores work in reverse. The higher the value, the worse the rating for these areas.

    1. Which establishments have a hygiene score equal to 20?
    2. Which establishments in London have a RatingValue greater than or equal to 4?
    3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
    4. How many establishments in each Local Authority area have a hygiene score of 0? 
        *Sort the results from highest to lowest, and print out the top ten local authority areas.

## Resources
----------------------------------------------------------------------------------------------------------------
```
{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}
```
----------------------------------------------------------------------------------------------------------------

### Collaboration
* Code debugging: ASU Learning Assistants & Xpert Learning Assistant (AI) Tool
* For latitude and longitude variable defintion troubleshooting: Classmate NG

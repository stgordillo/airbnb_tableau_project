# Tableau Project - Seattle AirBnB 2016
## Introduction

Hello and welcome to my first Tableau project. This won't be a deep dive like my Google Data Analytics Case Study, but rather a quick showcase of my Data Analytics skills focusing on Tableau.  

If you're interested in the final product or wanted to test things out for yourself, I have put the dataset linked at the bottom of the README.



## Data Sources

The Dataset used in this project was retrieved from the [Kaggle](https://www.kaggle.com/datasets/alexanderfreberg/airbnb-listings-2016-dataset) of Alex the Analyst, a Youtuber who specializes in educational videos for Data Analytics.



## Changelog & Cleaning

Below I describe, step-by-step the data cleaning and manipulation I performed to the dataset.  I combined 3 sheets into one data set for convenience when uploadiing to Tableau, "Calendar", "Listings", and "Reviews". After exploring the data and checking for duplicates, blanks, spellings mistakes and any other errors, it can be concluded that the dataset is pretty clean, although there is pretty of entries that won't be useful to us in a visualization.  The datasets were left untouched.



## Visualization Steps

**Bike Sales**  
  1. Used INNER JOIN on Tableau with Listings.ID and Calendar.Listing_Id and Listings.ID and Reviews.Listing_Id in order to match correctly
  2. 
  3. Copied all data to "Working Sheet".
  4. Used filters and conditional formatting to check for duplicates, blanks, spelling mistakes, etc.
  5. Checked the ID value lengths with =len.
  6. Used Find and Replace to change some data to make more sense when manipulating the data (changed m and s to married and single under Marital Status column and f and m to female and male under the gender column).
  7. Changed 10+ miles to More than 10 miles to make a future visualization easier to use.
  8. Added a new column Age Bracket and then entered the following nested formula referencing the Age column: =IF(L2>54,"Old",IF(L2>=31,"Middle Age",IF(L2<31,"Adolescent","Invalid"))).
  9. Created 4 pivot tables in the "Pivot Table" sheet using the data from "Working Sheet".  The pivot tables were for the average income of the customers by gender, the customer age bracket compared to whether or not they purchased bikes, commute distance compared to whether or not they purchased a     bike and one for specific ages.
  10. Created visualizations for the first three pivot tables referenced above.
  11. Copied the visualizations to the "Dashboard" sheet.
  12. Cleaned up the dashboard, created slicer filters and connected the filters to all three visualizations

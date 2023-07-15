# Tableau Project - Seattle airbnb 2016
## Introduction

Hello and welcome to my first Tableau project. This won't be a deep dive like my Google Data Analytics Case Study, but rather a quick showcase of my Data Analytics skills focusing on Tableau.  

If you're interested in the final product or wanted to test things out for yourself, I have put the dashboard linked at the bottom of the README.



## Data Sources

The Dataset used in this project was retrieved from the [Kaggle](https://www.kaggle.com/datasets/alexanderfreberg/airbnb-listings-2016-dataset) of Alex the Analyst, a Youtuber who specializes in educational videos for Data Analytics.



## Changelog & Cleaning

Below I describe, step-by-step the data visualization process I performed to the dataset.  I combined 3 sheets into one data set for convenience when uploadiing to Tableau, "Calendar", "Listings", and "Reviews". After exploring the data and checking for duplicates, blanks, spellings mistakes and any other errors, it can be concluded that the dataset is pretty clean, although there is plenty of entries that won't be useful to us in a visualization.  The datasets were left untouched, which meant that I had to exclude the null values and "0 room" values from appearing in my visualizations on each worksheet.



## Visualization Steps
  
  1. Used INNER JOIN on Tableau with Listings.ID and Calendar.Listing_Id and Listings.ID and Reviews.Listing_Id in order to match correctly
  2. The JOINS gave us about 23 million rows.  I tried to proceed to a sheet, but after quite awhile of waiting I decided to limit the scope down.
  3. I removed the Reviews sheet, since much of the data wasn't going to be worthwhile putting into a visualization.  I also removed the year 2017 that was included in this particular dataset.
  4. The first visualization, **Bar** was to look at the average price of an airbnb by location.  I put the Zipcode from measure names into columns and the sum(Price) value from Listings into rows.  I then changed the sum to avg and added color to the zipcode to make a bar chart.
  5. Next I created a new worksheet, **Map**, where I added the generated latitude and longitude values to the row and column, respectively.  I filtered by zipcode, gave the visualization color by zipcode that matched the previous visualization, and labeled the zipcode and avg(price) in the marks to create a map.
  6. Next I created a line chart, **Line**, by adding the date to the columns from the Calendar sheet and changing it from year to week and adding sum(price) value from the Calendar sheet as well.  They are filtered through SUM(price(Calendar)), YEAR(Date), and WEEK(Date).
  7. The next visualization was fairly simple, another bar chart called **Price per Bedroom**. I added the Bedrooms measure name to columns and avg(price) to rows, filtered by Bedrooms and labele the avg(price).
  8. My final visualization is called **Table** and is a simple table of the number of listings with a certain amount of bedrooms, from 1 - 6. I added Bedrooms to rows and the filter. I grabbed the Id from Listings and manipulated it to give me a distinct count to accurately and unique count of the listings by number of bedrooms.
  9. I then created a dashboard called **airbnb Dashboard**, added in all 5 of my visualizations and rearranged and resized them until I thought they were visually pleasing and next to visualizations that helped connect the ideas together. 

## Visualization Dashboard  

You can find all the visualizations on the dashboard made in Tableau here: [Seattle airbnb 2016 Tableau Project](https://public.tableau.com/authoring/TableauFullProject_16893141253750/Dashboard1/airbnb%20Dashboard#1)

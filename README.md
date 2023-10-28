# Understanding the impact of Tony Award outcomes on Broadway Productions

This is a project where I plan to study the impact of the Tony Awards on the financial success of Broadway productions, and how this relationship has changed over the last 40 years.

## Author: Maximilian Wisnefski
email: wisnef_m1@denison.edu

### prerequisites
To run all of the code for this project, one needs:
- R (version 4.1.1)
  - packages needed: ggplot2, dplyr, (will add more as necessary)
- Python (version 3.9)
  - packages needed: requests, BeautifulSoup, io, etree, urllib.request, urllib, re, string, datetime, pandas, numpy, selenium, webdriver, Keys, ast, (will add more as necessary)
- SQL (might not actually end up using SQL)


### data
All data is web scraped from the Internet Brodway Database, also known as the IBDB (Broadway League, 2023). The data was collected and curated by The Broadway League. While the IBDB has a large amount of data, such as information about specific actors, composers, producers, performance venues, etc., for the purposes of this research, I am only interested in the following data: 

1. <ins>Nominations:</ins> the number of Tony Awards a production was nominated for in a given year
2. <ins>Wins:</ins> the number of Tony Awards a production won in a given year
3. <ins>Year:</ins> the year the production was eligible for Tony nominations
4. <ins>Type:</ins> the type of show the production was (play, musical, special)
5. <ins>Production:</ins> the name of the production
6. <ins>Weekly gross:</ins> the amount of money a production grossed in a given week
7. <ins>Date:</ins> the date of a week in a production’s run
8. <ins>Capacity:</ins> the percentage of seats that were filled in a given week for a given production

The data are split into two .csv files. One contains weekly gross and capacity data for every production being considered (weekly_data.csv, variables 5-8). The other contains the number of nominations and wins received for every production being considered (tony_data.csv, variables 1-5). The former dataset has 54,134 rows, and the latter has 1,081 rows. You can find these .csv files in the [data](https://github.com/MaxWisnefski/Tony-Award-Data-Analysis/tree/main/data) folder.

database APA citation: The Broadway League. (2023). Internet Broadway Database. https://www.ibdb.com/


### code files 
- IBDB_data_collection.ipynb: This notebook is for web scraping data from the IBDB.
- initial_Tony_analysis.Rmd: This R markdown file contains my early analysis. Specifically, it contains the following:
  - summary statistics about my data
  - multiple linear regression model that uses number of nominations and number of wins as predictors for production longevity (i.e. the number of weeks a production stays open)
  - visuals depicting the relationship between nominations/wins and longevity
  - two time series graphs deciting how the weekly grosses of two musicals changed based on the outcome of Tony nominations/wins 

### other info

# Understanding the impact of Tony Award outcomes on Broadway Productions

In this project, I study the impact of the Tony Awards on the financial success of Broadway productions, and how this relationship has changed over the last 40 years.

Hypotheses:
1. Winning Tony Awards improves a production’s financial performance in the 5 weeks following the ceremony. After those 5 weeks have passed, the effect will begin to diminish.
2. Failing to receive nominations or failing to win after being nominated has the opposite effect on a production's financial performance in the 5 weeks following the ceremony.
3. The Tony Awards are less impactful now than they were in 1980. Therefore, while the award outcomes still matter, productions are more likely to succeed without winning awards than they used to be, and productions that win awards do not benefit to the extent that they used to. 


## Author: Maximilian Wisnefski
email: wisnef_m1@denison.edu

### prerequisites
To run all of the code for this project, one needs:
- R (version 4.1.1)
  - packages needed: ggplot2, dplyr, tidyverse, car, magrittr, ggpubr, segmented
- Python (version 3.9)
  - packages needed: requests, BeautifulSoup, io, etree, urllib.request, urllib, re, string, pandas, numpy, selenium, webdriver, Keys, ast


### data
All data are web scraped from the Internet Brodway Database, also known as the IBDB (Broadway League, 2023). The data were collected and curated by The Broadway League. While the IBDB has a large amount of data, such as information about specific actors, composers, producers, performance venues, etc., for the purposes of this research, I am only interested in the following data: 

1. <ins>Nominations:</ins> the number of Tony Awards a production was nominated for in a given year
2. <ins>Wins:</ins> the number of Tony Awards a production won in a given year
3. <ins>Year:</ins> the year the production was eligible for Tony nominations
4. <ins>Type:</ins> the type of show the production was (play, musical, special)
5. <ins>Production:</ins> the name of the production
6. <ins>Weekly gross:</ins> the amount of money a production grossed in a given week
7. <ins>Date:</ins> the date of a week in a production’s run
8. <ins>Capacity:</ins> the percentage of seats that were filled in a given week for a given production
9. <ins>Weeks open:</ins> On any given week in a production's run, the number of weeks since it played its first performance. Note that this variable was not originally in the data and was created in main_Tony_analysis.Rmd 

The data are split into four .csv files. The first two contain the raw web scraped data. One contains weekly gross and capacity data for every production being considered (weekly_data.csv; variables 5-8; 55,318 rows). The other contains the number of nominations and wins received for every production being considered (tony_data.csv; variables 1-5; 1,552 rows). 

The second two were created in initial_Tony_analysis.Rmd. The first contains variables 1-8 and is filtered to only include the productions that are relevant to the analysis. Variables have also been wrangled to make them easier to work with (combined_filtered.csv; 47,396 rows). The second is combined_filtered.csv grouped by production with a new column called "weeks." This column contains the total number of weeks a production stayed open (production_longevity.csv; 837 rows). 

You can find these .csv files in the [data](https://github.com/MaxWisnefski/Tony-Award-Data-Analysis/tree/main/data) folder.

database APA citation: The Broadway League. (2023). Internet Broadway Database. https://www.ibdb.com/


### code files 
- IBDB_data_collection.ipynb: This notebook is for web scraping data from the IBDB.
  - produces weekly_data.csv and tony_data.csv
- initial_Tony_analysis.Rmd: This R markdown file contains all early analysis. Specifically, it contains the following:
  - summary statistics about the data
  - multiple linear regression model that uses number of nominations and number of wins as predictors for production longevity (i.e. the number of weeks a production stays open)
  - visuals depicting the relationship between nominations/wins and longevity
  - two time series graphs deciting how the weekly grosses of two musicals changed based on the outcome of Tony nominations/wins
  - data filtering/wrangling to make the data eaiser to work with
  - several visuals for final paper
  - produces combined_filtered.csv and production_longevity.csv
- main_Tony_analysis: This R markdown file contains the remainder of my analysis. Specifically:
  - splits the data by year and performs the same multiple regression model as the previous .Rmd for each year of data separately
  - adds "weeks open" variable to combined_filtered
  - moderated multiple regression to look at relationship between wins/nominations and weekly capacity (for all data)
  - ^ repeats this process for every year of data separately
  - segmented regression (not included in final analysis)
  - several visuals for final paper

### visuals
The [visuals](https://github.com/MaxWisnefski/Tony-Award-Data-Analysis/tree/main/visuals) folder contains 8 visuals for the final paper. Specifically, it includes all of the panel plots created for the final paper.

### other info
I was not paid to do any of this work, and I have no vested interest in finding particular kinds of results. 

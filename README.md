# Understanding the impact of Tony Award outcomes on Broadway Productions

This is a project where I plan to study the impact of the Tony Awards on the financial success of Broadway productions, and how this relationship has changed over the last 40 years.

## Author: Maximilian Wisnefski
email: wisnef_m1@denison.edu

### prerequisites
To run all of the code for this project, one needs:
- R (version 4.1.1)
  - packages needed: ggplot2, dplyr, (will add more as necessary)
- Python (version 3.9)
  - packages needed: requests, BeautifulSoup, (will add more as necessary)
- SQL (might not actually end up using SQL)


### data
All data is web scraped from the Internet Brodway Database, also known as the IBDB (Broadway League, 2023). The data was collected and curated by The Broadway League. While the IBDB has a large amount of data, such as information about specific actors, composers, producers, performance venues, etc., for the purposes of this research, I am only interested in the following data: 

1. <ins>Nominations:</ins> the number of Tony Awards a production was nominated for in a given year

2. <ins>Wins:</ins> the number of Tony Awards a production won in a given year

3. <ins>Production:</ins> the name of the production

4. <ins>Weekly gross:</ins> the amount of money a production grossed in a given week

5. <ins>Date:</ins> the date of a week in a production’s run

6. <ins>Capacity:</ins> the percentage of seats that were filled in a given week for a given production

The data are split into two .csv(?) files. One contains weekly gross and capacity data for every production being considered (variables 3-6). The other contains the number of nominations and wins received for every production being considered (variables 1-3). The former dataset has _____ rows, and the latter has _____ rows (<b> will return to this later </b>).

database APA citation: The Broadway League. (2023). Internet Broadway Database. https://www.ibdb.com/


### code files 
none currently

### other info

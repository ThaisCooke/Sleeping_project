# Sleeping_project
Report of sleeping patterns.

The App "Sleep Watch" was used to collect data of my sleeping patterns. This data was collected for three months. The table was created on Excel and imported to SQL for analysis and Tableau for Visualization. 

This project is to check the correlation between a good night sleep and restfulness, and the factors that contribute to a restful night.

The thought process is documented here, and all the coding can be found above

<p>&nbsp;</p>

## Questions to be answered

1. What is the average sleep (in hours) that I had during this period of time?
2. How does the average sleep (in hours) compares to the fatigue during the day?
3. How does sleep disruption percentage relates to fatigueness during the day?
4. What is the main sleep disruption factor that has been recorded in this period of time? 
5. What is the main factor (in percentage) that made me lose sleep and impacted the restdness when waking up the most 
  (or the fatigueness during the day)?
6. Create a SP to play with parameters and answer: How does three day sleep target relates to fatigueness during the day?
7. Does working out helps for better night sleep?

<p>&nbsp;</p>

## Clean the data

I considered any percentage of sleep disruption that was above 0.05 as a night classified as "Difficult Staying Asleep".
I Started by fixing the "Difficult staying asleep", which should be "1" if the percentage of lost sleep is more than 5%.
To find those dates, I did the following:

#####  To fix "Difficult staying asleep", and replace "0" by "1", first I had to check which dates needed to be altered
1. The records needed to be updated. The UPDATE statement was used
2. Check the query
3. There was a typo on the table. The table said "Completed Rested" instead of "Completely Rested". The UPDATE statement was used again.

##### Decide what to do with NULLS

1. I decided to delete those rows instead of trying to populate it, since there was no data recorded for all the fields. The DELETE statement was used
2. There was one "NULL" on day 05-13-2023. That was replaced by the data for that day, which had been documented in the app, but not properly entered


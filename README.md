# Sleeping_project
Report of sleeping patterns.

The App "Sleep Watch" was used to collect data of my sleeping patterns. This data was collected for three months. The table was created on Excel and imported to SQL for analysis and Power BI for Visualization (coming soon :construction: :hammer:)

This project is to check the correlation between a good night sleep and restfulness, and the factors that contribute to a restful night.

The thought process is documented here, and all the coding can be found in the folders on this project
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

<p>&nbsp;</p>

## Answers to the questions:

##### 1. What is the average sleep (in hours) that I had during this period of time?

7.78 hrs

##### 2. How does the average sleep (in hours) compares to the fatigue during the day?

On the days where there was no fatigueness during the day, the average sleep was 8.47 hr vs 7.26 hr on the days where there was a lot of fatigueness during the day

##### 3. How does sleep disruption percentage relates to fatigueness during the day?

On average, the sleep disruption was about 8,12% when the fatigueness was recorded as "Completely Fatigued" vs 1% when the fatigueness was recorded as "Not at all Fatigued". It looks like sleep disruption has a big impact on the fatigue in the next day.

##### 4. What is the main sleep disruption factor that has been recorded in this period of time?

Disrupted by noise has had the most occurrencies (45 in total), followed by disrupted by caregiving (37 occurrencies)

##### 5. What is the main factor (in percentage) that made me lose sleep and impacted the restdness when waking up the most (or the fatigueness during the day)?

Disrupted by noise was the main factor associated with the difficulty staying asleep and restdness when waking up (16.49%), followed by Disrupted by Caregiving (14.43%)

##### 6. Create a SP to play with parameters:

This was to practice SP and their uses. Check code. The conclusion was when the three day sleep target is 'On Target', it shows that most of the days 
restdnessis up and fatigue during the day is low

##### 7. Does working out helps for better night sleep?

It seems to be no correlation between working out and a better night sleep. The number of days were the same, regardless of the level of fatigueness and restdness

<p>&nbsp;</p>

## Conclusions:

* The amount of sleep time impacts the fatigueness during the day, but also the sleep disruptions play a big role in it
* Most of the sleep disruptions were caused by noise or caregiving
* Three consecutive good night sleep is important to feel overall not fatigued during the day

<p>&nbsp;</p>

## Recommendations:

* Go to bed at a reasonable time
* Sleep with earplugs or white noise machine, or move to another room to avoid noise disruption
* Wait for my kids to grow to sleep throught the night :laughing:
* When having a bad night sleep, try to make up for it the next night. The fatigueness can last for up to three days

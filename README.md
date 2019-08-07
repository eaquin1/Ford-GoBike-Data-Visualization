# Ford GoBike Data Visualization
## by Emily Aquin


## Dataset

Using the Lyft app, you can rent a bicycle in the Bay Area. Within a service area, you can pick up and drop off a bicycle, based on your current needs. This project analyzes the data collected from users of the GoBike program, for 2017 and 2018. The data can be found at https://www.lyft.com/bikes/bay-wheels/system-data. 

The dataset includes:
* an ID number for each bicycle
* how long it was rented for, in seconds
* the beginning and end staton ID, latitude, longitude and station name
* the start and end time
* the year the user was born
* the gender of the user
* whether the user has a subscription to the service or not
​
There are 2252058 rows and 15 columns.

There was some cleaning needed to the dataset. This included: 
* Deleting the rows without gender or birth year
* Only use ages that are reasonable. Check for abnormally old or young values and remove them
* Change data types, including times to datetimes, and user_type and member_gender to categories
* Extract months and days of the week from start_time
* Create a column for distance in kilometers, based on the longitude and latitude start and end points (feature engineering)

## Summary of Findings

First, I discovered that 89% if the user type is subcriber, and only 11% are customers. 

The mean age is 35.4 years old, and after cleaning the data, the oldest age is 80 years old, and the youngest is 18 years old. 

The majority of the riders are male, at 74%. 24% are female and 1% identify as other.

The winter months have the fewest rides. The number of rides continues upwards throughout spring and summer, with the most popular being in September and October. Then, the frequency of rides goes back down again. This is true for both customers and subscribers, and all genders.

Subscribers predominately use the ride service on Monday through Friday, while customers ride the most on the weekends. This is most likely due to subscribers using the service to commute to work, while customers use the bikes on an occasional basis for something unusual in their schedule. This also applies to all genders, when analyzing the multivariate plots.

A line graph shows that the oldest riders had the greatest fluctuation between the shorest and longest rides.
Of course, it is possible for the rider to not take a direct trip from the starting to ending locations, and to deviate from a straight course. However, it is worthwhile to understand how far away the starting and ending locations are from each other.


## Key Insights for Presentation

For my presentation, I will focus on the difference in usage for customers and subscribers. On the later plots, I will show how gender also comes into play. I will first show the univariate results, such as usage on days of the week, and usage over months. I will then continue to see how adding more variables influences the results. My conclusion is that whether a user is a customer or a subscriber has the biggest influence on results, compared to gender. 
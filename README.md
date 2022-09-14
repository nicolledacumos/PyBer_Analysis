# PyBer_Analysis

## Analysis Overview
This analysis presents collected ride-sharing data by city type -- rural, urban, and suburban -- through a summary DataFrame coded with python and utiiling Pandas and Matplotlib formatting to ceate a line graph that presents specific ride far data by city type. 

## Deliverable 1
### Create a ride-sharing summary DataFrame by city type

In order to create a summary DataFrame including the following data:
- Total number of rides for each city
- Total number of drivers for each city
- Sum of the fares for each city
- Average fare per ride for each city type
- Average fare per driver for each city type

I first had to collect the data for each category using the groupby() function to create an index, count() to find the number of rides, and count() to find the total drivers and sum of fares. Additionally, the fare per ride average was calculated by dividing the sum of the fares by the total number of rides; the fare per driver average was found by dividing the total sum of fares by the total number of drivers.

![Screen Shot 2022-09-14 at 2 14 25 PM](https://user-images.githubusercontent.com/110862583/190242538-1dedf827-9933-4549-a4a1-cae523ee6e38.png)
![Screen Shot 2022-09-14 at 2 14 41 PM](https://user-images.githubusercontent.com/110862583/190242575-bcbbc93a-2648-4993-aa36-71b120a17292.png)

From there, I was able to create a summary dataframe outlining the calculated data from above, and I formatted the dataframe in order to present a clear DataFrame.

![Screen Shot 2022-09-14 at 2 15 55 PM](https://user-images.githubusercontent.com/110862583/190242829-48dcb068-78eb-4682-9843-88964b521aa5.png)

## Deliverable 2
### Create a multiple line plot that shows the total weekly of the fares for each type of city

To create a multiple line plot displaying the total fares for each type of city per month, I had to use the groupby() funciton to show the the sum of the fares for each date -- indexed using city type and date. 

![Screen Shot 2022-09-14 at 3 13 10 PM](https://user-images.githubusercontent.com/110862583/190253054-43cdccef-e41d-4c78-b831-8ff1bd1c0506.png)

Then, I created a pivot table based on the DataFrame, from which I created a new DataFrame with a loc on the dates "2019-01-01':'2019-04-29" in order to only show data up to April 29, 2019. 

![Screen Shot 2022-09-14 at 3 13 58 PM](https://user-images.githubusercontent.com/110862583/190253177-e2dfe7d1-403d-4963-ab90-89ba14a7b193.png)

I then resampled the data using resample() by week 'W' to display the sum of the fares per week.

![Screen Shot 2022-09-14 at 3 14 20 PM](https://user-images.githubusercontent.com/110862583/190253239-69c4713d-15aa-4c9f-98e5-0afb052a9ace.png)

Finally, I created the summary line graph by plotting the resampled data with the df.plot() function, imported the graph style from Matplotlib and formatted the graph so that it included X and Y axis labels, a leged, a title, and was larger. I then saved the graph to my analysis folder.
![Screen Shot 2022-09-14 at 3 17 30 PM](https://user-images.githubusercontent.com/110862583/190253826-c31eacfa-3f73-4d8d-ac01-72716f4687e3.png)

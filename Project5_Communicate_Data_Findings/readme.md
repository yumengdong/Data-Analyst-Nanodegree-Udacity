# Ford GoBike System Data Exploration
## by Yumeng


## Dataset

This data consisted of Ford GoBike System of year 2018. Ford GoBike is a bicycle sharing system in the San Francisco Bay Area. There are 1396765 trips information in this dataset. 
The features in the dataset include trip duration (second), trip start and end time, trip start and end location, user type, user birth year and user gender, etc. The data can be found [here](https://www.fordgobike.com/system-data)

During the data wrangling process, some unneeded variables were removed and some new variables were created to help investigate the dataset effectively.


## Summary of Findings

There are some inaccurate trip duration data and member birth year data. I looked at the interquartile range and truncate the inaccurate data but also ensure that large enough data is kept. <br>
The trip duration is my feature of interest in this project. Its distribution is right skewed. The trip duration distribution looks differently by different user type groups (Subscribers and Customers). <br>
Overall, the most common trip duration is between 5 – 10 minutes, and these trips coming from 23 – 38 years old users. This pattern looks a bit noisy during midnight (0am to 5am), but look much obvious after 5am. The number of trips decreases with trip duration increases, and user age increases.<br>
During weekends, the mean trip duration gradually increases from 8am and reaches the peak at 1pm. Then it starts to decrease. During workdays, we can see an obvious peak around 8am, and a less obvious peak around 5pm.<br>

Outside of the main feature of interest, the plots depict that most of the trips are from the Subscribers. Subscribers have much more trips around 8am and 5pm, and more trips during workdays than weekends. The trips from the Customers, however, has a uniformly distribution with no obvious peak at different time of day or days of week. 



## Key Insights for Presentation

In the presentation, one of the threads is to show readers how the trip numbers and trip duration patterns look differently between 2 groups of user type, Subscribers and Customers. Because the large percentage of trips are from Subscribers, Customers bike ride behavior will be invisible if we don’t look at the trips by user types. <br>
I used box plots and violin plots to depict how the Subscribers and Customers’ trips look differently. Then I threw out an assumption that Subscribers use bike for commute and Customers use bike for commute, fun, leisure, all different kinds of purposes. <br>
Later, I used bar plots to show trips at different time by user type to support my previous assumption. <br>
Another thread is to tell readers how the trip duration is correlated to different time of day and different days of week. I used point plot to show mean trip duration vs time by different week days to make this message clear and effective. 

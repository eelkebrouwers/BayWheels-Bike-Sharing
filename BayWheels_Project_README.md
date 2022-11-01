# Bay Wheels bike sharing 2019
## by Eelke Brouwers


## Dataset

The dataset contains data from Bay Wheels on bike sharing in greater Fransisco Bay area. The company was established in 2013 and operate under different names, starting with Bay Area Bike Share, then Ford GoBike in June 2017 and eventually they became Bay Wheels in June 2019. Data on their bike sharing system are available online at https://s3.amazonaws.com/baywheels-data/index.html, where they share data on the duration of trips, information on the start and end station (including id, name, latitude and longitude), bike id, user type (costumer/subscriber) and rental access method (app/zipper). Through Udacity I also obtained data on the age and gender of users, but only for the month February. 

In this report I analyzed the data from 2019, focussing on the frequency and the duration of bike trips throughout the day, week and year, and for different user types (age, gender and customer/subscriber). 


## Summary of Findings

__When are the bikes used most and by who?__

Most bike trips are made during the week (82.5%), and more specifically during morning and evening rush hours (8am and 5 pm respectively). Of the trips made on weekends most start between 11am and 4pm, peaking at 2pm. This pattern is consistent throughout the year, although the absolute frequencies differ. In March the bikes are used most, after which April and October. December is the month with the least trips. The data indicate that the bikes from Bay Wheels are often used for going to work (whether to the public transport station or directly to the office), even during the holiday months. 
A majority of the users in 2019 (80.4%) was a subscriber, the rest a customer. While both subscribers and customers mainly use the bikes during the week, the percentage of customers that use the bike during the weekends is higher than for subscribers. From the available data on gender 74.6% was male, 23.3% female and 2.1% were defined as 'other'. Although the users are mainly male, the moments they use the bikes seem not different from female. Both make most trips during the weekdays and rush hours. Their mean age was 34 years, with a minimum age of 18 and a maximum age of 80*. To access the bikes most people used the app instead of the clipper (88.9% versus 11.1%). 

*Age data were not normally distributed and contained some outliers at the upper end, including age 140. Data over 80 were considered outliers and removed from analysis

__Does the duration of trips differ depending on the hour, day, month, or on the type of user?__
The mean duration of bike trips in 2019 was 12.7 minutes, with a minimum of 1 and a maximum of 1293 minutes. As trip duration data were log normally distributed and contained some possible outliers to the far end that were difficult to define, the interaction of trip duration with other variables has been performed on dataframes both with and without outliers (based on the IQR method). 
Trip duration did not seem very strongly correlated with any of the other variable, but nevertheless some interesting patterns were observed. Depending on the hour of the day and the day of the week trip duration seems to change. However, the exact change has been difficult to interpret as data with and without outliers give contradictory results. Maintaining the dataset as is, so including possible outliers, the average bike trip seems to be longest between 11am and 3pm (outside of the long bike trips made during the night). This is irrespective of the day. Discarding outliers changes the pattern for weekdays completely, with the on average longest bike trips seen at rush hours (8am and 5pm). 
Of the different bike users, customers seem to make on average longer trips than subscribers, regardless of the day. On weekends this effect is even a little stronger. On average, bike trips made by male users seem to be slightly shorter than for female users, which is consistent over the entire month of February. The duration of bike trips does not correlate with age. 


## Key Insights for Presentation

- Bikes are most frequently used during weekdays, and more specifically in the morning and evening rush hours (8am and 5pm respectivily). On weekends most trips are started between 11am and 4pm, peaking at 2pm. Seen throughout the year, the months March, April and October are the months with the most trips, while the least trips are made during December. 

- The duration of trips fluctuates throughout the day, but the direction of this fluctuation is complicated as appears from comparing dataset including and excluding outliers. 

- Customers make on average longer bike trips than subscribers, especially on weekends. 
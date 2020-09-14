## Booz Allen Hamilton Hackathon 2020 - Challenge 1: Watershed Restoration Case Study 
### Project Authors: 
* Jen-Li Chen - [LinkedIn](https://www.linkedin.com/in/JenliChen)
* Marina Baker - [LinkedIn](https://www.linkedin.com/in/bakermarinam/)
* Bryan Lange - [LinkedIn](https://www.linkedin.com/in/bryanrobertlange)

# 2020 Chesapeake Bay Hackathon _Hack the Bay_ 
* Jen-Li Chen - [LinkedIn](https://www.linkedin.com/in/JenliChen)
1. Introduction

The Chesapeake Bay watershed is home to over 18 million people, spanning 6 states and Washington DC. The Bay is the largest estuary in the United States, providing 500 million pounds of seafood harvest each year. Declining water quality due to pollution and overharvesting in past decades led to poor ecosystem health and the near extinction of economically and culturally important aquatic species. In response to this decline, state and federal partners have invested heavily in restoration efforts, amounting to nearly 1.5 billion of state and federal funding in 2019 alone. Despite many years of costly efforts, warming temperatures, sea level rise, and increasing precipitation due to climate change have hindered the attainment of restoration goals. ([Citation](https://devpost.com/software/enabling-climate-resiliency-for-the-chesapeake-bay))

2. Data Collection

I chose __Water Temperature__ as the indicator. I used the CMC and CBP water quality data set provided by Booz Allen Hamilton. 
For the water temperature, all of the filtered data sets for the analysis and visualization are from the CMC dadabase.
([Link to the raw data](https://github.com/jenli810006995/hack-the-bay))


3. Data Preprocessing

    * Year: I used Python pandas to trim date and time elements from the __Date__ parameter, and filtered 2015 - 2020 as the time window I am interested in.
    * Season: I categorized May to August as __Summer__ , and November to February as __Winter__.
    
4. Exploratory Data Analysis

    * Methodology:
    
    1. Stationality: 
        Use AF, PACF and Augmented Dickey–Fuller test to check stationality. The water temperature is stationary time-series data. ([Citation](https://github.com/marbakes/pca-arima-fun/blob/master/Data%20Processing%20%26%20Modeling.ipynb))
    
    2. Summary Statistics: 
        After plotting water temperature within 2015 to 2020, I found the temperature range for the winter has something interesting to look at. Especially after 2017. For Example, the following scale of the winter water temperature reveals the increasing range:
    
    ![2017 Winter](https://github.com/jenli810006995/Hack_the_Bay_Repo/blob/master/Images/2017_winter_cbp_range.jpg)
    ![2018 Winter](https://github.com/jenli810006995/Hack_the_Bay_Repo/blob/master/Images/2018_winter_cbp_range.jpg)
    ![2020 Winter](https://github.com/jenli810006995/Hack_the_Bay_Repo/blob/master/Images/2020_winter_cbp_range.jpg)

5. Data Visualization

   * I created a seasonal overview dashboard in Tableau, using year, season and state parameters to invite end users to take a look at the data set.
   Additionally, With Tableau's geospatial mapping feature, I was able to check on the land use in the above region, The Yellow Breeches Creek in Pennsylvania, 
   which is a commonly fishing resort ([Reference](https://www.orvis.com/fishing_report.aspx?locationid=6015))
   
   * [Tableau Youtube Demonstration](https://jenli810006995.github.io/)
   * [![](http://img.youtube.com/vi/HbeXM46JjAo/0.jpg)](http://www.youtube.com/watch?v=HbeXM46JjAo "2020 Chesapeake Bay Hack the Bay Hackathon Data Visualization")

6. Challenges

   * Not all the states in the Chesapeake Bay area have comprehensive data in the 5-year window. 
   * Most data sets are in large magnitude, and hope to be able to access data sets in the FTP in the near future

7. Recommendation

   * Due to the time limit, I had not yet got time to dig into the residents occupation, conductivity, recreation and harvesting products in the Yellow Breeches Creek in Pennsylvania. From the satellite iamges, I saw most of the land use there is in agriculture. I assume agriculture and fishing might be the major land and water use there. 
   * I should have checked out on the data collection time in the specific region, as well as weather condition.
   * I had not checked on the air temperature and should have mapped a confusion matrix to check on the correlation between the air temperature and the water temperature.

8. Conclusion

    In conclusion, I was super thrilled to be able to touch on this topic and have a chance to look at the data sets, read the background documents, and work with my great teammates in the 2020 Hack the Bay Hackathon. Since the state and federal restoration efforts and funding have poured in since 2019, in the summer in 2020, the water temperature did not show high deviation from the previous year, though the winter temperature had several outliers. The top 2 highest degree are in Pennsylvania, and third highest is in Maryland. However, the highest one is 43 degree Celsius, while the second and the third are 26 and 24 degree Celsius. On the "Yellow Breeches Creek, Pennsylvania Fly Fishing Reports & Conditions" website, it did mention about high water temperature, but it stated the water quality is good. As a result, I propose the 43 degree Celsius in the winter might not be a typo from data collection. I look forward to expand this case study further in the days to come.

---

## :ocean: Keep it on the Loudoun :ocean:
- After looking at benthic macroinvertebrate health it became apparent that Loudoun County in Virginia had conisistently poor ratings over time and continues to decline in quality. 

![Loudoun_PowerBI](https://github.com/Bryan-Lange/Hack-the-Bay-Project/blob/master/images/Loudoun_pbi.png)

- Research revealed that Loudoun is one of the 20 fastest growing counties in the U.S. and this population increase impacts stream and river health. These waterways flow directly into the Potomac River and affect neighboring areas.
- The benthic data was not always collected from the same areas at the same time of year, so trying to accurately pinpoint clear declines or improvements was a challenge in itself 

## :droplet: Target Deliverables :droplet:

- Visualization that tells a story about water quality and surrounding land use over time:
![Power_BI](https://app.powerbi.com/groups/me/reports/1802a5ff-c902-49d1-939a-ddbf52db966a/ReportSection)
# oahu_weather_analysis

## Purpose

We were approached by a client looking to open a surf & ice cream shop on Oahu, Hawaii.  The client had already gathered weather data taken from weather stations throughout the island, and asked to to analyze the data for overall trends regarding temperature, precipitaiton, specific weather station (one with the most data), and aggregate results from the months of December and June. 

## Resources
- python
- pandas
- jupyter notebok
- flask
- sqllite
- sqlalchemy
- matplotlib (style: fivethirtyeight)
- numpy
- hawaii.sqlite (weather data for Oahu)

## Process

- The initial analyis looked at the year from 8/23/2016 - 8/23/2017, from this we saw that temperature and precipitation ranges varied per month, and we needed to get granular with the data to explore specific trends within a month, regardless of the year. (We needed, for example, to pull all data for june or decemer, and analyze based on the historical data per month, rather than focusing on a single year)
- Our client decided that june and december were the two months he wanted us to look at, which made sense as they are 6 months apart, and each are the start of summer and winter respectively.
- To do this, we pulled all june/december data separately to analyzie measures of central tendency, to determine any outlying factors.  We focused mainly on temperature as that is what our client asked for.

## Results / Findings

June Temperature data
<img width="172" alt="Screen Shot 2022-06-15 at 4 04 13 PM" src="https://user-images.githubusercontent.com/6634774/173917056-428065c3-37e5-4644-b126-359077de6fb1.png">

December Temperature data
<img width="164" alt="Screen Shot 2022-06-15 at 4 05 01 PM" src="https://user-images.githubusercontent.com/6634774/173917160-224a7e69-fbf4-4e96-bd86-2a77139ad7c0.png">

1. Firstly, we noticed a slight descrpancy in the total number of temperate(tobs) data we had by ~200 data points, we took this in stride and deiced that this would probably not skew our analysis, so we proceeded as normal.
2. Mean temperatures: June(74.9), December(71.0), this makes sense as June is in the summer and December is in the winter, the change in mean is not drastic, which would indicate that the general climate for these two time periods does not swing too drastically.  This could mean equal (or close to) amount of success regardless of the time of year (based on TEMP only).
3. Min/Max: June(min:64/max:85), December(min:56/max:83), again this data makes sense based on the time period and the general tropical climate of the Hawaiian islands.  The min and max temperature differences indicate that during December, it would seem that the lows are significatnly lower than the lows for June, but the max temperatures remain fairly close.  Again, I would suggest that our client monitor the temperature and if/when it drops below 60, they may want to consider shortening hours or closing the shop entirely.  
4. STD(standard deviation): June(3.26), December(3.75), this indicates that during December there will be a greater variation in temperatures throughout the month, thus the client should maintian a watchful eye on the forecast (in terms of temperature) to decie if/when to stay open during the month of december.  

## Further suggestions (more data is needed)
1. Weather data is great, but there is no correlation as to the temperature/precipitation and the amount of ice cream sold.  We can reasonably assume that lower temp & higher precipitation yields less ice cream sales, thus (logically), a tropical environment would be great location for a surfing/ice cream shop; however, finding a study that actually correlates temp/precip to ice cream habits would yeild even greater analysis on when to close/open the shop. 
2. Surfing trends of various beaches in oahu:  Selecting a location will be paramount to this businesses success, without surfing trends/data from the beaches of Oahu, the client will be going in slightly blind on where to set up shop.  If we gathered/found/monitored surfing trends over the course of the year(s) for select Oahu beaches, our client would be able to make a better decision on where to set up their business AND when to stay open/close during the (slighty) colder tropical months. 

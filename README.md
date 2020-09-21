The Perfect Weather For A Vacation

The Goal:
The goal for this project was to analze 500+ cities around the world and their relationship to the equator. The second part of the project was to find the perfect city for a vacation based on my ideal weather. 

In a world that is warming rapidly, I wanted to analyze the relationship between cities near the equator and their levels of humidity, cloudiness, maximum temperature, and wind speed. The main question I wanted to ask was if there was a relationship between humidity and the location to the equator. 

Once it was completed, I took that [cleaned CSV](https://github.com/EmmaLimoli/api-python-challenge/blob/master/weather_py/output_data/weatherPy_clean_data.csv) and created a live website with it. This can be found in [Web Design](https://github.com/EmmaLimoli/web-design-challenge). 

![north hemisphere of humitidy latitude and linear regression](https://github.com/EmmaLimoli/api-python-challenge/blob/master/weather_py/output_data/nhemHumLatReg.png)


How Was This Achieved Part One (WeatherPy):
To analyze the data, I created scatterplots with and without linear regression. I looked at the four areas as aforementioned and created scatterplots to analyze the relationship between the equator and the 500 cities. 

The first step was to add in the depenedencies such as Matplotlib, Pandas, Numpy, Requests, API keys, CitiPy, and SciPy. These would help to analyze the data efficiently and effectively. I set up my weather API key to pull the weather for the cities and then I created a loop to pull the data.

Once the random cities were pulled, I performed the API call and pulled the data that would help to determine the relationship between the equator and these cities. By creating a dictionary, I was able to clearly see the data for each of these cities and to export them into a CSV.

After, I used describe in Python to calculate the mean, STD, minimum and maximum etc. to clearly see the overall data for the four factors I was analyzing. It was important to take into account the cities with a humidity of 100% and analyze those since humidity was the main relationship I wanted to analyze. 

Once that was complete, I exported another CSV that was clean. Now is when I created 12 scatterplots. The first four were regular scatterplots analyzing the latitude vs. the factors such as max temperature, humidity, cloudiness, and wind speed. I also included little blurbs to analyze each factor. To keep the scatterplots apart, I used color coding so they didn't look exactly the same. I also saved these figures to use on the website.

The eight other scatterplots had linear regression. I divided up the north and south hemispheres, so each scatterplot analyzed one of the factors and the north or south hemisphere. This helped to show more clearly the relationship between cities north and south of the equator and how their weather was affected. All of the scatterplots were saved and I used color coding to keep them separate and easily viewed.

How Was This Achieved Part Two (VacationPy):
In the second part, I used the created clean data CSV to create heat maps to gain a better understanding of where these cities were located. This heat map, which was used with a configured map from Gmaps, showed the relationship between the lat/lng and the humidity. This helped to create a better visualize to analyze. 

I also created a dataframe to pull out the 'most desirable cities' based on max temps and humidity. For those who would like to stay in those places, I then used Google APIs, specifically place, to pull up the best hotels in the area to stay in. I used a for loop to pull all of those hotels, created an additional column, and then put them into a dataframe. Lastly, I created another map to point out where all of the hotels are and used marker layers to identify them easier.

Conclusion:
In conclusion, there were two things that were learned from this project. The best cities in the world to visit based on the weather and the random 500+ cities that were used. The second was that humidity and the location to the equator don't have a relationship.  

Observable Trends:

Observable Trend One: 
The first observable trend is that there seems to be a lot more cities in the northern part of the hemisphere. At least, a majority of the cities that are pulling are in the north. Each time I've run the numbers, I'll get many more cities in the northern hemisphere.

Observable Trend Two: 
The second observable trend is cloudiness. It seems to be something all cities get no matter where it's located in the world. The cloudiness scatter plot is very diverse. Many cities have very low clouds or a lot of clouds and then there are cities that fall in between. Cities that have the highest clouds aren't always the warmest, which makes sense since they block out the sun.

Observable Trend Three: 
Lastly, the most humid cities aren't always the closest to the equator as you would assume. Some of the cities that have 100 humidity are in the US or Canada. For example, on the latest run that I pulled five cities were in Canada and three in the US. Additionally, those cities had a max temps between 50-60. Based on the cloud ratio of about 90, I'd say a lot of that humidity was from moisture in the air.

Tools used: API calls, Pandas, JSON, Numpy, Matplotlib, gmaps, scipy.stats, citypy


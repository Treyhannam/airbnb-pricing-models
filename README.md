![Denver](https://github.com/Treyhannam/Capstone2/blob/main/andrew-coop-NflJmUuaYVI-unsplash.jpg?raw=True)
# airbnb Price Reccomendation in Denver Colorado
Denver Colorado is the capitol of Colorado. The city is well located for tourists to visit attractions such as Red Rocks Ampitheater, Rocky Mountain National Park, or a day within the city. In 2019, Denver saw over [17 million overnight visitors.](https://www.denver.org/tourism-pays/tourism-pays-for-denver/) For property owners in Denver there is oppertunity to make money for housing the tourists. A pricing model will be useful for airbnb hosts to evaluate what there property is worth given the prices of all listings within the area. So, hosts can make sure their listing is competitive with other listings on airbnb.

## Data Source
The data used is provided by a scraping website that contains all the airbnb listings within Denver. For this project data used was current as of 9-30-2021.

- [Inside Airbnb](http://insideairbnb.com/get-the-data.html)

## Preparing the Data
**Removing Listings With No Reviews**
![Price Distribution](https://github.com/Treyhannam/Springboard/blob/main/Capture.PNG?raw=True)
The decision to remove reviews was to avoide using listings that do not have a level of reputaion with consumers. This is similair logic to looking at reviews for a restuarant or on Amazon before spending money. 

**Removing Outlairs**
 Outlairs were removed because the price variable was skewed to variables that were not realistic. For example, one airbnb was listed for $4950.0 a night. Such a value is not typical of what a tourist would spend for the night even if it was a larger and wealthier group. Arguably keeping such outlairs will do more harm than good so they were removed in this case.

## Model
The model chosen for pricing was LGBMRegressor. This model had the lowest root mean squared. In other words, the lowest total error of predictions when predicted and evaluated on a test data set. To use the model an airbnb host will enter their listing id and this a price value will be output for the model.
![Prediction](https://github.com/Treyhannam/Springboard/blob/main/Capture2.PNG?raw=True)
## Future Improvements
There are many softwares to use for listing a housing property (VRBO, Evolve, etc). So, creating a model that is informative for features that are well known (locations, number of rooms) could be used to provide pricing information for what somebody could make if they want to use AirBnB to list their property. Ex. Somebody currently has their listing on VRBO and would like to know what price point they would be at if they used AirBnB. Or an investor could use the tool to get an idea of how much money a property could generate if they were to buy it.

Dedicating more time to feature engineering. Efforts would be worthwhile to build features from existing data and outside sources. Also, the focus should be on developing features that would be useful from a self service standpoint. For example, deriving features from the address of a listing. This could be variables such as, longitude, latitude, distance from DIA (major airport), etc. 

## Credits
Thank you to the team at Insideairbnb.com for developing, maintaining, and shareing the data they have collected. Also, thank you to Springboard mentor Lucas for advise on the project.

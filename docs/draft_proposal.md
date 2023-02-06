## This is a draft proposal for the capstone project

# **Price prediction of Airbnb housing**

### Abstract

- It is always difficult to chose an airbnb for stay during vacation from huge number of listings. Sometimes it feels that an Airbnb is overly priced and it is not worth the price and thus airbnb is rated low and negative reviews. This causes reduced number of bookings to that airbnb in near future. If an Airbnb is priced at very less price range then there is an risk that host of the airbnb may experience loss in business. So, a correct estimate of price for Airbnb will help both hosts and customers to keep up its standards while providing customer satisfaction and avoid loss in business.

### **How does this project help?**

- This project will help hosts in determining the price estimate of their airbnb considering the inputs of housing information like location of the house, number of bedrooms, number of bathrooms, number of beds etc. 
- This project will have web application where host can enter all of the housing information and they can obtain their suitable price to list on airbnb.

### **Advantages of prediction**

- This will help hosts in optimizing their revenue by setting with accurate prices for the houses. 
- Accurate price listing of airbnb houses will have advantage of remaining competition with other listings in that area.
- The end user / customers will also get benefited as they dont feel overpriced and give satisfactory ratings and good reviews which will help for future bookings.

### **Dataset used**

- The datset is not directly available form the airbnb website. There are many third party ebsites which scraped data from airbnb and they are providing datasets in csv format. Some of them are inside Airbnb (insideairbnb.com), AirDNA (airdna.co) and Smartbnb (smartbnb.io). 
- I chose to get data from inside airbnb as it has datasets seperately for each city. So I took three of the major cities in USA (New york, New Jersey and Washington D.C). All of these datasets are downloaded from inside airbnb website.
-  All the three datsets are having 18 columns with each state having different number of airbnb listings (many rows). All the three datsets are merged and hence it has 49010 airbnb listings and 19 features with one extra column of location ( New york, New Jersey and Washington DC) included manually.
-  As this dataset feom inside airbnb dataset is scraped on December 2022 and it is having the data from 12 months befor December 2022. So the data is from December 2021 to December 2022 

### Columns in dataset are
- 1)   id - int64  ( The id of the Airbnb of particular location)                         
- 2)   name - object  ( The name of Airbnb)                         
- 3)   host_id  - in64 ( Unique id of the host)
- 4)   host_name - object ( Name of the host)
- 5)   neighbourhood_group - object  ( the neighbourhood group that airbnb belongs to)
- 6)   neighbourhood - object ( neighbourhood that airbnb belongs to)
- 7.   latitude -  float64 ( latitude of airbnb)
- 8.   longitude - float64 (longitude of airbnb)
- 9.   room_type -  object (type of the room that airbnb has)
- 10.  price - int64  (price of airbnb)
- 11.  minimum_nights - int64  (minimum number of night stay for the listing (calendar rules may be different)
- 12.  number_of_reviews  - int64 ( no of reviews of airbnb)
- 13.  last_review  - object (he date of the last/newest review)
- 14.  reviews_per_month  -  float64 (no of reviews per month)
- 15.  calculated_host_listings_count -  int64  (The number of listings the host has in the current scrape, in the city/region geography.)
- 16.  availability_365 - int64  (avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host.)
- 17.  number_of_reviews_ltm  - int64  (The number of reviews the listing has (in the last 12 months)
- 18.  license  - object ( licence of airbnb)
- 19.  location -  object ( location of airbnb ( NY,NJ,DC)

### **Machine learning models**

- The initial dataset needs to be cleaned and drop unnecessary columns and impute any missing values with Mean/median/mode or interpolate with any statistical methods.
- The cleansed data is to be trained with machine learning algorithms to predict the price of the new house with the existing neighbourhood housing prices in airbnb.
- I wanted to train the data with linear regression if they have linear relationship between the features and predict the price and also use Random Forest and XGBoost, gradient boosting model for price prediction

### **Web deployment**

- After training the model with the machine learning algorithm, the web application is deployed in Streamlit and host can enter the details of their housing in the given inputs and obtain the predicted priice of his housing to list in airbnb.
- The webapp has series of inputs to be provided by the host and when the host enters all of the information, the ML model will run and gives desired price prediction suitable for the airbnb location to the host

### **Conclusion**

- Thus this project will helps hosts of airbnb to list their houses with accurate prices while staying in the competetion. Accurate price prediction of housing in airbnb will attract customers booking and have positive reviews.




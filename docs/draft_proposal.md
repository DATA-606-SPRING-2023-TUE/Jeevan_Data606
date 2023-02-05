# This is a draft proposal for the capstone project

## Price prediction of Airbnb housing

### Abstract

#### It is always difficult to chose an airbnb for stay during vacation from huge number of listings. Sometimes it feels that an Airbnb is overly priced and it is not worth the price and thus airbnb is rated low and negative reviews. This causes reduced number of bookings to that airbnb in near future. If an Airbnb is priced at very less price range then there is an risk that host of the airbnb may experience loss in business. So, a correct estimate of price for Airbnb will help both hosts and customers to keep up its standards while providing customer satisfaction and avoid loss in business.

### How does this project help?

#### This project will help hosts in determining the price estimate of their airbnb considering the inputs of housing information like location of the house, number of bedrooms, number of bathrooms, number of beds etc. This project will have we application where host can enter all of the housing information and they can obtain their suitable price to list on airbnb

### Advantages of prediction

#### This will help hosts in optimizing their revenue by setting with accurate prices for the houses. 
#### Accurate price listing of airbnb houses will have advantage of remaining competition with other listings in that area.
#### The end user / customers will also get benefited as they dont feel overpriced and give satisfactory ratings and good reviews which will help for future bookings.

### Dataset used

#### The datset is not directly available form the airbnb website. There are many third party ebsites which scraped data from airbnb and they are providing datasets in csv format. Some of them are inside Airbnb (insideairbnb.com), AirDNA (airdna.co) and Smartbnb (smartbnb.io). I chose to get data from inside airbnb as it has datasets seperately for each city. So I took three of the major cities in USA (New york, New Jersey and Washington D.C). All of these datasets are downloaded from inside airbnb.

### Machine learning models

#### The initial dataset needs to be cleaned and drop unnecessary columns and impute any missing values with Mean/median/mode or interpolate with any statistical methods. The cleansed data is to be trained with machine learning algorithms to predict the price of the new house with the existing neighbourhood housing prices in airbnb.


### Web deployment

#### After training the model with the machine learning algorithm, the web application is deployed in Streamlit and host can enter the details of their housing in the given inputs and obtain the predicted priice of his housing to list in airbnb.

### Conclusion

#### Thus this project will helps hosts of airbnb to list their houses with accurate prices while staying in the competetion. Accurate price prediction of housing in airbnb will attract customers booking and have positive reviews




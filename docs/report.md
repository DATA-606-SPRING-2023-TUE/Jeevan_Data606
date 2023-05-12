# Final Report of Capstone Project on Price prediction of Airbnb Housing

Presentation slides link: https://github.com/DATA-606-SPRING-2023-TUE/Jeevan_Data606/blob/main/docs/capstone.pptx

Presentation video link: 

## Introduction

Airbnb Hosts and Guests always find difficult to agree on price because hosts want to make money in their business and guests want to save money by not overpaying. A web application which can predict the prices of airbnb with the help of machine learning model will be helpful to both hosts and guests in deciding on the price. This project has several stages starting from data collection to data cleaning, exploratory data analysis, visulaization, feature engineering, machine learning model training and web deployment of model through streamlit.

The final goal of this project is that user should be able to visit the web application and fill the Airbnb details like Location, Room type, neighborhood area, neighbourhood group, latitude and longitude values and other features of airbnb and they can able to see the predicted price from the features.

https://user-images.githubusercontent.com/123945822/218366802-eaac65f5-45ab-4c19-a473-83f9df1993f1.mp4

## Data Collection

- The datset is not directly available form the airbnb website. There are many third party websites which scraped data from airbnb and they are providing datasets in csv format. Some of them are inside Airbnb (insideairbnb.com), AirDNA (airdna.co) and Smartbnb (smartbnb.io). 
- Data is downloaded from insideairbnb.com for three locations- New york, New Jersey and Washington D.C as of 16 December 2022 ( 3 datasets for 3 locations)
- As this dataset from inside airbnb dataset is scraped on December 2022 and it is having the data from 12 months before December 2022. So the data is from December 2021 to December 2022 
- All the three datsets are having 18 columns with each state having different number of airbnb listings (many rows). All the three datsets are merged and hence it has 49010 airbnb listings and 19 features with one extra column of location ( New york, New Jersey and Washington DC) included manually.


## **Data cleaning and Exploratory Data Analysis**

- There are few missing details like name of airbnb and host_name which will not affect our analysis. Licence column, Id, Host_ID are dropped as they are not useful for analysis
- Neighbourhood group has 5 groups in New york but there are no neighbourhood groups in New Jersey and Washington DC
- Price column has abnormal values while anlaysis and observed that there are many houses whose price is above $5000 due to luxury houses but there are 7 houses whose price is above $10000 with highest being $98159.
- There are also listings with zero price and they are hotel room types. Dropping those rows too as they are not useful for analysis
- Price distribution is skewed and hence logarithmic conversion is applied to price column and now the distribution looks normal.
- Null values are filled with appropriate values and some rows are dropped which have no information

## **Data Insights and Visualization**

-  Several plots and graphs are derived from data using data visualization tool Tableau.
-  Bar graphs like Count of Airbnb by room type, count of airbnb by location and neighborhood group. Average price of airbnb by location and room type and filters are applied on Tableau to select the location and neighbourhood.
-  Geospatial analysis with respect to different locations are plotted using latitude and longitude on the basis of neighborhood group and room type
-  Dashboard is built with all these plots and filters are applied so user can select the location, neighborhood and room types to view their desired plots and graphs.

### **Feature Engineering**

-  There are total 18 features and target variable ‘price’ in the dataset
-  There are few features like Id, Host Id and license which does not affect the target variable price. 
-  Correlation matrix is used and selected features which are strongly correlated. Selected features are derived from the correlation matrix plot
-  Selected features are free from nulls and they are strongly related with target variable price

### **ML model training**

-  Trained the model with different Machine learning algorithms like Linear Regression, Lasso and Ridge Regression, XGBoost Regression and Random forest regression
-  Data is initially trained with Linear Regression model and it gave R2 score of 0.12 which means it has more variance in prediction
-  Regularization techniques like Lasso and Ridge regression are used with linear regression but they gave a maximum R2 score of 0.49
-  Tried various machine learning algorithms like Huber regression, catboost regression, XG boost regression but still the R2 score is 0.72 and still there is variance in the prediction
-  Finally tried to train with Random Forest Regression model and got 0.62 R2 score. Hyperparameter tuning is used to improve the R2 score. Best parameters are selected after trying with different hyperparameters
-  Random forest with nest parameters gave 0.82 R2 score and it is the best model to predict the price among the others.
-  This application can also be utilized by Airbnb to provide suggestions to hosts regarding adjusting prices in response to market competition.



### **Web deployment of Model**

- After training the model with the machine learning algorithm, the web application is deployed in Streamlit and host can enter the details of their housing in the given inputs and obtain the predicted priice of his housing to list in airbnb.
- The model trained is converted into pickle file and this pickle file is fed into streamlit. Streamlit is a web based library in python and it takes the inputof features from user and used to output the predicted price
- The Streamlit has series of inputs to be provided by the host and when the host enters all of the information, the ML model will run and gives desired price prediction suitable for the airbnb location to the host
- The web application allows users to input various features such as location, neighbourhood, and neighbourhood group. Additionally, users can select their exact location on the map and obtain the corresponding latitude and longitude values


### **Advantages of Project**

- This will help hosts in optimizing their revenue by setting with accurate prices for the houses. This will help in increasing their bookings
- This will also help in analysing the market around it and determining price based on the market.
- Accurate price listing of airbnb houses will have advantage of remaining competition with other listings in that area.
- The web application is easy to use and both hosts and guests can fill out the information and predict the price
- Real estate investors can also make use of this application and predict the price of a house and they can decide to invest in housings that makes profit.
- This application can also be utilized by Airbnb to provide suggestions to hosts regarding adjusting prices in response to market competition.
- The end user / customers will also get benefited as they dont feel overpriced and give satisfactory ratings and good reviews which will help for future bookings.

### **Conclusion**

- Thus this project will helps hosts of airbnb to list their houses with accurate prices while staying in the competetion. Accurate price prediction of housing in airbnb will attract customers booking and have positive reviews.
- This project aimed to develop a machine learning model that could accurately predict the prices of Airbnb listings in three locations: NYC, NJ, and DC, using various features available in the dataset.
- The web application assists hosts and guests in assessing their housing and Airbnb bookings.
- There is potential for improving the model's accuracy by incorporating additional features, expanding to more locations, and gathering more data, among other possibilities.
- Leveraging Natural Language processing on the Airbnb name and reviews will help in bringing more features and helps in model training and accuracy









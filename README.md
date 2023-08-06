# ML-for-Predicting-Restaurant-Inspection-Grade-with-Urban-Features

## Abstract:
Food safety and sanitation are closely related to residents’ health. To improve the dinning sanitation and guarantee the safety, the New York City Department of Health and Mental Hygiene (DOHMH) conducts unannounced inspections towards restaurants and gives a grade letter to each restaurant based on their hygiene, pest control, food handling, and other sanitary factors.

The project is aimed to delve into the impact factors of restaurant inspection grades in New York City. The project takes some demographic and urban social factors into consideration, including, waste management resources, income, education attainment, population composition, and so on, and applies machine learning models on predicting restaurant inspections grade, and shed light on the contribution of urban features to the restaurant's sanitation condition.

## Data Source:
- Inspection Data:
The main dataset that is used for this project is restaurant inspection results open data provided by DOHMH. The project only focuses on the inspection results in 2023 and results with meaningful results A or B or C. After we cleaned the features data, we merged features data with restaurant inspections data by zip code. The final dataset contains 9259 data records, with 7229 records in grade A, 1300 records in grade B, and 730 records in grade C.

- DSNY Data:
The project uses the dataset about food scrap dropoff locations provided by DSNY. The data is aggregated into zip code level and converted to the number of food scrap dropoff locations in each zip code. Although the food scrap dropoff location is for residential waste management, we would like to use this factor to reflect the waste management resources distribution among New York City.

- Census Data:
The demographic factors we use are median income, education attainment, population density, race distribution in each zip code in 2021. The datasets are from the US Census Bureau. The census data has missing values in some zip codes. To handle the missing values, we use the average data level in each borough to replace the missing value. In this way, we could keep more valid data records and also guarantee the demographic data differences among the city.

- Crime Data:
The data is from the NYPD. We aggregated the data by zip code and calculated the number of crimes happening in 2021 in each zip code.

- Cuisine Type:
The project also dive into the relation between cuisine and inspection results. To simplify the cuisine category and reduce the feature dimension, we group some categories as a new cuisine category. Eventually, we have 58 types of cuisine.

## Methods:
The project contains data preprocessing, Exploratory Data Analysis for spatial distribution, and Anomaly Detection to detect zips that have anomalous grades proportion. 
### Models: Decision Trees, Random Forest, Gaussian Mixture

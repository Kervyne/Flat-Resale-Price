# **Data Analysis and Prediction of Resale Flat Prices with Regression**
<br>
<br>
This is a self-continuation of data analysis project as part of my assignment. Data used is "RESALE.xlsx" while the codes for data cleaning, analysis, visualisation, regression modelling and result analysis is contained within the file "Regression and Data Analysis of Flat Resale Price.ipynb".
<br>
<br>

## **Preface**
<br>
 

As reported in [CNA](https://www.channelnewsasia.com/singapore/hdb-resale-flat-prices-2023-increase-bto-supply-4020341), the prices for resale flat rose by 4.8% in 2023 but it still was less than in 2022 where the increased was 10.4%, according to Housing Development Board (HDB). In the fourth quarter of 2023, the resale volume is also the lowest compared to the last three years. One of the contributing reason could be the relatively more options in the Build-To-Order (BTO) market. Nonetheless, the experts stated that the reduction in resale prices is not likely in the near future. Regardless, the market for resale flat is always open.

<br>

## **Context**
<br>
A property agent who specializes in the sale of resale flats wants to determine the significant factors contributing to the price of the resale flats. Assuming all other external factors such as macro-economic factors are constant across the years, the property agent would like to identify factors that will affect how resale prices could change based on the information within the dataset provided.
<br>

## **Project Objectives**
<br>
The high level overview is to find out the distribution of the different flat types in the different towns and how different factors correlates with the resale price. Ultimately, this project aims to build a regression model and to evaluate the features that are important in predicting the resale flat prices.
<br>

## **Data** 
<br>
The data size is 183905 rows by 18 columns prior to data cleaning
<br> <br>


| Column Name            | Measurement Level | Description |
|------------------------|-------------------|-------------|
| Full Address           | Nominal           | Full address of resale flat sold |
| Storey Range           | Nominal           | Resale flat’s floor range |
| Flat Model             | Nominal           | Resale flat model |
| Flat Type              | Nominal           | Resale flat type |
| Town                   | Nominal           | Town |
| Town (group)           | Nominal           | Estate Type |
| Floor Area Sqm         | Numeric           | Floor Area Sqm |
| Latitude               | Numeric           | Latitude |
| Longitude              | Numeric           | Longitude |
| Lease Commence Date    | Numeric           | Lease Commence Date |
| Year-Month Sold        | Numeric           | Year-Month Sold |
| Nearest Hawker         | Nominal           | Nearest Hawker |
| Nearest MRT            | Nominal           | Nearest MRT |
| Nearest Primary School | Nominal           | Nearest Primary School |
| Hawker Dist            | Numeric           | Distance between flat and nearest hawker |
| Mrt Dist               | Numeric           | Distance between flat and nearest MRT    |
| School Dist            | Numeric           | Distance between flat and nearest school |
| Resale Price           | Numeric           | Resale Price (Target) |
<br>



## Insights

### Correlation Matrix
<br>
<img width="657" alt="Screenshot 2024-02-18 at 2 16 37 AM" src="https://github.com/Kervyne/Flat-Resale-Price/assets/133936905/a130e1a4-8d48-4784-901d-b3269a1460d4">
<br>

### Correlation in descending order of different factors with resale prices
<br>
<img width="294" alt="Screenshot 2024-02-18 at 2 16 52 AM" src="https://github.com/Kervyne/Flat-Resale-Price/assets/133936905/e01138d6-a38d-4d39-8d57-9badc7d9fb1f">
<br>
Expectedly, the floor area and the level of the flat is positively correlated with the resale flats while the rest of the factors including years since leased, distance to school, mrt and hawker centres are negatively correlated to the resale prices.
<br>
Specifically, the property agent would also like to find out how the prices of 5 room flats in different town compare, in general
<br>


![Median Price Plot](https://github.com/Kervyne/Flat-Resale-Price/assets/133936905/f68a1e45-fb84-488d-9907-54d5fa2b1536)
<br>
The resale flat prices in central area are significantly higher than the rest of the heartland towns
<br>
## Results and Conclusion
<br>
The resultant Mean Absolute Error on test data is 51394.31689392543
<br>
The resultant R2 value on test data = 0.7813148037818582
<br>

### Feature Importance
<br>

![Feature Importance](https://github.com/Kervyne/Flat-Resale-Price/assets/133936905/2058cfa8-57d3-41b9-98f7-71c871645e09)
<br>
<br>
Overall, this is a simple multiple linear regression analysis to analyze the resale flat prices with the different factors. It was also showed that the flat type was the most important in building the predictive power for the resale flat prices. On the other hand, the estate type is the least important in predicting the resale flat price. This could, however, be due to the lack of variance in their data type with only mature and non-mature. It is also important to note that the resale flat prices is also affected by many other factors such as, but not limited to, government policy, inflation rate, supply and demand factors. Furthermore, more sophisticated models can also be explored to improve the results and accuracy of predicting the resale flat prices, which can eventually help in reducing the challenges in predicting resale flat prices that can then help to provide more insights for the housing markets.


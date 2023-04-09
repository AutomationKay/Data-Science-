# NBA MVP Prediction Project 
 ![image](https://user-images.githubusercontent.com/112325655/230544171-98b86307-474c-4ab5-b1a7-7e53088a464f.png)

The National Basketball Association (NBA) Most Valuable Player (MVP) award is the most prestigious individual award in the National Basketball Association. This award is given to the player that makes the greatest individual contributions to their respective team. There are various statistical categories that are leveraged when selecting the winner of this award, points per game (ppg), value over replacement player (VORP), and win share are a few categories for example. Based on a player’s performance in each category, officials from around the league award a player first, second or third-place votes. At the end of the regular season, votes are tallied up and the player with the most first-place votes takes home the award. 

## **1.	Data**

_[Kaggle](https://www.kaggle.com/datasets/robertsunderhaft/nba-player-season-statistics-with-mvp-win-share)_
 
This data set contains the Assists Per game, Minutes Per game, Points per game, and other key stats used in tracking NBA players’ individual impact on the team. The data included in the model can be used to predict the next NBA MVP or to predict who will lead the league in a certain statistic. In recent years the NBA has started to rely heavily on data analytics, using historical data to create new offensive and defensive strategies. One of the most notable analytic shifts in the NBA was seen with the Houston Rockets in the last 6 years. The team found that based on historical data, the mid-range shot was the least efficient shot in basketball and started to discourage their players from taking that shot. The team eventually built its entire offense based on that methodology, recruiting players and coaching staff that fit the metric. The data can also be used to analyze the types of shots favored over the years etc. 

## **2.	Method**

The dataset contains data on every NBA season from 1982 – 2022, over the years the NBA has added new statistical categories and some fundamental changes to the game. The addition of the three-point line is one of the biggest changes in the history of the league. Due to this major change, earlier seasons in this dataset do not have values in this category, which may affect the models’ ability to accurately predict the MVP of each season. There are a few advanced metrics that utilize the three-pointer in their measurements, making this statistic an important factor. However, due to the nature of the NBA voting process and its heavy dependence upon those advanced statistics, filling in missing values with the standard deviation or mean method would skew the data and cause the model to return even more inaccurate results. Therefore, for this project, the approach taken was to simply fill in all missing values with 0s and remove data only when necessary. 

## **3.	Data Wrangling**

_[Data Wrangling Notebook](https://github.com/AutomationKay/Data-Science-/blob/main/Capstone%202/notebooks/Capstone_2_DW.ipynb)_

The dataset pulled in from Kaggle needed a few changes made to it. First, the column names were updated to be more readable and also more consistent, then all NaN values were filled with 0s, as mentioned under (2) Method this choice was to preserve the integrity of the data in making predictions. Next, the data was used to find the actual MVP winners for each season and create a new dataset that would be used to contain the MVP statistics for later reference. The intention of doing this would be to create a benchmark, as changes were made to the broad dataset, those changes could be compared to or applied to the data frame containing the MVP data. Finally, a heatmap was created to look at the correlation between the key metric “award_share” and all the other statistical categories. 
![image](https://user-images.githubusercontent.com/112325655/230544201-c0780567-30ed-45ed-9d04-767db88f4371.png)


 
## **4.	EDA**

_[Exploratory Data Analysis Notebook](https://github.com/AutomationKay/Data-Science-/blob/main/Capstone%202/notebooks/Capstone_2_EDA.ipynb)_

This phase of the project examined the relationships between award_share and other statistical categories. In this phase, the data was also adjusted to a 35-minute-per-game basis. This allowed the comparison of stats for players that have played different minutes to be compared on a per-minute basis. This adjustment was applied to the general dataset and also the MVP data frame, scaling both datasets to a 35-minute-per-game basis. Next, the data in the general dataset was normalized, and the columns containing the stat categories most correlated to the award_share metric were split off from the data. This was done to perform a mutual information score test between the categorical values and the target variable. In doing this, a few stats that were somewhat correlated to the key metric were dropped. 

 ![image](https://user-images.githubusercontent.com/112325655/230544228-c76d5e61-5da9-48da-9949-bcc96d8174a8.png)
![image](https://user-images.githubusercontent.com/112325655/230544238-5a79c8a6-7d92-47e2-9838-7f5661888902.png)

 
## **5.	Preprocessing**

_[Preprocessing Notebook](https://github.com/AutomationKay/Data-Science-/blob/main/Capstone%202/notebooks/Capstone_2_PreP.ipynb)_

This phase of the project was all about preparing the data for modeling. Here the data was reviewed and all changes made so far were double-checked to make sure there wasn’t any noise that could interfere with the results. Finally, the results obtained from the mutual information score test were used along with the master data frame to create a new data frame that would be ready for testing.

## **6.	Modeling**

_[Modeling Notebook](https://github.com/AutomationKay/Data-Science-/blob/main/Capstone%202/notebooks/Capstone_2_Model.ipynb)_

The final phase of the project, with the data already preprocessed and ready for testing, 4 different methods were tested. Linear Regression, Random Forest Regression, XGB Regressor, LGBM Regressor. Each model was tested on every season from 1982 – 2022 using the stats deemed most appropriate through the heatmap from the data wrangling phase and mutual information scores from the EDA phase.
 ![image](https://user-images.githubusercontent.com/112325655/230544263-c1d1de55-9467-4bca-a0f2-f22bfa3e0bda.png)



## **7.	Future Improvements**

In the future, I plan to use hyperparameter tuning to quickly find the best parameters for each model in order to obtain higher accuracy scores for each model. The goal of this project is to get as close to 100% as possible, that is predicting the MVP each season for as many seasons as possible. I would also like to fine-tune the models so new data can be imported after every season and the MVP for the upcoming season can be predicted based on the latest data. 



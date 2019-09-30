# Pro-Kabaddi-League
Pro Kabaddi League Hackathon by upGrad

## TASK 2 Point table Top Team Prediction
***************************************
1. We have collected the data for all seasons point table data.
2. We have removed all the columns which had all values NULL.
3. There are columns which had ONLY one value so we decided to remove those columns also as they are not going to add any value to our problem statement.
4. We have see cateorical plots for the LOST, WINS and NORESULT to see the pattern.
5. We have started with LineaRegression and the followed by Ridge Regression and XGBRegressor.

*************************************************************************************
### Predict the the top team in the points table after the completion of league matches
*************************************************************************************
a. LineaRegression - with MEAN RMSE - 0.6811 - Top Team: Dabang Delhi K.C
b. Ridge Regression with alpha value as =0.020 - with MEAN RMSE -  0.6748 Top Team: Dabang Delhi K.C
c. XGBRegressor with n_estimators=1500, learning_rate=0.20 - with RMSE - Mean - 0.6329 Top Team: Bengal Warriors

*****************
### Final Prediction:
*****************
Dabang Delhi K.C

Out 2 out of 3 models predictig the Dabang Delhi K.C as Top in point table.


## TASK 6 & TASK 7 Player Level Prediction tasks:
***********************************************
Steps:
1. From https://www.prokabaddi.com we have extracted the JSON URLs and extracted the player_id. Using the player_id exteacted the details of the each who have participated in earlier seasons and participating in the current season. 
2. We have checked the data for NULL values and removed the all the columns which had 95% values as NULL.
3. There are some columns like super_10s and high_5s which had around 14% values as NULL so we have replaced those values with zero assuming that player had not scored either super_10s or high_5s in that season.
4. We have taken starategy that for training purpose we will keep the data from season 1 to season 6 & season 7 data we will keep for for the testing and prediction purpose.
5. During data analysis we have found that there are some players who have not played much matches and their sucess rate for raid and tackle is 100%. E.g. One player has played only 1 match and done one raid which is sucessfull. So we decided to keep only those players who have played at least 15 matches across all the seasons for training purpose.
6. We have seen pair plot to see the relationship of our independent variables and dependent variables. But we have found any strong predictor of our dependent variables
7. We have also drawn the heatmap to visualize relationship among different variables. Not found any strong predictor.
8. We have started with LineaRegression and the followed by Ridge Regression and XGBRegressor.

*************************************
### sucessfull raid percentage-prediction
**************************************
a. LineaRegression - with RMSE - Mean - 10.51 : Top player: Victor Onyango Obiero
b. Ridge Regression with alpha value as 0.05 - with RMSE - Mean - 9.731 : Top Player: Pawan Kumar Sehrawat
c. XGBRegressor with n_estimators=1000, learning_rate=0.10 - with RMSE mean - Mean - 4.807 : Top Player: Pawan Kumar Sehrawat


#### Final Prediction:
*****************
Top : Pawan Kumar Sehrawat as XGB model mean RMSE is quite low and for CV RMSE mean is also low and this model predicted this name as top scorer in this category.


*************************************
### sucessfull tackle percentage-prediction
**************************************
a. LineaRegression - with mean RMSE - 8.979: Top Player: Vishal
b. Ridge Regression with alpha value as 0.15 - with mean RMSE - 7.741 : Top Player: Vishal Bhardwaj
c. XGBRegressor with n_estimators=1000, learning_rate=0.15 - RMSE - 3.611 : Top Player: Baldev Singh

*****************
#### Final Prediction:

First : Baldev Singh as XGB model mean RMSE is quite low and for CV RMSE mean is also low and this model predicted this name as top scorer in this category.

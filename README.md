# Appliance-Energy-Prediction
The house temperature and humidity conditions were monitored with a ZigBee wireless sensor network. Each Wireless node transmitted the temperature and humidity conditions around 3.3 min. Then, the wireless data was averged for 10 minutes. Weather from nearest airport station was also merged together with the experimental data sets using the date and time column. We need to predict the enrgy use of appliances. T1,T2,T3,T4,T5,T6,T7,T8 and T9 are the diffrent temperatures of diffrent rooms which are the columns of our dataset, In the same relative humidities for all nine rooms are given in the dataset. Some additional information is also provided in the dataset like outside building temperature and humidity. for refernce we are also provided the temperature and humidity of outside of the airport station. Some other conditions are also mentioned in the dataset like Pressure,Windspeed,Visibility,Tdewpoint.And the energy of appliances is also provided that we have to predict for an unseen data.

Firstly we tried to understand our dataset and variables and checked the null values and duplicate values.Then we saw the skewness of our variable and transform them accordingly for predicting the best results. We have also tried to remove Outliers from the variables.After doing EDA we concluded that our data is non linear in nature.We also discovered that our dataset has multicollinearity which can impact our results badly.We have try to remove those multicollinarity using feature engineering. To remove multicollinearity i have also tried the technique called VIF, but after adjusting the vif of all features my dataset become too simple. I have also tried Principle component analysis(PCA) to reduce the dimmension but the results were not satisfactory.By doing some basic feature engineering we have reduced the multicollinearity to some extend.

After cleaning and doing some pre processing of our data we have divided our data into two subset one is trainig datset and one is testing dataset using train_test_split function into 80-20% ratio respectively. Then we have used some ML algorithms to predict our energy variable.ML algorithms that are used are

Linear Regression

Polynomial Regression

Lasso

Ridge

Decision Tree Regressor

K Nearest Neighbour

Support Vector Machine

Bagging Regressor

Gradient Boosting

Xtreeme gradient boosting

Random Forest

Xtra Tree Regressor

Tree based models are by far the best model while dealing with data set that has most of its features having no linear correlation with target variable. For similar reasons, linear models such as linear regression, Ridge and Lasso perform the worst.

The best Algorithm to use for this dataset is Extra Trees Regressor.

The untuned model was able to explain 74.7% of variance(R2_test_score=0.747),while the tuned model was able to explain 74.9% of variance which is a tiny improvement of 2.68%.

Our best model is a black box model so for model explainability we have use LIME algorithm.

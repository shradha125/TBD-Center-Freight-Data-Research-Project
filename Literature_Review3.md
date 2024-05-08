**1. Freight Vehicle Travel Time Prediction Using Gradient Boosting Regression Tree**

***Citation:*** X. Li and R. Bai, "Freight Vehicle Travel Time Prediction Using Gradient Boosting Regression Tree," 2016 15th IEEE International Conference on Machine Learning and Applications (ICMLA), Anaheim, CA, USA, 2016, pp. 1010-1015, doi: 10.1109/ICMLA.2016.0182. keywords: {Trajectory;Regression tree analysis;Boosting;Predictive models;Companies;Data models;Transportation;gradient boosting regression tree;GBRT;decision tree;machine learning;data mining;travel time prediction;freight vehicle;trajectory},

***Link:*** https://ieeexplore-ieee-org.ccny-proxy1.libr.ccny.cuny.edu/document/7838286 

***Summary:***

Accurate travel time prediction can help the transportation companies make better planning and task scheduling. Aim is to perform travel time predictions for freight vehicles at individual level using Gradient Boosting Regression Tree (GBRT) models. 

***Data:***
All the features were extracted or composed from vehicles’ temporally sparse trajectory data. Three routes from China were selected for the prediction experiments. 3 different datasets for each route. 
In the three datasets, each for different route, where each row contains an interval and its corresponding mean travel time calculated using training set only. 
Each trip is a trip tuple that contains types of features: 
1.	Basic - The basic features are mainly date-time relevant features.
2.	historical travel time - historical interval mean travel time. 

***Methodology:***
Used a 15-minute trip interval to collect the corresponding trips for the calculation of mean travel time. 

With the basic and historical travel time features, pre-start (before a trip starts) prediction for all the vehicles is performed. Furthermore, used trajectory data as the real-time information to perform post-start (after a trip starts but before it ends) prediction.
The post-start prediction is useful especially for freight companies who want to make realtime adjustment of their plans and schedules. 
To perform post start prediction, mean speed sequence feature is introduced. Mean speed sequence is a sequence of mean speed values of travelled distances estimated using trajectory data. Trajectory report is received every 30 second, this allows to estimate a new mean speed value every 30 seconds.

Bayesian optimisation was adopted for model fitting while the results show that both pre-start (before trip starts) and post-start (after trip starts) predictions accuracies reach above 80%. With Bayesian optimisation the time of model fitting process was reduced to less than an hour while this process can last long with traditional grid search approach.

Experiments were first performed for pre-start predictions using only basic and historical travel time features. Experiments were then performed for post-start predictions by adding the mean speed sequence from the 15 minutes for example and the historical mean speed sequence from the last 15 minutes. The historical mean speed feature can be considered as the compensation of the incomplete real-time information in order to gain more confidence about what might be happening during the rest of the trips.

***Evaluation:*** Root mean squared error (RMSE) and mean absolute percentage error (MAPE) are selected as the metrics of prediction performance evaluation for this study. 
For example, the prediction performances are gradually improved by adding more real time mean speed estimates. 
The error is reduced to about 11% when the mean speed sequences of first 5 minutes are used.
 The error is reduced by about 5% when it is compared to pre-start predictions without using any amount of real-time information.






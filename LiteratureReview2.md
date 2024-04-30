**A Machine-Learning Based Approach for Zoning Urban Area in Consolidation Schemes Context**

***Citation:*** J. E. Ouadi, H. Errousso, S. Benhadou, H. Medromi and N. Malhene, "A Machine-Learning Based Approach for Zoning Urban Area in Consolidation Schemes Context," 2020 IEEE 13th International Colloquium of Logistics and Supply Chain Management (LOGISTIQUA), Fez, Morocco, 2020, pp. 1-7, doi: 10.1109/LOGISTIQUA49782.2020.9353901. keywords: {Uncertainty;Urban areas;Transportation;Machine learning;Benchmark testing;Data models;Logistics;urban logistics;freight consolidation;logistics demand;zoning;machine-learning},

***Link:*** https://ieeexplore-ieee-org.ccny-proxy1.libr.ccny.cuny.edu/document/9353901 

***Summary:***
This research propose a hybrid machine-learning framework combining several algorithms and the achieved accuracy benchmarks.
In this paper, the focus is on assessing demand in order to involve consolidation.
    i.e. switching hubs. Aim of this paper proposed a machine-learning framework for creating zones within a city.

They are actually consolidating 2 hubs.   

1 - the suppliers send the shipments to this hub. They receive the flows that have to reach the city and to organize their shipments. 
2 - urban hubs that are located along with the mass transport network. They are responsible for collecting supplies and organizing trips to final destinations. 

The proposed approach involves three main steps: 

***Data*** - Location data and demand data. 

***Demand Segmentation*** - Clustering k-means. k-medoids (widely thought to be practical and efficient for geocoded data), clara. CLARA repeats the sampling and clustering processes a pre-specified number of times in order to minimize the sampling bias
a clustering algorithm includes a similarity feature that seeks to establish k -clusters from geographical data with the intent of minimizing between item dissimilarity within the same cluster and maximizing the inter-clusters dissimilarity. 

***Logistic Demand Prediction*** - What behavior do demand involve in while in a zone?
Answering this question will uncover whether the transportation demand in this zone is certain or not over the long term. Taking into account demand dynamics, zones could react according to different levels: zone boundaries and zone capacity growth.

While machine learning methods, like Artificial Neural Networks (ANN), K-Nearest Neighbour (k-NN) are used for classification and regression, Support Vector Machine (SVM), decision trees and Adaboost classifiers improve the predictive ability with data samples.

To evaluate the forecasting accuracy and compare the selected models, they chose the normalized forecasting performance metrics namely, MSE (Mean squared error), RMSE (Root mean square error), MAPE (Mean absolute percentage error) and R-Squared (R ). 

***Logistics demand prediction:*** SVM model achieved the better performance. 

The basic idea was to use commodity flows and their geographical distribution as a starting point for locating hubs in a p-hub median problem. Research that is cited here handled a geocoded addresses data and through quantifying the median distance using bivariate statistics, they examined the clustering of locations of the fast-food restaurants.
 As a result, accuracy of machine-learning algorithms is used for an efficient demand investigation that helps when implementing, over the long-term, mobility systems and networks. 

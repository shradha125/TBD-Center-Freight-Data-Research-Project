**1. A Machine-Learning Based Approach for Zoning Urban Area in Consolidation Schemes Context**

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

The basic idea was to use commodity flows and their geographical distribution as a starting point for locating hubs in a p-hub median problem. Research that is cited here handled a geocoded addresses data and through quantifying the median distance using bivariate statistics, they examined the clustering of locations of the fast-food restaurants. Accuracy of machine-learning algorithms is used for an efficient demand investigation that helps when implementing, over the long-term, mobility systems and networks.  


**2. Evaluation of machine learning methodologies to predict stop delivery times from GPS data**

***Citation:*** Sebastián Hughes, Sebastián Moreno, Wilfredo F. Yushimito, Gonzalo Huerta-Cánepa, Evaluation of machine learning methodologies to predict stop delivery times from GPS data,
Transportation Research Part C: Emerging Technologies, Volume 109, 2019, Pages 289-304, ISSN 0968-090X, https://doi.org/10.1016/j.trc.2019.10.018. (https://www.sciencedirect.com/science/article/pii/S0968090X18314645)

***Link:*** https://www.sciencedirect.com/science/article/pii/S0968090X18314645?casa_token=5Gy06HhmjC4AAAAA:A-wJRrlwFvw3baGPsrbsEJFbpUECONalR3zyQXyPZQsyH5s3FkmRuRNz33ArJ_Rt2gyNqcIzXWg  

***Summary:***
The research aims to predict the stop delivery times (i.e., the time spent at each stop to deliver goods to final receivers). This is done by testing a wide range of machine learning techniques (including different types of ensembles).  
(1) predict the stop delivery time. - (lasso regression, ridge regression, and elastic net)
(2) to determine whether the total stop delivery time will exceed a predefined time threshold (classification approach). - naive Bayes, logistic regression, K-nearest neighbors, support vector machines, classification trees, and neural networks.

The resulting contributions are twofold. First, we leverage operational data collected directly from GPS traces provided by a company that provides routing solutions in Latin America to evaluate the machine learning models. This approach also allows us to include operations-related data in the prediction (i.e., demand, number of clients visited in a stop).

Evaluated based on  accuracy and F1 score (harmonic mean between precision and recall).


**3. Diffusion Models: A Comprehensive Survey of Methods and Applications**

***Citation:*** Ling Yang, Zhilong Zhang, Yang Song, Shenda Hong, Runsheng Xu, Yue Zhao, Wentao Zhang, Bin Cui, and Ming-Hsuan Yang. 2023. Diffusion Models: A Comprehensive Survey of Methods and Applications. ACM Comput. Surv. 56, 4, Article 105 (April 2024), 39 pages. https://doi.org/10.1145/3626235

***Link:***
https://dl.acm.org/doi/full/10.1145/3626235?casa_token=dzWXYo2eR1oAAAAA%3AB330awEm-SOLEJcFrvvVXAcwAPY3zh4IpAdjVrHzniuNnf3NdHVMV6bRo7oNC8NC7OMgmBw2yn7Ojw 

***Summary:***
Diffusion models have emerged as a powerful new family of deep generative models with record-breaking performance in many applications, including image synthesis, video generation, and molecule design. Diffusion models are a family of probabilistic generative models that progressively destruct data by injecting noise, then learn to reverse this process for sample generation.
***Github: https://github.com/YangLing0818/Diffusion-Models-Papers-Survey-Taxonomy***
In this paper, the foundations of diffusion models, providing a brief but self-contained introduction to three predominant formulations: denoising diffusion probabilistic models (DDPMs), score-based generative models (SGMs), and stochastic differential equations (Score SDEs) are explained. 

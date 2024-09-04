## End-to-End Prediction of Parcel Delivery Time With Deep Learning for Smart-City Applications

***Citation:*** 
A. C. de Araujo and A. Etemad, "End-to-End Prediction of Parcel Delivery Time With Deep Learning for Smart-City Applications," in IEEE Internet of Things Journal, vol. 8, no. 23, pp. 17043-17056, 1 Dec.1, 2021, doi: 10.1109/JIOT.2021.3077007.
keywords: {Estimation;Logistics;Internet of Things;Deep learning;Global Positioning System;Data models;Smart transportation;Deep learning;last mile;origin–destination (OD);parcel delivery;predictive modeling},

***Summary:*** 

**Data Source:** 
- Canada Post Dataset: The dataset comprises last-mile delivery records in the Greater Toronto Area (GTA) from January 2017 to June 2017.
- Weather Data: Daily weather information, including temperature, rain, and snow precipitation.

**Data Features:** 
- Origin and Destination Coordinates: Longitude and latitude for the depot and delivery location.
- Timestamps: Out-for-delivery scan time and delivery completion time.
- Weather Conditions: Daily temperature, precipitation levels (rain and snow), and snow on the ground.

**Data Preprocessing:**
- Coordinate Normalization: Normalize geographical coordinates.
- Time Feature Extraction: Extract features such as hour of day, day of week, and week number from the timestamps.
- Weather Encoding: Normalize weather data to a scale of 0-1.

**Feature Extraction:**
- Haversine Distance: Compute the Haversine distance between origin and destination coordinates.
- Temporal Features: Hour of day, day of week, and week number.
- Weather Features: Daily temperature, precipitation of rain and snow, and amount of snow on the ground.

**Models Used:**
- VGG-Based CNN
- ResNet-Based CNN  (superior accuracy in predicting parcel delivery times)
- Squeeze-and-Excitation (SE) Augmentation

**Model Training**
Configuration:
- Loss Function: Mean Squared Error (MSE).
- Optimizer: Adam optimizer with an initial learning rate of 10 
- Batch Size: 64 samples.
- Early Stopping: Stop training if no improvement is seen after 25 epochs.
- Learning Rate Adjustment: Reduce learning rate by half every 40 epochs.

Implementation:
- Use the Keras API with TensorFlow backend.
- Train models using an Nvidia RTX 2080 Ti GPU or equivalent.

**Model Evaluation:** 

Metrics
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)
- Mean Absolute Relative Error (MARE)
- Error Window (±EW): Specifically EW90% for 90% error window.

**Error Analysis**
- Spatial Distribution: Analyze errors across different depots.
- Distance Analysis: Evaluate errors with respect to the distance between origin and destination.
- Temporal Analysis: Assess errors against time of day, week, and delivery duration.

Errors were generally lower for deliveries starting earlier in the day and for those with longer distances, likely due to less traffic variability on highways.

Spatial and temporal patterns were identified, indicating that certain depots and times of day are more predictable than others.

**Synthetic Data Generation Survey paper:**

https://arxiv.org/html/2302.04062v6 

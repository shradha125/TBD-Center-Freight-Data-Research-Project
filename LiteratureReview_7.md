## A framework for anomaly detection in maritime trajectory behavior


Handle GPS tracking data from maritime ships, specifically mentioning the use of AIS (Automatic Identification System) data.
AIS is a tracking system used by ships traffic services to identify and locate vessels by electronically exchanging data with other nearby ships, base stations, and satellites. So the maritime trajectory data likely comes from AIS transmissions of ship positions over time, which utilizes GPS for positioning.

**Data Preprocessing**

***Frequent Region Extraction***

A grid-based clustering approach is used to extract frequent regions from the trajectory data, representing areas frequently visited by ships. 
The raw GPS trajectory data is first preprocessed to extract frequent regions visited by ships using a density-based clustering approach.

The key steps are:
***Grid Partitioning:***
The area of interest is first partitioned into equal-sized grid cells.

***Density Computation:***
Instead of counting the number of trajectory points in each cell, the density of a cell is computed by counting the number of trajectory segments passing through that cell. 
A trajectory segment is defined as the spatial segment between two consecutive location points.

***Frequent Region Criteria:***
A grid cell is identified as a frequent region if it contains at least a minimum number of trajectory segments (MinTs) passing through it.

***Iterative Clustering:***
The frequent region clustering is performed iteratively using a quarter-partitioning approach (Algorithm 1):
- Start with the entire area as a single cluster
- In each iteration, partition each cluster into four equal-sized quarter cells
- Compute density for each quarter cell
- Add quarter cells with density ≥ MinTs to the next cluster set
- Repeat until the coverage (fraction of trajectories covered by frequent regions) meets the minCover threshold

***The key parameters are:***

- MinTs: Minimum number of trajectory segments for a cell to be considered a frequent region
- minCover: Minimum coverage (fraction of trajectories) that must be achieved by the extracted frequent regions

**Feature Engineering**

***3 outlying features are engineered to characterize trajectories based on deviations from learned patterns***

- Spatial Outlying Feature: 
  Anomalies where a vessel visits a sparse or low-density region that is infrequently visited by other vessels based on historical data.

- Sequential Outlying Feature:
  The sequence of transitions between locations

- Behavioral Outlying Feature: 
  Anomalies in the motion dynamics like speed and direction. If the behavioral vector pi(t-1)pi(t) deviates significantly from typical clustered patterns for that transition, it is       considered a behavioral anomaly.

This involves computing probabilities, conditional probabilities, and distances from clustered centroids. 

The key evaluation metrics: 
Accuracy: Proximity of detected anomalies to true injected anomalies.


## Task 1: Truck Volume - To evaluate the traffic volume

**Metrics: Difference in Truck Volume from Non-peak to Peak Hours**
- Compared the Segment ID's with open source NYC DCP's open source data to get the latest active Segment ID's.
- Created a new dataframe containing the data for only those latest Segment ID's and calculated the difference in truck volume for Non-peak to Peak hours per time period. (WD Evening, WD Mid-Day, WD Morning, WE Saturday)
- Unique Segment ID's after filtering = 11118.
- Plotted a Stacked Bar Graph to visualize the difference in truck volume per time period for first 20 Segments.
- Positive values indicate the volume of trucks at the Peak hours whereas the negative values indicate the volume of trucks at the Off-Peak hours.
- Out of the sample of 20 segments, the SegmentID 9008369 which corresponds to Street 'SEDGWICK AVENUE' has the count of around 1000 trucks using the road segment on Weekday Peak morning hours and around 500 trucks using the road segment on Weekday Midday Peak hours. It indicates that this segment experiences heavy truck traffic during that time.
- Comparing usage with other segments where truck traffic is lower provides a context for understanding the relative importance and demand for "SEDGWICK AVENUE" among other road segments.
- This information highlights "SEDGWICK AVENUE" as a significant thoroughfare for truck transportation, experiencing notable traffic volumes during peak hours, which is crucial for transportation planning, infrastructure management, and understanding local traffic dynamics.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/620c7861-d60a-44d9-9a60-2cbd5a6ef121)


**Metrics: Volume of Trucks by Time Categories**
- Created a grouped bar chart (bar1 for positive counts and bar2 for negative counts) to visualize the truck volume differences across segments and time categories.
- It calculates and visualizes how many segments have positive or negative truck volume differences, providing insights into when and where truck traffic peaks or dips relative to each time category. 
- Calculated the sum of the above displayed difference in truck volumes (WD Evening, WD Mid-Day, WD Morning, WE Saturday) grouping by SegmentID.
- Result shows the Weekday Morning counts high volume during the peak hours.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/2cc0b726-c966-42ed-b56f-c2dca0f89c52)

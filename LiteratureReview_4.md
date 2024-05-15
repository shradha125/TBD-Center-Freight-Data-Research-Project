**Title: Using Truck Fleet Data in Combination with Other Data Sources for Freight Modeling and Planning**

***Citation:*** Creator(s) : Pinjari, Abdul R.;Zanjani, Akbar Bakhshi;Thakur, Aayush;Irmania, Anissa;Kamali, Mohammadreza;Short, Jeffrey;Pierce, Dave;Park, Lisa;
Corporate Creator(s) : University of South Florida. Dept. of Civil and Environmental Engineering;American Transportation Research Institute;
Published Date : 2014-07-01
Report Number : BDK84-977-20
***URL :*** https://rosap.ntl.bts.gov/view/dot/27807

***Description:***
ATRI’s truck GPS data in Florida used to measure average speeds on each mile of Florida’s SIS highway network for different time periods of the day. 

1. Develop algorithms to convert large streams of ATRI’s truck GPS data into a more useable truck trip format.
2. Analyze truck trip characteristics in Florida using ATRI’s truck GPS data. - 4 months of ATRI’s truck GPS data

These algorithms were applied to four months of raw GPS data from ATRI, comprising a total of 145 million raw GPS data records, to develop a large database of truck trips traveling within, into, and out of the state. The resulting database comprised more than 1.2
million truck trips traveling within, into, and out of the state. 

The truck travel characteristics: total trip duration, trip distance, trip speed, time-of-day profiles, and Origin Destination (OD) flows, duration of intermediate stops (e.g., at traffic signals and rest stops) in the trip.

Each record within the database contained :
1. Unit Information: A unique identifier for the transponder/truck.
2. Geographic Information: The latitude and longitude data that identify where a truck position record was recorded.
3. Temporal Information: The time at which a truck position record was recorded, format – MM-DD-YYYY HH:MM:SS.
![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/fd267b92-2456-4f5f-b498-05d9a281173d)

Unique Truck ID -> Confidential

Narrowed down to include specific segments that fall along Florida’s SIS road network (in this case).
Average speeds were calculated for each segment during each time period.

***Algorithm:***
![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/b6c60992-bd97-4f52-b064-c922ee631f81)


**Title: Expanding Truck GPS-based Passive Origin-Destination Data in Iowa and Tennessee**

https://www.researchgate.net/profile/Vince-Bernardin/publication/378036330_Expanding_Truck_GPS-based_Passive_Origin-Destination_Data_in_Iowa_and_Tennessee/links/65c408661e1ec12eff7bce32/Expanding-Truck-GPS-based-Passive-Origin-Destination-Data-in-Iowa-and-Tennessee.pdf

Understanding the representativeness of ATRI’s truck GPS data and how to weight or expand it for use in forecasting models and other analyses.

Search Term: transportation ATRI dataset in machine learning -> Google Scholar


**Title: Diffusion-based Time Series Imputation and Forecasting with Structured State Space Models**

***Citation:*** Alcaraz, J.M.L. and Strodthoff, N., 2022. Diffusion-based time series imputation and forecasting with structured state space models. arXiv preprint arXiv:2208.09399.

***Link:*** https://arxiv.org/abs/2208.09399

***Description:***
Dataset: Electricity Transformer dataset: https://github.com/AI4HealthUOL/SSSD/blob/main/src/get_data.py 

Provide imputations for different missingness scenarios that are not only quantitatively but even qualitatively superior.
Address these shortcomings by proposing a new generative-model-based approach for time series imputation. 

Also, proposed a simple yet powerful methodology in which the noise of the diffusion process is introduced just to the regions to be imputed, which turns out to be superior to approaches proposed in the context of image inpainting.

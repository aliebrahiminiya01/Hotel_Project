## Hotel Reservation Analysis

This project analyzes hotel reservation data to uncover trends, customer behavior, and booking patterns. The goal is to provide insights that can help improve hotel occupancy rates and customer satisfaction.


## Overview
This project explores and visualizes hotel reservation data using **Python** and libraries such as:
- **Pandas** – for data manipulation  
- **Matplotlib** and **Seaborn** – for data visualization  
- **NumPy** – for numerical computations  


## Objectives
- Analyze booking trends over time  
- Identify factors influencing cancellations  
- Study the impact of lead time on booking success  
- Compare customer behavior across different market segments  


## Dataset
The dataset includes the following key fields:
- `hotel` – Type of hotel (City or Resort)  
- `lead_time` – Number of days between booking and check-in  
- `arrival_date` – Date of arrival  
- `stays_in_weekend_nights` – Number of weekend nights booked  
- `adults`, `children`, `babies` – Number of guests  
- `meal` – Type of meal booked  
- `market_segment` – Source of the booking (e.g., direct, corporate)  
- `is_canceled` – Whether the booking was canceled  


## Key Findings

**1. City Hotel seem to be more successful though it has more reservations and more revenue although this hotel has 6.5 percent more cancellation than Resort hotel**

**2. Passengers mostly select the __A__, __D__, __E__ and __F__ types of rooms**

**3. Even though the minimum and mean of prices of two hotels are almost same, the City hotel with having high revenue for some conditions has a significant high amount of revenue in some reservations.**

**4. Portugal, United Kingdom, France, Spain and Germany are the 5 top nationalities between passengers booked rooms.**

**5. Online travel agencies have the greater part of the market in reserving methods.**

**6. From start of the year the number of reservations increase until August. Months July and August are the peak months in numbers of reservations. After August we can see a 
decreasing pattern. In October there is slight increase in reservation. Number of reservations in November and December are almost same, both less than October.** 

## Hotel Reservation Analysis

This project analyzes hotel reservation data to uncover trends, customer behavior, and booking patterns. The goal is to provide insights that can help improve hotel occupancy rates and customer satisfaction.


## Overview
This project explores and visualizes hotel reservation data using **Python** and libraries such as:
- **Pandas** – for data manipulation  
- **Matplotlib** – for data visualization  
- **NumPy** – for numerical computations  


## Objectives
- Analyze booking trends over time  
- Identify factors influencing cancellations  
- Study the impact of lead time on cancellations  
- Compare customer behavior across different market segments  


## Dataset
[Hotel booking demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) — 119,390 bookings of a
City Hotel and a Resort Hotel in Portugal, with arrival dates from **July 2015 to August 2017**.

The dataset includes the following key fields:
- `hotel` – Type of hotel (City or Resort)  
- `is_canceled` – Whether the booking was canceled  
- `lead_time` – Number of days between booking and arrival  
- `arrival_date_year`, `arrival_date_month` – Date of arrival  
- `stays_in_weekend_nights`, `stays_in_week_nights` – Number of nights booked  
- `adults`, `children`, `babies` – Number of guests  
- `market_segment` – Source of the booking (e.g., online travel agent, direct, corporate)  
- `deposit_type` – No Deposit / Non Refund / Refundable  
- `adr` – Average daily rate (price per night)  

**Cleaning steps:** missing values in `children`, `agent` and `company` are filled with 0, duplicate rows are removed,
and bookings with no guests or an invalid price (negative, or a single €5,400 data entry error) are dropped.
Revenue is computed as `adr × nights` for non-cancelled bookings.


## How to Run
1. Download `hotel_bookings.csv` from the Kaggle link above and save it next to the notebook as `Hotel_Bookings.csv`.
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run the notebook:
   ```bash
   jupyter notebook Hotel_Project.ipynb
   ```


## Key Findings

**1. City Hotel has 1.57 times more reservations and more total revenue (≈ €12.2M vs €10.8M), but it also has a higher cancellation rate: 30.1% vs 23.5% for Resort Hotel (6.6 percentage points more).**

**2. Room type __A__ is by far the most booked (≈ 65% of bookings), followed by __D__ (≈ 20%), __E__ (≈ 7%) and __F__ (≈ 3%). The same room types also bring the most revenue.**

**3. City Hotel rooms are more expensive on average (median adr ≈ €105 vs €80), while Resort Hotel prices vary much more (std ≈ €64 vs €42) because of strong seasonal pricing. The very large maximum price seen in the raw data (€5,400) was a single data entry error and was removed.**

**4. Portugal, United Kingdom, France, Spain and Germany are the 5 top nationalities of the guests; Portugal alone accounts for about 31% of all bookings.**

**5. Online travel agencies have the greater part of the market (≈ 59% of bookings), followed by offline travel agencies (≈ 16%) and direct bookings (≈ 14%).**

**6. In 2016 (the only complete year), January and February are the quietest months, March–July stay at a steady level (≈ 3,500–3,850 bookings), August is the peak month and October is the second busiest. The cancellation rate of Resort Hotel is clearly seasonal (lowest in winter, highest in summer), while City Hotel stays between ~25% and ~35% all year.**

**7. Lead time is strongly related to cancellations: only ≈ 8% of bookings made within a week of arrival are cancelled, compared with ≈ 35–40% of bookings made more than 3 months in advance.**

**8. Surprisingly, "Non Refund" deposits have a ≈ 95% cancellation rate. These are mostly group bookings made through agencies, so this is a known quirk of the dataset rather than evidence that deposits encourage cancellations.**

# Zomato_sales_analysis_Project_PowerBI-
Project report:-
📊 Project Overview
The Zomato Restaurants Analysis Dashboard provides an end-to-end business intelligence solution built using Power BI.
The project focuses on understanding Zomato’s global restaurant data — analyzing restaurant performance, cuisines, customer engagement, and regional distribution.
By transforming raw data into meaningful visuals, the dashboard enables stakeholders to make data-driven business decisions in the restaurant industry.

🧩 Data Modeling Process:-
After data cleaning, a structured star schema model was created to enhance analytical efficiency and reduce redundancy.
Model Design:
Fact Table:
Restaurant_Fact – Contains metrics such as Votes, Average Rating, Online Delivery, and Table Booking.
Dimension Tables:
Country_Dim – Country and region information
City_Dim – City-level details
Cuisine_Dim – Cuisine categories
Date_Dim – Date, Year, Quarter, and Month hierarchy
Relationships Established:
Restaurant_Fact[CountryID] → Country_Dim[CountryID]
Restaurant_Fact[CityID] → City_Dim[CityID]
Restaurant_Fact[CuisineID] → Cuisine_Dim[CuisineID]
Restaurant_Fact[DateKey] → Date_Dim[DateKey]
Calculated Measures (DAX):
Total Votes = SUM(Restaurant_Fact[Votes])
Total Restaurants = COUNT(Restaurant_Fact[RestaurantID])
Average Rating = AVERAGE(Restaurant_Fact[Rating])
Online Delivery % = DIVIDE(CALCULATE(COUNTROWS(Restaurant_Fact), Restaurant_Fact[OnlineDelivery] = "Yes"), COUNTROWS(Restaurant_Fact))
Table Booking % = DIVIDE(CALCULATE(COUNTROWS(Restaurant_Fact), Restaurant_Fact[TableBooking] = "Yes"), COUNTROWS(Restaurant_Fact))
This model allowed dynamic filtering and drilling down by city, cuisine, or year.
The Power BI dashboard includes interactive visuals, filters, and KPIs to present clear insights:

Visualization	Description:-
KPI Cards:	show overall metrics: Total Restaurants, Cuisines, Countries, Cities, Total Votes, and Average Rating
Bar Chart: (City-Wise)	Displays the number of restaurants in major cities
Combo Chart: (Cuisines vs Ratings)	shows how cuisines perform based on average ratings
Horizontal Bar Chart: (Cuisine-wise)	represents the restaurant count per cuisine type
Donut Charts: Visualize the proportion of restaurants offering Online Delivery and Table Booking
Filters/Slicers: Allow filtering by Year and Country to explore trends interactively.

💡 Key Insights:-
India dominates the dataset with the highest number of restaurants, followed by the UAE and the UK.
New Delhi leads the city-wise list with over 5,000 restaurants listed on Zomato.
North Indian cuisine is the most popular, followed by Chinese and Fast Food.
The average rating across all restaurants is 2.89, showing a moderate satisfaction level.
Approximately 70% of restaurants offer online delivery, indicating a high level of digital adoption in the food service industry.
Only 12–15% of restaurants provide table booking, which may signal potential for market growth.




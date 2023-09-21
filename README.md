## Dynamic & Interactive Pizza Sales Dashboard By Tableau & SQL 👇

Please visit my Tableau Public Profile to Access the Project: https://public.tableau.com/app/profile/kunal7999/viz/Pizza_Sales_Proj_1/Home

For this Project First, we Used Tableau to create interactive and dynamic Dashboards and uploaded .csv File to Microsoft SQL Server where we Pre-processed the data ~ (ETL), and then created a Validation Report (Performed Complex SQL Queries) to Justify/ Validate the KPI's or Different Charts that we are showing through our Viz. Also, it will help our Business Clients to make important Decisions.

1.) Dataset Overview
In this Project, I have used Pizza Sales Dataset for the Year 2015, which has the following Attributes:
Categorical Variables
Pizza Name, Pizza Size (S, M, L, XL), Pizza Category (Classic, Veggie, Supreme, Chicken), Pizza Ingredient, Pizza Name
Numerical Variables (Discrete & Continous)
Pizza Id - Primary Key Unique ID for each Pizza, Order Id: Can have duplicates, Quantity: How Many Number of Pizza's, Unit Price/ Total Price: The Price of Each Pizza for specific Order & with specific Quantity.
Data & Time: Order Date: DD-MM-YYYY, Order Time: HH:MM:SS

2.) Problem Statement
A. KPI's Requirement
We need to analyze key indicators for our pizza sales data to gain insights into our business performance. Specifically, we want to calculate the following metrics:

Total Revenue: The sum of the total price of all pizza orders.
Average Order Value: The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
Total Pizzas Sold: The sum of the quantities of all pizzas sold.
Total Orders: The total number of orders placed.
Average Pizzas Per Order: The average number of pizzas sold per order, is calculated by dividing the total number of pizzas sold by the total number of orders.

B. Charts Requirement
We would like to visualize various aspects of our pizza sales data to gain insights and understand key trends. We have identified the following requirements for creating charts:
Hourly Trend for Total Pizzas Sold:
Create a stacked bar chart that displays the hourly trend of total orders over a specific period. This chart will help us identify any patterns or fluctuations in order volumes on an hourly basis.
2. Weekly Trend for Total Orders:
Create a line chart that illustrates the weekly trend of total orders throughout the year. This chart will allow us to identify peak weeks or periods of high-order activity.
3. Percentage of Sales by Pizza Category:
Create a pie chart that shows the distribution of sales across different pizza categories. This chart will provide insights into the popularity of various pizza categories and their contribution to overall sales.4
3.1 % Of Sales by Pizza Categories for the Month of January only, Quarter 1, Combined Months

4. Percentage of Sales by Pizza Size:
Generate a pie chart that represents the percentage of sales attributed to different pizza sizes. This chart will help us understand customer preferences for pizza sizes and their impact on sales.
4.1 E.1) % Of Sales for each Pizza Size of A Particular category
5. Total Pizzas Sold by Pizza Category:
Create a funnel chart that presents the total number of pizzas sold for each pizza category. This chart will allow us to compare the sales performance of different pizza categories.
6. Top 5 Best Sellers by Revenue, Total Quantity and Total Orders
Create a bar chart highlighting the top 5 best-selling pizzas based on the Revenue, Total Quantity, and Total Orders. This chart will help us identify the most popular pizza options.
7. Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders
Create a bar chart showcasing the bottom 5 worst-selling pizzas based on the Revenue, Total Quantity, and Total Orders. This chart will enable us to identify underperforming or less popular pizza options.

3.) Tools & Technologies

MS OFFICE/ EXCEL: VERSION 2021
MS SQL SERVER: 19.0
SQL SERVER MANAGEMENT STUDIO – 19.0.20209.0
TABLEAU DESKTOP: 2023.3.0
MS POWERPOINT: FOR Creating INTERACTIVE Backgrounds WITH SUB BLOCKS

4.) Data Gathering, Pre-Processing, and loading Data into Microsoft SQL Server
The data is downloaded from the official Kaggle website.
Here the data is in .xlsx format, we need to convert it to .csv as only .csv files are loaded in Micro. SQL Server.
Import The data as a Flat File into the SQL Server, and create a Database using the current connection.
After Loading we need to do some Pre-processing such as:
1.) Change the Data Types of some Attributes according to the type of data it has:
Pizza Id: smallest - Default Dt assigned by SQL Server to Int
Order Id: tinyint - int
Pizza Size : nvarchar(50) -> varchar(50)
Pizza Category nvarchar(50) -> varchar(50)
Pizza Ingredients varchar(50) -> varchar(200) ~ as No. of ingredients can have more than 150 Words
Pizza Name: nvarchar(50) -> varchar(50)
2.) Rename the Pizza Size Column as ~ so that they are understood by the Clients --> not commit if not want to change the original Database
S - Small
M - Medium
L - Large
XL - X Large
XXL - XX-Large
3.) Handling Null/Missing Values: By taking the Mean, Median and mode of that particular column & replacing the Null values with it
4.) Handling Noisy Data/Outliers: Performing Min/Max Normalization where the values will lie in the range [0.1] 

5.) Performing & writing Validation Queries to test the Results of the Dashboard

6.) Creating 2 To & Fro Dashboards: 
1.) Home Page ~ Landing or Main Page, 2.) Best/ Worst Pizza Sellers 

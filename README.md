## Dynamic & Interactive Pizza Sales Dashboard By Tableau & SQL 👇 

Project Link: https://public.tableau.com/app/profile/kunal7999/viz/Pizza_Sales_Proj_1/Home

📈 For this project, I utilized Tableau to create interactive and dynamic dashboards. I uploaded a .csv file to Microsoft SQL Server, where the data was pre-processed using ETL (Extract, Transform, Load) techniques. Subsequently, I created a validation report by performing complex SQL queries to justify and validate the visualizations presented in Tableau.

I developed various charts and interactive dashboards, including a "Home" dashboard and dashboards showcasing the best and worst-selling pizzas. Additionally, I highlighted five key performance indicators (KPIs) that significantly impact pizza sales. 

This project aims to assist clients in the pizza business by providing valuable insights through real-time data analytics dashboards, enabling them to make informed decisions to improve their sales.

### 1. Dataset Overview

In this Project, I have used Pizza Sales Dataset for the Year 2015, which has the following Attributes:
<ul>
<b><li> Categorical Variables </li></b>
Pizza Name, Pizza Size (S, M, L, XL, XXL), Pizza Category (Classic, Veggie, Supreme, Chicken), Pizza Ingredient, Pizza Name
<b><li> Numerical Variables (Discrete & Continous) </li></b>
Pizza Id - Primary Key Unique ID for each Pizza, Order Id: Can have duplicates, Quantity: How Many Number of Pizza's, Unit Price/ Total Price: The Price of Each Pizza for specific Order & with specific Quantity.
<b><li> Data & Time Variables: </li></b> Order Date: DD-MM-YYYY, Order Time: HH:MM:SS </ul>

### 2. Problem Statement
<ol>
<b><li> KPI's Requirement </li></b>
<br>
We need to analyze key indicators for our pizza sales data to gain insights into our business performance. Specifically, we want to calculate the following metrics:
<ul>
  <br>
<b><li> Total Revenue:</b> The sum of the total price of all pizza orders. 
<b><li> Average Order Value: </b> The average amount spent per order, calculated by dividing the total revenue by the total number of orders.
<b><li> Total Pizzas Sold: </b> The sum of the quantities of all pizzas sold.
<b><li>Total Orders: </b> The total number of orders placed.
<b><li> Average Pizzas Per Order: </b> The average number of pizzas sold per order, is calculated by dividing the total number of pizzas sold by the total number of orders. </ul>
<br>
<b><li> Charts Requirement </li></b>
<br>
We would like to visualize various aspects of our pizza sales data to gain insights and understand key trends. We have identified the following requirements for creating charts:
<br>
<ul> 
<br>
<b><li> Hourly Trend for Total Pizzas Sold: </b>
Create a stacked bar chart that displays the hourly trend of total orders over a specific period. This chart will help us identify any patterns or fluctuations in order volumes on an hourly basis.
<b><li> Weekly Trend for Total Orders: </b>
Create a line chart that illustrates the weekly trend of total orders throughout the year. This chart will allow us to identify peak weeks or periods of high-order activity.
<b><li> Percentage of Sales by Pizza Category: </b>
Create a pie chart that shows the distribution of sales across different pizza categories. This chart will provide insights into the popularity of various pizza categories and their contribution to overall sales.4
<b><li> Percentage of Sales by Pizza Size: </b>
Generate a pie chart that represents the percentage of sales attributed to different pizza sizes. This chart will help us understand customer preferences for pizza sizes and their impact on sales.
<b><li> Total Pizzas Sold by Pizza Category: </b>
Create a funnel chart that presents the total number of pizzas sold for each pizza category. This chart will allow us to compare the sales performance of different pizza categories.
<b><li> Top 5 Best Sellers by Revenue, Total Quantity and Total Orders: </b>
Create a bar chart highlighting the top 5 best-selling pizzas based on the Revenue, Total Quantity, and Total Orders. This chart will help us identify the most popular pizza options.
<b><li> Bottom 5 Best Sellers by Revenue, Total Quantity and Total Orders: </b>
Create a bar chart showcasing the bottom 5 worst-selling pizzas based on the Revenue, Total Quantity, and Total Orders. This chart will enable us to identify underperforming or less popular pizza options. 
</ol> </ol>

### 3. Tools & Technologies
<ul>
<li><b> MS OFFICE/EXCEL :</b> VERSION 2021 
<li><b> MS SQL SERVER :</b> 19.0
<li><b> SQL SERVER MANAGEMENT STUDIO :</b> 19.0.20209.0
<li><b> TABLEAU DESKTOP :</b> 2023.3.0
<li><b> MS POWERPOINT :</b> FOR Creating INTERACTIVE Backgrounds WITH SUB BLOCKS </li>
</ul>

### 4. Data Gathering, Pre-Processing, and loading Data into Microsoft SQL Server

<ul>
<li> The Data is downloaded from the official Kaggle website.
<li> Here the data is in .xlsx format, we need to convert it to .csv as only .csv files are loaded in Micro. SQL Server.
<li> Import The data as a Flat File into the SQL Server, and create a Database using the current connection.
<li> After Loading we need to do some Pre-processing such as: </ul>

<ol>
<b><li> Change the Data Types of some Attributes according to the type of data it has: </b></li>
Pizza Id: smallest - Default Dt assigned by SQL Server to Int
Order Id: tinyint - int
Pizza Size : nvarchar(50) -> varchar(50)
Pizza Category nvarchar(50) -> varchar(50)
Pizza Ingredients varchar(50) -> varchar(200) ~ as No. of ingredients can have more than 150 Words
Pizza Name: nvarchar(50) -> varchar(50)

<b><li>  Rename the Pizza Size Column as ~ so that they are understood by the Clients --> not commit if not want to change the original Database </b></li>
S - Small
M - Medium
L - Large
XL - X Large
XXL - XX-Large

<b><li> Handling Null/Missing Values: </b></li> By taking the Mean, Median and mode of that particular column & replacing the Null values with it 

<b><li> Handling Noisy Data/Outliers: </b></li> Performing Min/Max Normalization where the values will lie in the range [0,1] 
</ol>

### 5. Performing & writing Validation Queries to test the Results of the Dashboard 

<img src = "https://github.com/KunalAnand2907/Dynamic_PizzaSalesReport_ByTableau_SQL/assets/46574881/01e3d543-0cf5-4b8f-b1e6-7d9e964292d3">

### 6. Created 2 To & Fro Dashboards:

<p align="center"> <b>1.) Home Page ~ Landing or Main Page</b></p>

![Screenshot 2023-09-18 042209](https://github.com/KunalAnand2907/Dynamic_PizzaSalesReport_ByTableau_SQL/assets/46574881/a5105283-a3fb-4a28-b69c-01101d0908aa)


<p align="center"> <b> 2.) Best/ Worst Pizza Sellers </b></p>


![Screenshot 2023-09-18 042326](https://github.com/KunalAnand2907/Dynamic_PizzaSalesReport_ByTableau_SQL/assets/46574881/e690fc3c-0103-4c6d-9dae-34ee77aa4def)


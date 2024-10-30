# Laptop Price Data Analysis
---
![Main Image](https://github.com/Zhiweikau/Laptop_Price_Analysis-Python-Tableau/blob/main/Report%20Images%20and%20Icon/Main%20Image.jpg)

## Table of Contents


### Project Overview
This project involves analysis a laptop price dataset using Python and Tableau. The goal is to explore various factors that influence laptop pricing and identify trends, patterns, and key insights that can help consumers make informed purchasing decisions and help manufacturers optimize their pricing strategies.

---

### Objectives
-	To identify key factors and attributes that significantly influence laptop prices, including screen resolution (ScreenResolution), processor performance, and laptop type (e.g., Ultrabook, Notebook).
-	To develop interactive visualizations that enable users to explore and compare laptop prices by different attributes, helping to identify trends and price variations across brands and specifications.
-	To provide insights and recommendations based on the visualized data to guide consumers and businesses in understanding the laptop market and making informed purchasing or marketing decisions.

---

### Data Source
- [Kaggle](https://www.kaggle.com/datasets/muhammetvarl/laptop-price)

---

### Terminologies Used in Data
Dataset of laptop_price csv file:
-	laptop_ID: An identifier for each laptop.
-	Company: The brand or manufacturer of the laptop (e.g., Apple, HP).
-	Product: The model’s name of the laptop.
-	TypeName: The category/type of the laptop (e.g., Ultrabook, Notebook).
-	Inches: The screen size of the laptop in inches.
-	ScreenResolution: The display resolution and panel type of the screen.
-	Cpu: Information about the processor, including brand and clock speed.
-	Ram: The amount of RAM in the laptop (e.g., 8GB, 16GB).
-	Memory: The storage type and capacity (e.g., SSD, HDD).
-	Gpu: The graphics card details.
-	OpSys: The operating system installed on the laptop.
-	Weight: The weight of the laptop.
-	Price_euros: The price of the laptop in euros.

---

### Methodology
#### Our approach to analysing laptop sales data was methodical and multi-phased, ensuring both data integrity and insightful visualization. The stages of our methodology are as follows:
**Data Ingestion and Preprocessing**
- Objective: To establish a structured foundation for data analysis.
- Process:
1. Data Loading: The laptop sales dataset was ingested using Python’s pandas library to facilitate efficient data handling and transformations.
2. Data Cleaning: Initial data preprocessing involved verifying data types for accuracy, checking for any missing values, and performing adjustments to ensure data consistency and completeness.
3. Data Validation: Columns were verified for correct data types (e.g., Weight and Price as a float, Ram as strings converted to integers) to ensure analytical accuracy.

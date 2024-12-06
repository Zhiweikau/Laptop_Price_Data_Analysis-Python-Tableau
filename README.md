# Laptop Price Data Analysis
---
![Main Image](https://github.com/Zhiweikau/Laptop_Price_Analysis-Python-Tableau/blob/main/Report%20Images%20and%20Icon/Main%20Image.jpg)

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives) 
-	[Data Source](#data-source) 
-	[Terminologies Used in Data](#terminologies-used-in-data) 
-	[Methodology](#methodology) 
-	[Tools and Technologies Used](#tools-and-technologies-used) 
-	[Visualization Requirement for Laptop price Analysis](#visualization-requirement-for-laptop-price-analysis)
-	[Data Visualization Interfaces](#data-visualization-interfaces)
-	[Key Insights and Findings](#key-insights-and-findings)
-	[Recommendations](#recommendations)
-	[Getting Started](#getting-started)
-	[Conclusion](#conclusion)
-	[MIT License](#mit-license)


### Project Overview
This project involves analysis a laptop price dataset using Python and Tableau. The goal is to explore various factors that influence laptop pricing and identify trends, patterns, and key insights that can help retailers make informed purchasing decisions and help manufacturers optimize their pricing strategies.

---

### Objectives
-	To identify key factors and attributes that significantly influence laptop prices, including screen resolution (ScreenResolution), processor performance, and laptop type (e.g., Ultrabook, Notebook).
-	To develop interactive visualizations that enable users to explore and compare laptop prices by different attributes, helping to identify trends and price variations across brands and specifications.
-	To provide insights and recommendations based on the visualized data to guide retailers and businesses in understanding the laptop market and making informed purchasing or marketing decisions.

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

**Data Transformation**
- Objective: To enrich the dataset with derived columns that support more in-depth analysis.
- Process:
1. Feature Engineering: 
- 1. New columns were created for ease of analysis. For example, a Touchscreen and IPS columns was added to indicate whether a laptop has touchscreen functionality and an IPS display (1/0) mean “Yes” or “No”. These additions allowed for a more detailed analysis of how display features affect laptop prices and consumer preferences.
- 2. x_resolution and y_resolution columns were created to store the horizontal and vertical resolution values of each laptop screen. These two columns were then used to derive a new column, PPI (Pixels Per Inch), which measures the pixel density of the screen. This PPI metric provided valuable insights into display quality across different models and the formula as following:
![PPI Forula:](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Report%20Images%20and%20Icon/PPI.png)
- 3. CPU Brand column was created and categorised into Intel Core i3, Intel Core i5, Intel Core i7, AMD Processor and Other Intel Processor.
- 4. GPU Brand column was created and categorised into Intel, Nvidia, AMD and ARM.
- 5. OS columns was created was created and categorized into Windows, Mac and Others/No OS/Linux.
2. Data Standardization: Units for attributes like Ram and Weight were standardized (e.g., removing 'GB' or 'kg') to allow numerical comparisons.

**Exploratory Data Analysis (EDA)**
- Objective: To gain an initial understanding of the distributions within the dataset.
- Process:
1. Descriptive Statistics: Key statistical measures (mean, median, mode) were calculated for continuous field.
2. Correlation Analysis: Checking the relationship of the relevant features with the Price.

**Feature-Specific Analysis**
- Objective: Analysis relationships between laptop features and price for insights into sales performance.
- Process:
1. Overall Metrics: Calculated Total Amount, Total Quantity, and Average Amount per Quantity.
2. Feature-Based Analysis: Created tables and breakdowns for Company and RAM, screen size, touchscreen, IPS, CPU, GPU, and OS preferences.

**Visualization in Tableau**
- Objective: Present findings through clear, interactive visualizations.
- Process:
1. Single-Value Metrics: Displayed key totals and averages.
2. Tables and Charts: Developed tables and stacked bar charts for feature-specific sales metrics; created pie charts for sales distribution across TypeName, CPU, GPU, and OS.

---

### Tools and Technologies Used
- <img src="https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Report%20Images%20and%20Icon/Jupyter%20Notebook%20Icon.png" alt="Jupyter Notebook Icon" width="30" height="30"> Python: Utilized for data cleaning, transformation, exploratory data analysis (EDA), and feature engineering in the laptop price analysis project. Python libraries such as Pandas and NumPy enabled efficient data handling, including loading datasets, handling encoding issues, removing duplicates, and managing missing values. Data types were adjusted for accurate analysis, with transformations applied to columns such as RAM, Weight, and Price for consistency. Feature engineering techniques included creating binary indicators for touch screens and IPS displays, as well as calculating screen resolutions, to enrich the dataset for more insightful analysis.
- <img src="https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Report%20Images%20and%20Icon/Tableau%20Icon.png" alt="Tableau Icon" width="30" height="30"> Tableau: A powerful data visualization and business intelligence tool used to create interactive dashboards and visual reports. Tableau was utilized to transform the prepared data into clear visual insights, highlighting key findings from the analysis. This approach allowed stakeholders to easily interpret complex patterns and relationships in the dataset, enhancing data-driven decision-making.

---

### Visualization Requirement for Laptop price Analysis
These visualizations offer insights into pricing trends, brand positioning, and the impact of specifications on laptop prices.
1.	**Total Amount:** A single value showing the sum of all laptop prices and it gives an overview of the overall sales amount.
2.	**Total Quantity:** A single value showing the total number of laptops and it provides insight into total sales volume.
3.	**Average Amount per Quantity:** A calculated value showing the average price per laptop, providing insight into the typical expenditure per unit.
4.	**Total Amount, Total Quantity and Average Amount per Quantity by Company, RAM (Table):** A table format displaying the total amount and quantity and the Average Amount per Quantity for each combination of company and RAM size. This helps identify high-performing brands and preferred RAM configurations.
5.	**Total Amount and Total Quantity by Inches (Bar Chart):** Shows the combined amount and quantity for each screen size. This visualization reveals which screen sizes contribute most to overall sales and volume.
6.	**Total Amount and Total Quantity by Touchscreen (Bar Chart):** Compares total amount and quantity between touchscreen and non-touchscreen laptops, providing insights into consumer preferences for touchscreen functionality.
7.	**Total Amount and Total Quantity by IPS (Bar Chart):** Compares sales for laptops with and without IPS screens, showing demand for IPS technology.
8.	**Percentage of Total Amount and Total Quantity by TypeName (Bar Chart):** Shows the share of total amount and quantity across different laptop types. 
9.	**Percentage of Total Amount and Total Quantity by CPU Brand (Bar Chart):** Displays the distribution of sales by CPU brand, revealing brand popularity and contribution to sales.
10.	**Percentage of Total Amount and Total Quantity by GPU Brand (Bar Chart):** Breaks down the total amount and quantity by GPU brand, offering insights into preferred GPU choices among consumers.
11.	**Percentage of Total Amount and Total Quantity by OS (Bar Chart):** Shows the distribution of sales by operating system, reflecting OS preferences and their impact on sales.

---

### Data Visualization Interfaces
Dive deeper into our laptop price analysis project with our interactive dashboards! These visualizations provide an intuitive way to explore data, spotlight key metrics, and uncover actionable insights, making the analysis of laptop prices both engaging and insightful.
| Tool      | Tableau                                                                                                                                                                                                                              |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Overview  | The dashboards present a detailed analysis of laptop prices across various brands, specifications, and feature attributes. This interactive visualization offers a comprehensive breakdown of total sales amount, quantity sold, and average price per unit, making it easy to understand how different features impact laptop pricing and sales. Users can explore data based on factors such as type, brand, RAM, screen size, and more, enabling deeper insights into pricing trends and market preferences. |
| Features  | - **KPIs**: Key metrics like Total Amount, Total Quantity, and Average Price per Unit.  <br>- **Type Analysis**: Sales breakdown by laptop type (Notebook, Gaming, etc.). <br>- **GPU & CPU Analysis**: Distribution of sales by GPU (Intel, Nvidia, AMD) and CPU brands. <br>- **OS Analysis**: Sales and quantity by operating system (Windows, Mac, Linux). <br>- **Brand & RAM Analysis**: Price and quantity by brand and RAM size. <br>- **Screen Size**: Sales insights by screen size (inches). <br>- **Touchscreen & IPS Display**: Impact of touchscreen and IPS on sales and quantity.  |

### Laptop Price Distribution by Features
![Dashboard Price Distribution by Features](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Tableau/Dashboard%20-%20Laptop%20Price%20Distribution%20by%20Features.png)

### Performance Metrics
![Dashboard Performance Metrics](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Tableau/Dashboard%20-%20Performance%20Metrics.png)

---

### Key Insights and Findings
**Total Sales Performance:**
-	The overall sales amount is €1,463,505 across 1,302 units, with an average price per unit of €1,124. This shows a healthy sales volume and a mid-range average price point.

**Screen Size:**
-	15.6 inches is the most popular screen size, generating the highest sales amount and quantity. This suggests a standard preference for mid-sized laptops, which balances portability and usability.
-	Larger screen sizes (17.3 inches) contribute significantly to the sales amount, possibly due to higher prices for larger display models.

**Touchscreen and IPS Display Impact:**
-	Non-touchscreen laptops overwhelmingly dominate sales, indicating that touchscreen capability might not be a key priority for most buyers.
-	IPS displays contribute substantially to the total sales, reflecting a preference for better screen quality among consumers.

**Price and RAM Analysis by Brand:**
-	Dell and Lenovo stand out with the highest total sales amounts, reporting figures of €352,262 and €322,656, respectively. This success can be attributed to their extensive range of RAM options, which include 2GB, 4GB, 6GB, 8GB, 12GB, 16GB, and 32GB.
-	Average amount per unit sold, Razer leads the category with an average of €3,346, despite having a total quantity of only seven units. This is largely due to the fact that customers tend to select higher RAM configurations, specifically 16GB and 32GB options.

**Laptop Type Distribution:**
-	Notebooks account for the largest share, making up 55.84% of total quantity sold, followed by Ultrabooks (15.05%) and Gaming laptops (15.75%). Notebooks dominate both in quantity and revenue, suggesting they are the most popular type in the market.
-	Workstations and Netbooks have the lowest sales, indicating a niche or limited demand.

**GPU and CPU Preferences:**
-	Intel GPUs are the most popular, with 55.45% of total units sold, followed closely by Nvidia (30.72%). AMD GPUs have a smaller share, which may indicate a lower preference or availability.
-	Intel i7 CPUs lead in terms of both total sales amount and quantity (57.46% of sales amount), suggesting high demand for performance-oriented laptops. Intel i5 follows as a balanced choice for cost and performance, while AMD processors hold a minor share.

**Operating System:**
-	Windows is the dominant OS, representing 91.45% of total sales, while Mac and Linux options are minimal. This indicates a strong market preference for Windows laptops.

---

### Recommendations
**Focus on Popular Screen Sizes:**
-	Product Line Expansion: Given the popularity of 15.6-inch laptops, consider expanding the range of models in this category, including variations in specifications (e.g., RAM, storage) and styles (e.g., colour options, designs).
-	Marketing Campaigns: Launch targeted marketing campaigns that highlight the advantages of mid-sized laptops, emphasizing their balance between portability and usability.

**Enhance IPS Display Offerings:**
-	Increase the number of models with IPS displays, as this feature significantly contributes to consumer satisfaction. Highlight the benefits of IPS technology, such as better colour accuracy and viewing angles, in marketing materials.

**Target Notebooks and Ultrabooks:**
-	Continue to promote notebooks, as they account for the majority of sales. Consider developing ultrabooks that emphasize lightweight design and longer battery life, catering to business professionals and students.

**Expand Marketing for Intel Products:**
-	Given the strong preference for Intel CPUs and GPUs, consider strategic partnerships or sponsorships with Intel to highlight performance benefits in your advertising.

**Enhance the Windows Offering:**
-	With Windows dominating the OS market, ensure that your laptops are optimized for the latest Windows features and updates. Consider bundling software that enhances user experience, such as productivity or gaming applications.

---

### Getting Started
Prerequisites:
-	Jupyter Notebook: Used for data loading, transformation, feature engineering, correlation analysis, and metric calculations.
-	Tableau: Utilized for creating and visualizing interactive dashboards.

Installation and Setup
1.	Clone the Repository:
    ```bash
    [https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau]
    ```

2. Dataset Setup in Python:
-	Import Required Libraries: Import the necessary libraries for database interaction and data manipulation.
-	Load Data from CSV: Read the [laptop_price.csv file](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Dataset/laptop_price.csv) into a pandas DataFrame.

3.	EDA and Metrics Calculation:
-	Run the [code](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Python/Laptop%20Price%20Data%20Analysis.ipynb) by Python

4. Create a new CSV file:
-	Save the new version dataset as [new_laptop_price.csv file](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Dataset/new_laptop_price.csv)

5. Tableau Setup:
-	Launch the provided [Tableau](https://public.tableau.com/app/profile/zhi.wei.kau/viz/LaptopPriceVisualization/Dashboard1)
-	Tableau connect the [new_laptop_price.csv file](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/Dataset/new_laptop_price.csv)

---

### Conclusion
The analysis of the laptop pricing data conducted using Python for data cleaning and transformation, alongside the calculation of key performance indicators (KPIs), has yielded significant insights into market dynamics and pricing strategies. Python's robust data manipulation capabilities facilitated the extraction of meaningful patterns from the dataset, ensuring accuracy in the computation of essential metrics.

Tableau further enhanced the analysis by providing intuitive and interactive visualizations, allowing for a clear representation of trends and relationships within the data. This visualization capability has proven crucial in highlighting critical aspects such as pricing trends, sales performance across different segments, and customer preferences, enabling a comprehensive understanding of the factors influencing sales.

Overall, this data project effectively leverages the strengths of Python and Tableau to identify actionable insights and opportunities for optimization. The findings will support informed business decisions aimed at refining pricing strategies, improving sales performance, and ultimately enhancing the customer experience. Through the integration of advanced data processing and visualization techniques, this project sets a solid foundation for ongoing analysis and strategic planning within the competitive landscape of the laptop market.

---

### MIT License
This project is released under the [MIT License](https://github.com/Zhiweikau/Laptop_Price_Data_Analysis-Python-Tableau/blob/main/LICENSE), permitting you to freely use, modify, and share the codebase, provided that the original license and copyright notice are retained.

### Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Zhi%20Wei%20Kau-blue?logo=linkedin)](https://www.linkedin.com/in/zhi-wei-kau-945338243/)

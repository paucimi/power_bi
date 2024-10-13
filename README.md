# Power_bi
Hands-on Power BI Data Analysis and Visualization

# UK E-Commerce Sales Dashboard

## Project Overview
This project presents an interactive Power BI dashboard designed for a UK-based e-commerce company specializing in selling gifts for all occasions. The dashboard focuses on providing insights into sales performance, customer behavior, and product returns. The primary goal of the analysis is to identify top-selling products, reduce returns, and optimize sales by region and product category.

## Business Case
The e-commerce company aims to better understand its sales performance and customer purchasing patterns. The goals of the analysis are to:

- Increase sales by identifying the most popular products and regions with high revenue.
- Reduce returns by analyzing return reasons.
- Optimize performance across different regions and customer segments.

## Key Features of the Dashboard
- **Total Sales by Region:** A bar chart that displays total sales across various regions of the UK, allowing users to understand geographic sales distribution.
- **Top-Selling Products:** A tree map that highlights the most popular product categories based on average sales order value.
- **Sales and Average Order Value by Gender:** A combination chart that shows the sales breakdown by gender, along with the average order value, to provide insights into customer behavior.
- **Reasons for Product Returns:** A donut chart displaying the top reasons for returns, segmented by categories like excessive discount, low sales amount, and others.


## KPIs and Metrics
- **Total Sales:** The total revenue generated during the analysis period.
- **Return Percentage:** The percentage of total orders that were returned, calculated as:
  ```powerbi
  Return_Percentage = DIVIDE(COUNT(Returns[Order_ID]), COUNT(Orders[Order_ID]), 0)

  Avg_Sales_Per_order = DIVIDE(SUM(Orders[Sales_Amount]), DISTINCTCOUNT(Orders[Customer_ID]))

## Data Sources
The dashboard uses the following data tables:

- **Orders**: Contains sales-related information such as order ID, sales amount, product, and customer data.
- **Products**: Contains product details including category and product name.
- **Retailers**: Includes information about the retailer locations (region, country).
- **Returns**: Tracks returns, including the order ID and reason for return.

## Technical Features

- **Interactivity**: The dashboard features slicers that allow users to filter data by year, product category, and gender, providing a dynamic way to explore the data.
  
- **Calculated Columns and Measures**: Custom DAX measures have been used to calculate key performance indicators such as:
  - Return Percentage
  - Average Sales per Customer
  - Returns by Category or Product

- **Visualizations**: The dashboard includes bar charts, donut charts, and tree maps to visualize sales, returns, and performance across different segments.

## How to Use the Dashboard

- **Explore Sales by Region**: Use the bar chart to identify regions that generate the most sales. Filter by year to compare performance across time.
- **Analyze Product Returns**: The donut chart highlights the main reasons for returns, helping to understand why customers return certain products.
- **Understand Customer Behavior**: Use the sales and average order value chart to analyze how sales differ between male and female customers, and which products are driving the most revenue.
- **Top-Selling Products**: The tree map visualizes the most popular product categories, helping identify key products that drive revenue.

## Future Improvements

- **Customer Retention Metrics**: If customer-level data becomes available, future iterations could focus on customer retention analysis, such as repeat purchase rates or customer lifetime value (CLV).
- **Tied to Marketing Data**: If marketing data (e.g., cost per acquisition, ad spend) becomes available, further insights into return on investment (ROI) and customer acquisition costs could be added.

## Project Setup

To replicate this project:

1. **Install Power BI Desktop**: Download Power BI Desktop from the [official website](https://powerbi.microsoft.com/).
2. **Load Data**: Import the Excel files (`Orders.xlsx`, `Products.xlsx`, `Retailers.xlsx`, `Returns.xlsx`) into Power BI.
3. **Create Relationships**: Ensure that relationships between tables are correctly established, especially between Orders, Products, and Returns.
e calculated columns and measures for KPIs like total sales, return percentage, and average order value.
Build Visualizations: Add bar charts, donut charts, and tree maps, ensuring appropriate interactivity through slicers and filters.
Publish or Share: Once the dashboard is complete, it can be published to Power BI Service for sharing with stakeholders.
License
This project is licensed under the MIT License - see the LICENSE

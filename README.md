# Monday Coffee Co. – India Expansion Analysis (SQL - PYTHON)

# Table of Contents

- [Objective](#objective)
- [Key Research Questions](#key-research-questions)
- [Tools and Technologies](#tools-and-technologies)
- [Repository Structure](#repository-structure)
- [Environment Setup and Installation](#environment-setup-and-installation)
- [Analysis Overview](#analysis-overview)
- [Key Insights and Recommendations](#key-insights-and-recommendations)
- [Conclusion](#conclusion)

## Objective

This project analyzes the sales data of Monday Coffee Co.—which has been selling its products online since January 2023—with the goal of recommending the top three major cities in India to open new coffee shop locations. The recommendations are based on consumer demand, sales performance, and various market indicators.

## Key Research Questions

The analysis is structured around several critical questions:

- **Coffee Consumers Count:**  
  How many people in each city are estimated to consume coffee (assuming 25% of the population)?

- **Total Revenue from Coffee Sales:**  
  What is the total revenue generated from coffee sales across all cities in the last quarter of 2023?  
  *Additionally, which cities contributed the most revenue?*

- **Sales Count for Each Product:**  
  How many units of each coffee product have been sold?

- **Average Sales Amount per City:**  
  What is the average sales amount per customer in each city?

- **City Population and Coffee Consumers:**  
  Provide a list of cities along with their populations and the estimated number of coffee consumers.

- **Top Selling Products by City:**  
  What are the top 3 selling products in each city based on sales volume?

- **Customer Segmentation by City:**  
  How many unique customers are there in each city who have purchased coffee products?

- **Average Sale vs Rent:**  
  What is the average sale per customer compared to the average rent per customer in each city?

- **Monthly Sales Growth:**  
  What is the percentage growth (or decline) in sales on a monthly basis by city?

- **Market Potential Analysis:**  
  Identify the top 3 cities based on highest total sales. For each, return key metrics such as total sales, total rent, number of customers, and estimated coffee consumers.

## Tools and Technologies

The following tools and libraries were used throughout the project:

- **Jupyter Notebook:** For writing and executing Python code, visualizing data, and documenting the analysis.
- **Python:** For data processing, executing SQL queries, and creating visualizations.
- **SQLAlchemy:** To connect to a PostgreSQL database and run SQL queries from Python.
- **Matplotlib & Seaborn:** To create various charts (bar charts, line charts, donut charts, scatter plots) for data visualization.
- **Pandas & NumPy:** For data cleaning, transformation, and analysis.
- **Graphviz:** To generate a visual diagram of the relationships between tables in the database.
- **PrettyTable:** To display SQL query results in a formatted table.
- **PostgreSQL & SQL:** For data storage, table creation, and running SQL queries.

## Repository Structure

- Monday Coffee Co. India Expansion Analysis.ipynb - Main Jupyter Notebook with complete analysis
  
- schemas.sql - SQL script to create and define tables (city, customers, products, sales)
  
- city.csv - CSV file with city data (city_id, city_name, population, estimated_rent, city_rank)
  
- customers.csv - CSV file with customer data (customer_id, customer_name, city_id)
  
- products.csv - CSV file with product data (product_id, product_name, price)
  
- sales.csv - CSV file with sales data (sale_id, sale_date, product_id, customer_id, total, rating)
  
- table_relationships.png - Diagram showing the relationships between tables


## Environment Setup and Installation

To run the analysis locally, follow these steps:

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. **Set up a virtual environment (recommended):**

```
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows
```

3. **Install required Python libraries:**

```
pip install pandas numpy matplotlib seaborn jupyter sqlalchemy prettytable graphviz

```


4. **Database Setup:**

- Ensure PostgreSQL is installed and running.
- Create a database named monday_coffee_db.
- Run the SQL commands in schemas.sql to create the tables.
- Load the CSV data into the corresponding tables (this was done via the system terminal using the COPY command).


5. **Start the Jupyter Notebook:**
   
```
jupyter notebook
```

6. **Open and run the notebook:**
   
Open ```Monday Coffee Co. India Expansion Analysis.ipynb``` and run the cells sequentially to perform the analysis.

# Analysis Overview

The notebook covers several stages of analysis:

1. Database Connection & Table Creation:
- The notebook connects to the PostgreSQL database using %sql magic and SQLAlchemy.
- It creates four tables: city, customers, products, and sales.
- CSV files are loaded into these tables.

3. Data Overview:
- Sample queries display data from each table to ensure correct data loading.
- A Graphviz diagram visualizes the relationships between tables.

4. Key Analytical Sections:
- Coffee Consumers Count:
  - Estimates the number of coffee consumers per city (25% of population) and visualizes the data.
    
- Total Revenue Analysis:
  - Calculates total revenue in Q4 2023 per city, visualizing both overall revenue and city-level comparisons.
    
- Product Sales Count:
  - Counts the number of orders per product and shows a donut chart for the top 5 products.
    
- Average Sales per City:
  - Computes the average sale per customer in each city with a corresponding bar chart.
    
- City Population vs. Coffee Consumers:
  - Compares the population-based estimate of coffee consumers with the actual number of unique customers per city.
    
- Top Selling Products by City:
  - Determines the top 3 selling products in each city and visualizes the frequency with a count plot.
    
- Customer Segmentation:
  - Identifies the number of unique customers per city, helping to segment the market.
    
- Average Sale vs. Rent:
  - Analyzes the relationship between average sales and average rent per customer in each city using a scatter plot.
    
- Monthly Sales Growth:
  - Calculates and visualizes the month-over-month sales growth percentage for each city.
    
- Market Potential Analysis:
  - Combines various metrics to rank cities by market potential. Key metrics include total sales, total rent, total customers, and estimated coffee consumers.

## Key Insights and Recommendations

- Major Cities:
Cities like Pune, Chennai, and Bangalore show high total revenue and strong customer spending, making them prime candidates for expansion.

- Consumer Behavior:
The analysis reveals seasonal trends (e.g., increased sales during September–November) and differences in average sales per customer across cities.

- Product Trends:
Certain products (e.g., Cold Brew Coffee Pack, Ground Espresso Coffee) dominate sales, suggesting a focus on promoting these items.

- Market Segmentation:
The data supports tailored strategies such as loyalty programs in high-customer cities and localized marketing in smaller cities.

### Recommendations:

- Invest in High-Potential Markets:
Focus on cities with high revenue and customer spending (e.g., Pune).

- Optimize Operations:
Consider strategies to manage high operational costs in cities like Mumbai.

- Tailor Marketing Efforts:
Use seasonal trends to plan promotions and introduce loyalty programs in cities with a strong consumer base.

## Conclusion

This comprehensive analysis offers data-driven insights into the expansion potential for Monday Coffee Co. in India. By evaluating sales performance, customer behavior, and market indicators, the project provides actionable recommendations to support strategic decisions for new coffee shop locations.

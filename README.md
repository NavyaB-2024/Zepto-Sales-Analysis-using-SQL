 Zepto SQL Data Analysis Project

Project Overview:
This project is based on a sample dataset inspired by Zepto (online grocery delivery app).  
The goal was to perform  “data exploration, cleaning, and analysis”  using SQL to understand product pricing, discounts, inventory, and revenue estimation.  

Tech Stack:
- SQL (PostgreSQL / MySQL compatible)
  
Dataset Overview:
The dataset is inspired by Zepto’s online grocery platform and mimics a real-world e-commerce inventory system.
It contains product-level details such as pricing, discounts, stock availability, and weights.
Each row represents a unique SKU (Stock Keeping Unit) for a product. Duplicate product names may appear because the same product can exist in different package sizes, weights, or discounts — similar to actual catalog data.
Columns:
1.	sku_id → Unique identifier for each product (Primary Key)
2.	name → Product name as it appears in the app
3.	category → Product category (e.g., Fruits, Snacks, Beverages)
4.	mrp → Maximum Retail Price (originally in paise, later converted to ₹)
5.	discountPercent → Discount applied on MRP (%)
6.	discountedSellingPrice → Final price after discount (₹)
7.	availableQuantity → Units available in inventory
8.	weightInGms → Product weight in grams
9.	outOfStock → Boolean flag (TRUE = product unavailable)
10.	quantity → Quantity purchased/ordered

Project Workflow:
1. Data Exploration
- Counted total rows in the dataset.
- Checked for `NULL` values across columns.
- Identified unique product categories.
- Analyzed products in stock vs. out of stock.
- Found duplicate product names (multiple SKUs).

2. Data Cleaning
- Detected products with `mrp = 0` or `discountedSellingPrice = 0` and removed them.
- Converted values from **paise to rupees**.
- Verified updated pricing.

3. Data Analysis (Key Business Questions)
1. Top 10 best-value products based on discount percentage.  
2. Products with high MRP but out of stock(premium items unavailable).  
3. Estimated revenue per category based on available stock.  
4. Products with MRP > ₹500 but discount < 10%(low-discount luxury items).  
5. Top 5 categories with highest average discount percentage.  
6. Price per gram for products above 100g (value-for-money check).  
7. Categorized products into Low, Medium, Bulk   based on weight.  
8. Total inventory weight per category(supply chain planning).  

Insights:
- Some high-MRP products were out of stock, showing demand-supply gaps.  
- Certain categories had very high average discounts, indicating promotional strategies.  
- Price per gram analysis helped in identifying the best value products.  
- Bulk items contributed heavily to total inventory weight.  

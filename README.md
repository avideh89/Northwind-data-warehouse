# Northwind-data-warehouse
Data Warehouse project for Northwind dataset, including star schema modeling, ETL, and SQL queries for analytics.
This project is a Data Warehouse implementation for the Northwind database.
It includes:
- Star Schema modeling
- ETL process design
- SQL queries for analytics

# Northwind Operational Database - Overview

![Northwind EDR](https://github.com/avideh89/Northwind-data-warehouse/blob/main/2_Northwind%20operational%20diagram.png?raw=true)


The Northwind Operational Database is a transactional (OLTP) database designed to manage the daily operations of a wholesale business. It includes key entities such as Orders, Customers, Products, Suppliers, Employees, and Shippers.

Key Features:

	•	Orders and Order Details: Tracks sales transactions, linking products to customer orders.
	•	Products and Categories: Organizes items into specific product categories.
	•	Customers and Suppliers: Stores business partners’ details, including buyers and vendors.
	•	Employees and Territories: Manages employee assignments and geographic regions.
	•	Shippers: Identifies third-party logistics providers used for order deliveries.

This normalized relational model ensures data consistency and efficiency in handling real-time business transactions. 🚀

# Northwind Data Warehouse - Star Schema

Why Star Schema?<br>
	✅ Simplifies Queries: Reduces complex joins by centralizing transactional data into a single Fact Table.<br>
	✅ Improves Performance: Queries run faster compared to a normalized OLTP model.<br>
	✅ Optimized for BI Tools: Enables better reporting in Power BI, Tableau, and SQL-based analytics.<br>

## Northwind Data Warehouse - Star Schema Overview

## Star Schema Structure
	✔️Fact Table:
		• FactOrders → The central fact table that stores sales transactions, 
  		  including order details, revenue, and related keys for dimensions.
	 
	✔️Dimension Tables:
		• DimCustomer → Contains customer information.
		• DimProduct → Stores product details and links to product categories.
		• DimGeography → Includes country, region, and territory details.
		• DimSupplier → Stores supplier-related data.
		• DimEmployee → Holds employee details and their roles in the sales process.
		• DimDate → Provides a structured date dimension for time-based analysis.


## Decision: 
Removal of ShipName and Shippers
Initially, ShipName was considered as a separate dimension due to its presence in Orders. 
However, after evaluating its impact:

	• High cardinality made it inefficient for analytical queries.
	• It did not significantly contribute to sales performance analysis.
	• It was merged with DimShippers but later removed entirely from the schema.

📌 If needed, shipping data can be added later in a separate table.





















































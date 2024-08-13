# DATA-DEFINITION-LANGUAGE-PROJECT
This project involves creating a robust database schema for an e-commerce system, designed to handle and manage essential business processes. The schema consists of three key tables: Customer, Product, and Orders. Each table is meticulously crafted to ensure data integrity and efficient query performance.

Table Definitions
Customer Table

Purpose: To store detailed information about customers who interact with the e-commerce system.
Key Columns:
CustomerID (Primary Key): Unique identifier for each customer.
FirstName: Customer's first name.
LastName: Customer's last name.
Email: Customer's email address (unique).
PhoneNumber: Customer's contact number.
Address: Customer's physical address.
DateOfBirth: Customer's date of birth.
Constraints:
Email should be unique.
PhoneNumber should be in a valid format.
Product Table

Purpose: To catalog all products available for purchase in the e-commerce system.
Key Columns:
ProductID (Primary Key): Unique identifier for each product.
ProductName: Name of the product.
Description: Brief description of the product.
Price: Price of the product.
StockQuantity: Number of units available in stock.
Constraints:
Price must be a positive value.
StockQuantity must be a non-negative integer.
Orders Table

Purpose: To record transactions made by customers, linking them with purchased products.
Key Columns:
OrderID (Primary Key): Unique identifier for each order.
CustomerID (Foreign Key): References the CustomerID in the Customer table.
ProductID (Foreign Key): References the ProductID in the Product table.
OrderDate: Date and time when the order was placed.
Quantity: Number of units ordered.
TotalAmount: Total cost for the order (computed as Price * Quantity).
Constraints:
CustomerID must refer to a valid Customer.
ProductID must refer to a valid Product.
Quantity must be a positive integer.
Relationships
Customer to Orders: One-to-Many. A single customer can place multiple orders, but each order is associated with only one customer.
Product to Orders: One-to-Many. A single product can appear in multiple orders, but each order refers to only one product.
Benefits
This schema supports fundamental e-commerce operations, including managing customer details, cataloging products, and recording orders. The well-defined relationships between tables ensure data integrity and facilitate complex queries, such as retrieving a customer's order history or checking product availability.

By implementing this schema, you'll have a solid foundation for building a comprehensive e-commerce application that can efficiently handle and analyze customer and product data.

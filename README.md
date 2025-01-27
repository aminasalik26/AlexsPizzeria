# AlexsPizzeria

# **Pizzeria Excel, SQL Database and Dashboard Project**

## **Project Overview**

This project demonstrates the end-to-end process of crating a spreadsheet, designing and building a SQL database for a Alex's pizzeria business, writing custom SQL queries, and integrating the database with a BI tool to create interactive dashboards for reporting and analysis.

The database tracks key business data such as customer orders, inventory stock levels, and staff information. Custom SQL queries are used to extract valuable insights, while **Google Data Studio** visualiaes this data to help optimise business performance.

## **Key Features**

- **Database Design**: A relational database schema is designed to store and manage orders, customers, inventory, staff, and menu items.
- **Data Normalisation**: Redundant data is eliminated by normalizing the data model, creating separate tables for customers, addresses, and menu items.
- **SQL Queries & Views**: Custom SQL queries and views are created for reporting key metrics like total orders, total sales, top-selling items, and more.
- **Advanced Calculations**: Calculations such as ingredient costs, stock levels, and sales trends are derived from queries.
- **Dashboard Creation**: Data from the SQL database is connected to **Google Data Studio** to build interactive dashboards visualising business performance.

## **Technologies Used**

- **SQL (MySQL)**: For creating and managing the database, writing complex queries, and building views.
- **Quick DBD**: For designing the relational database schema.
- **Navicat for MySQL**: For managing MySQL databases and query execution.
- **Google Data Studio**: For connecting the SQL database and building interactive dashboards.

## **Database Schema**

The database schema consists of the following main tables:

1. **Customers**: Stores customer information (ID, name, contact details).
2. **Addresses**: Stores address information (ID, street, city, postal code).
3. **Menu Items**: Details about the pizzeria’s menu items (ID, name, category, size, price).
4. **Orders**: Stores customer orders (ID, customer ID, order details, delivery address, total price).
5. **Order Items**: Connects menu items to orders (order item ID, order ID, item ID, quantity).
6. **Staff**: Staff information (ID, name, role, hours worked).
7. **Inventory**: Tracks ingredient stock levels (ingredient ID, name, quantity, cost).

## **Installation Instructions**

To run the database locally and interact with the dashboards, follow these steps:

1. **Clone this repository**:
    ```bash
    git clone https://github.com/yourusername/pizzeria-sql-dashboard.git
    cd pizzeria-sql-dashboard
    ```

2. **Set up the database**:
   - Create a new **MySQL** database and import the SQL schema from the `schema.sql` file.
   - Populate the database with sample data (optional: check `sample_data.sql`).

3. **Connect to the database** using **Navicat** or your preferred MySQL client.

4. **Connect the database to Google Data Studio**:
   - Use the [MySQL connector](https://datastudio.google.com/) in **Google Data Studio** to connect to the local database.

5. **Build and explore the dashboard**:
   - Open the `dashboard.pbd` file in **Google Data Studio** to interact with the visualized data.

## **Usage**

After setting up the database and Google Data Studio connection, you can use the dashboard to explore the following insights:

- **Total Sales**: See how much revenue has been generated.
- **Top-Selling Items**: Identify the most popular menu items.
- **Orders by Time**: Visualize orders by hour and identify peak order times.
- **Stock Levels**: Monitor remaining stock and ingredient levels.

### **Example Queries**

Some useful SQL queries:

- **Total Orders**:
  ```sql
  SELECT COUNT(*) AS total_orders FROM orders;

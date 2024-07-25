![image](https://github.com/user-attachments/assets/bbf42628-097b-445a-a5f9-8db5ac2015c3)
![image](https://github.com/user-attachments/assets/3645ab14-a0c9-4e75-afb8-1db39adbc944)

# Data Modelling
Data modeling is the process of creating a data model to visually represent the data structures and their relationships within a database. It serves as a blueprint for designing and understanding the database.

### Dimension Table
- **Purpose**: Stores descriptive information to provide context for facts.
- **Content**: Contains attributes that describe dimensions, such as "Product Name," "Category," "Date," "Location."
- **Characteristics**: 
  - Often contains textual information.
  - Typically non-volatile and changes infrequently.
  - Contains primary keys that uniquely identify each record.

### Fact Table
- **Purpose**: Stores quantitative data for analysis and measurement.
- **Content**: Contains facts or measures such as "Sales Amount," "Quantity Sold," "Revenue."
- **Characteristics**:
  - Contains foreign keys linking to dimension tables.
  - Usually contains numeric data.
  - Can grow large as it accumulates transactional or event data over time.

### Example
Consider a retail business:

**Dimension Table**: 
- `Product Dimension`:
  - ProductID (Primary Key)
  - ProductName
  - Category
  - Brand

**Fact Table**:
- `Sales Fact`:
  - SaleID (Primary Key)
  - DateKey (Foreign Key to Date Dimension)
  - ProductID (Foreign Key to Product Dimension)
  - StoreID (Foreign Key to Store Dimension)
  - SalesAmount
  - QuantitySold

In this model, the `Sales Fact` table records each sales transaction, linking to the `Product`, `Date`, and `Store` dimensions to provide context for each sale.



![image](https://github.com/user-attachments/assets/7c7bf749-7de4-45cf-ac6d-76fcd2ffe830)



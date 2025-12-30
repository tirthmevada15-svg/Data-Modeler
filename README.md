# Data Modeler – Building a Normalized Star Schema Data Model (Power BI)

## Project Overview
This project demonstrates the complete **end-to-end data modeling process in Power BI**, focusing on designing a **normalized Star Schema** using real-world business datasets.  
The objective is to transform raw transactional data into an **optimized analytical model** that supports fast performance, clean reporting, and scalable business insights.

This project is suitable for:
- Data Analyst roles
- Power BI Developer roles
- Data Modeler / BI Architect evaluations
- Academic & portfolio submissions

## Project Objectives
- Build a **proper Star Schema data model**
- Separate **Fact and Dimension tables**
- Create **clean relationships with correct cardinality**
- Apply **best practices in Power BI modeling**
- Enable accurate and high-performance reporting

## Data Sources
The project uses **six datasets** hosted on Google Sheets and connected directly to Power BI via **Web Connector**.

### Datasets Used
1. **Sales_Fact**  
   - Transaction-level sales data  
   - Measures: Sales Amount, Quantity, Discount, Profit  

2. **Customer_Dim**  
   - Customer details  
   - Attributes: Customer Name, Segment, Gender, City  

3. **Product_Dim**  
   - Product master data  
   - Attributes: Product Name, Category, Sub-Category  

4. **Region_Dim**  
   - Geographic hierarchy  
   - Attributes: Country, State, City, Region  

5. **Date_Dim**  
   - Calendar table  
   - Attributes: Date, Year, Quarter, Month, Day  

6. **Sales_Person_Dim**  
   - Sales representative information  
   - Attributes: Salesperson Name, Team, Manager  

## Data Modeling Approach

### Star Schema Design
- **Sales_Fact** is the central fact table
- All dimension tables connect **one-to-many** to the fact table
- No relationships between dimension tables (pure star schema)

### Relationships
| From Table | To Table | Cardinality | Direction |
|----------|---------|------------|-----------|
| Customer_Dim | Sales_Fact | One → Many | Single |
| Product_Dim | Sales_Fact | One → Many | Single |
| Date_Dim | Sales_Fact | One → Many | Single |
| Region_Dim | Sales_Fact | One → Many | Single |
| Sales_Person_Dim | Sales_Fact | One → Many | Single |

Surrogate keys used where applicable  
Referential integrity maintained  
No many-to-many relationships  

---

## Data Cleaning & Transformation
Performed using **Power Query Editor**:

- Removed duplicates
- Standardized column names
- Corrected data types
- Handled missing/null values
- Created calculated columns where required
- Built a dedicated Date Dimension table

## Measures & Calculations (DAX)
Key measures created using DAX:

- `Total Sales`
- `Total Quantity`
- `Total Profit`
- `Average Order Value`
- `Profit Margin %`
- `Year-over-Year Sales`
- `Running Total`

All measures follow:
- Proper naming conventions
- Measure table organization
- Reusability best practices

## Reporting Capabilities
The data model supports dashboards such as:
- Sales Performance Overview
- Product Category Analysis
- Customer Segmentation
- Regional Sales Trends
- Time Intelligence (YoY, MoM)

## Performance Optimization
- Star schema minimizes filter propagation
- Single-direction relationships for efficiency
- Fact table kept narrow
- Dimensions optimized for slicing and dicing
- Reduced model complexity

## Tools & Technologies
- **Power BI Desktop**
- **Power Query (M Language)**
- **DAX**
- **Google Sheets (Web Connector)**

## Key Learnings
- Importance of proper data modeling
- Difference between flat models and star schema
- Performance impact of relationships
- Real-world BI best practices


## 📌 License
This project is for **educational and portfolio purposes**.

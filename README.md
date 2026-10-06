# Sample Superstore Sales Dashboard

## 📊 Project Overview

**Sample Superstore Sales Dashboard** is an interactive **Microsoft
Power BI** business intelligence project built to analyze retail sales
performance across customers, products, regions, categories, shipping
modes, and time.

The dashboard converts transactional Superstore sales data into a
compact management view with KPI cards and interactive slicers. Users
can filter the report by **Month, Year, Ship Mode, Customer Segment,
Region, and Product Category** to explore business performance from
different perspectives.

------------------------------------------------------------------------

## 🎯 Project Objectives

The main objectives of this project are to:

-   Monitor overall **Sales, Profit, Orders, Customers, and Products**.
-   Analyze sales performance across different **customer segments**.
-   Compare business performance by **region**.
-   Analyze performance across different **product categories**.
-   Understand the impact of different **shipping modes**.
-   Perform time-based analysis using **Month and Year** filters.
-   Provide an interactive Power BI dashboard for business reporting and
    decision-making.
-   Demonstrate practical knowledge of **Power BI data modeling, DAX
    measures, slicers, and dashboard design**.

------------------------------------------------------------------------

## 🛠️ Tools & Technologies

  -----------------------------------------------------------------------
  Tool / Technology                   Purpose
  ----------------------------------- -----------------------------------
  **Microsoft Power BI**              Dashboard development and
                                      visualization

  **Power Query**                     Data preparation and transformation

  **DAX**                             KPI and analytical measures

  **Power BI Data Model**             Relationships between fact and
                                      dimension tables

  **Power BI Visuals**                KPI cards, slicers and interactive
                                      analysis
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🗂️ Data Model

The report uses a dimensional model containing a central sales fact
table and supporting dimension tables.

### Fact Table

### `Fact sales`

The main transactional table contains sales-related information used for
business analysis, including:

-   Sales
-   Profit
-   Orders
-   Product information
-   Customer information
-   Shipping information
-   Date information

### Dimension Tables

### `Dim Customer`

Used for customer and customer-segment analysis.

Important analytical fields include:

-   Customer
-   Segment
-   Region

### `Dim Product`

Used for product and category analysis.

Important analytical fields include:

-   Product
-   Category

### `DIM CALENDAR`

Used for time-based analysis.

Important fields include:

-   Month
-   Year
-   Date-related information

### Model Structure

``` text
                  ┌─────────────────┐
                  │  Dim Customer   │
                  │ Segment         │
                  │ Region          │
                  └────────┬────────┘
                           │
                           │
┌─────────────────┐        │        ┌─────────────────┐
│   Dim Product   │────────┼────────│  DIM CALENDAR   │
│ Category        │        │        │ Month / Year    │
└─────────────────┘        │        └─────────────────┘
                           │
                    ┌──────▼──────┐
                    │  Fact sales │
                    │ Sales       │
                    │ Profit      │
                    │ Orders      │
                    └─────────────┘
```

> The diagram represents the logical analytical structure. The actual
> relationships are maintained inside the Power BI model.

------------------------------------------------------------------------

## 📑 Report Structure

The PBIX contains **one report page**, named:

### Page 1

The page is designed as an interactive Superstore performance dashboard.

The dashboard combines:

-   KPI cards
-   Time filters
-   Shipping filters
-   Customer segment filters
-   Regional filters
-   Product category filters

This creates a simple executive-style interface for exploring retail
performance.

------------------------------------------------------------------------

## 📌 Key Performance Indicators

The dashboard contains five primary KPI measures:

  -----------------------------------------------------------------------
  KPI                                 Description
  ----------------------------------- -----------------------------------
  **Total Sales**                     Overall sales generated from the
                                      available transactions

  **Total Products**                  Total number of products
                                      represented in the analysis

  **Total Orders**                    Total number of orders

  **Total Customers**                 Total customers represented in the
                                      dataset

  **Total Profit**                    Overall profit generated from sales
  -----------------------------------------------------------------------

These KPIs provide a quick snapshot of the business's overall
performance.

------------------------------------------------------------------------

## 🎛️ Interactive Slicers

The dashboard contains **six interactive slicers**.

### 1. Month

Allows users to filter the dashboard based on the selected month or
month range.

``` text
DIM CALENDAR → Month
```

### 2. Year

Allows year-based analysis.

``` text
DIM CALENDAR → Year
```

### 3. Ship Mode

Filters the report according to the selected shipping method.

``` text
Fact sales → Ship Mode
```

### 4. Customer Segment

Allows comparison between different customer segments.

``` text
Dim Customer → Segment
```

### 5. Region

Filters the dashboard by geographical region.

``` text
Dim Customer → Region
```

### 6. Product Category

Allows users to focus on specific product categories.

``` text
Dim Product → Category
```

------------------------------------------------------------------------

## 🧮 DAX Measures

The dashboard's KPI section uses measures from the **Fact sales** table.

The primary measures used by the report are:

``` text
Total Sales
Total Products
Total Orders
Total Customers
Total Profit
```

These measures are displayed together in the dashboard's KPI/card
visual.

### Example DAX Concepts

The project demonstrates the use of DAX measures for aggregating
business data.

Typical patterns include:

``` dax
Total Sales = SUM('Fact sales'[Sales])
```

``` dax
Total Profit = SUM('Fact sales'[Profit])
```

For unique entity counts, a typical DAX approach is:

``` dax
Total Customers = DISTINCTCOUNT('Dim Customer'[Customer ID])
```

``` dax
Total Products = DISTINCTCOUNT('Dim Product'[Product ID])
```

> The exact implementation of measures should be verified inside the
> PBIX's Model/Data view if the measure definitions need to be modified.

------------------------------------------------------------------------

## 🔍 Business Questions Answered

The dashboard can be used to answer questions such as:

1.  What is the total sales generated?
2.  What is the total profit?
3.  How many orders have been placed?
4.  How many customers are represented?
5.  How many products are represented?
6.  How does performance change across years?
7.  How does performance change across months?
8.  Which customer segment is contributing to the selected results?
9.  Which region performs best?
10. Which product category contributes most to sales and profit?
11. Which shipping mode is associated with the selected business
    performance?
12. How do the KPIs change when multiple filters are applied
    simultaneously?

------------------------------------------------------------------------

## 📊 Dashboard Interactivity

One of the main strengths of the report is its filter-driven analysis.

For example:

``` text
Year
  ↓
Month
  ↓
Region
  ↓
Customer Segment
  ↓
Product Category
  ↓
Ship Mode
  ↓
Updated KPIs
```

Selecting one or more slicer values dynamically filters the report's KPI
results.

This allows users to move from an overall business view to a more
specific segment of the dataset.

------------------------------------------------------------------------

## 🧠 Skills Demonstrated

This project demonstrates practical skills in:

-   Microsoft Power BI
-   Data visualization
-   Power BI dashboard design
-   Data modeling
-   Fact and dimension tables
-   DAX measures
-   KPI development
-   Interactive slicers
-   Customer analysis
-   Product analysis
-   Regional analysis
-   Shipping analysis
-   Time-based filtering
-   Business intelligence reporting
-   Data storytelling

------------------------------------------------------------------------

## 🚀 How to Open the Project

### Prerequisites

Install:

-   **Microsoft Power BI Desktop**
-   Windows operating system compatible with Power BI Desktop

### Steps

1.  Download the `.pbix` file.
2.  Open `Sample_superstore.pbix` in **Power BI Desktop**.
3.  Wait for the report to load.
4.  Open **Page 1**.
5.  Review the KPI cards.
6.  Use the Month, Year, Ship Mode, Segment, Region and Category
    slicers.
7.  Explore how the KPI values change based on the selected filters.
8.  Open the **Model** view to inspect the data model.
9.  Open the **Data** view to inspect the underlying tables and fields.
10. Review the DAX measures used by the report.

------------------------------------------------------------------------

## 📁 Project Structure

``` text
Sample-Superstore-PowerBI/
│
├── Sample_superstore.pbix
└── README.md
```

------------------------------------------------------------------------

## 💼 Practical Business Use Cases

This dashboard can be useful for:

-   Retail business analysis
-   Sales management
-   Profitability analysis
-   Customer segmentation
-   Product category analysis
-   Regional performance analysis
-   Shipping performance analysis
-   Executive reporting

Managers can use the dashboard to quickly understand how selected
business dimensions affect overall sales and profit.

------------------------------------------------------------------------

## 🔮 Future Enhancements

The dashboard can be extended with:

-   Sales and profit trend line charts.
-   Regional maps.
-   Top 10 customers by sales.
-   Top 10 products by profit.
-   Category-level profit margin.
-   Sales growth percentage.
-   Year-over-year comparison.
-   Month-over-month comparison.
-   Average order value.
-   Average profit per order.
-   Profit margin %.
-   Discount analysis.
-   Shipping cost analysis.
-   Customer lifetime value.
-   Product-level drill-through pages.
-   Regional drill-through pages.
-   Power BI Service publishing and scheduled refresh.

------------------------------------------------------------------------

## ⭐ Project Summary

The **Sample Superstore Sales Dashboard** is a Power BI business
intelligence project that transforms retail transaction data into an
interactive KPI-driven report.

It combines a dimensional data model with DAX measures and interactive
slicers to provide a flexible way to analyze **sales, profit, orders,
customers, and products** across **time, region, customer segment,
product category, and shipping mode**.

The project is suitable for demonstrating practical **Power BI, DAX,
data modeling, dashboard development, and business analytics skills** in
a portfolio, academic project, or job interview.

------------------------------------------------------------------------

## 👨‍💻 Author

**Yeshwanth**

**Power BI \| Data Analytics \| DAX \| Business Intelligence**

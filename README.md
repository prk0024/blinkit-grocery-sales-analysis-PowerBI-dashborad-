# blinkit-grocery-sales-analysis-PowerBI-dashborad-
Interactive Power BI dashboard analyzing BlinkIT grocery sales, product performance, customer ratings, and outlet trends using Power Query, DAX, and data visualization.
## Project Overview

The goal of this project was to turn raw grocery sales data into a clear
business-performance dashboard. The analysis explores how sales vary by
product category, fat content, outlet type, outlet size, outlet
location, and outlet establishment year.

The dashboard helps stakeholders monitor key performance indicators
(KPIs), compare outlet performance, identify leading product categories,
and explore opportunities for better product and inventory planning.

## Business Objectives

-   Measure overall sales performance using key KPIs.
-   Compare sales of Low Fat and Regular products.
-   Identify the item categories contributing most to sales.
-   Compare outlet performance by outlet type, size, location, and
    establishment year.
-   Review average customer ratings alongside sales performance.

## Dataset

The source Excel dataset contains **8,523 records and 12 columns**. It
includes product-level and outlet-level attributes such as:

  Field                       Description
  --------------------------- ---------------------------------
  Item Identifier             Product identifier
  Item Type                   Grocery product category
  Item Fat Content            Fat-content classification
  Item Weight                 Product weight
  Item Visibility             Product visibility measure
  Item MRP                    Maximum retail price
  Outlet Identifier           Outlet identifier
  Outlet Establishment Year   Year the outlet was established
  Outlet Size                 Outlet size classification
  Outlet Location Type        Tier 1, Tier 2, or Tier 3
  Outlet Type                 Outlet format
  Sales                       Sales value
  Rating                      Customer rating

## Tools and Technologies

-   **Microsoft Power BI** --- report and dashboard development
-   **Power Query** --- data cleaning and transformation
-   **DAX** --- KPI and measure calculations
-   **Microsoft Excel** --- source dataset

## Data Preparation

The dataset was imported from Excel into Power BI and prepared in Power
Query. Preparation included:

-   Reviewing column data types and data quality.
-   Standardizing inconsistent values in `Item Fat Content` (for
    example, `LF`, `low fat`, and `Low Fat` into `Low Fat`; and `reg`
    and `Regular` into `Regular`).
-   Reviewing missing values in `Item Weight`.
-   Checking for duplicate records and preparing fields for analysis.

## Key KPIs

The dashboard tracks four core measures:

  KPI                   Meaning
  --------------------- -------------------------------------------
  **Total Sales**       Total sales value across all item records
  **Average Sales**     Average sales value per item record
  **Number of Items**   Count of item records in the dataset
  **Average Rating**    Average customer rating

Example DAX measures (adjust the table name if it differs in your PBIX
file):

``` dax
Total Sales = SUM('BlinkIT Grocery Data'[Sales])

Average Sales = AVERAGE('BlinkIT Grocery Data'[Sales])

Number of Items = COUNTROWS('BlinkIT Grocery Data')

Average Rating = AVERAGE('BlinkIT Grocery Data'[Rating])
```

> **Metric definition:** `Number of Items` above counts rows/item
> records. It is not the count of distinct `Item Identifier` values.

## Dashboard Visualizations

The report addresses the following business requirements:

  -----------------------------------------------------------------------
  Analysis                Visualization           Purpose
  ----------------------- ----------------------- -----------------------
  Total Sales by Fat      Donut chart             Compare sales
  Content                                         contribution from Low
                                                  Fat and Regular
                                                  products

  Total Sales by Item     Bar chart               Identify leading
  Type                                            product categories

  Fat Content by Outlet   Stacked column chart    Compare fat-content
  for Total Sales                                 sales across outlets

  Total Sales by Outlet   Line chart              Examine sales by outlet
  Establishment Year                              establishment cohort

  Sales by Outlet Size    Donut/Pie chart         Compare sales
                                                  contribution by outlet
                                                  size

  Sales by Outlet         Map                     Explore the geographic
  Location                                        distribution of sales

  All KPIs by Outlet Type Matrix                  Compare core metrics
                                                  across outlet types
  -----------------------------------------------------------------------

## Key Findings

The analysis indicates the following patterns in the dataset:

-   Total sales are approximately **\$1.20 million**.
-   Average sales are approximately **\$141 per item record**.
-   Average customer rating is approximately **3.97**.
-   Low Fat products contribute more sales than Regular products.
-   Fruits & Vegetables and Snack Foods are among the leading item
    categories by sales.
-   Supermarket Type1 has the highest total sales among outlet types.
-   Tier 3 outlets contribute the highest sales among the location
    tiers.
-   Medium-sized outlets contribute the highest sales among the
    outlet-size groups.

These findings describe patterns in the supplied dataset; they do not,
by themselves, establish the reasons behind those patterns.

## Potential Business Applications

1.  **Product assortment:** Review category-level sales to inform
    product availability and assortment decisions.
2.  **Outlet benchmarking:** Compare outlet formats and sizes to
    identify high- and low-performing groups.
3.  **Location strategy:** Investigate why sales differ across location
    tiers before making expansion decisions.
4.  **Inventory planning:** Use category and outlet sales patterns as
    inputs to replenishment planning.
5.  **Performance monitoring:** Track sales and customer ratings
    together to identify areas that may need further investigation.

## Repository Structure

``` text
BlinkIT-Grocery-Sales-Analysis/
├── Dataset/
│   └── BlinkIT Grocery Data.xlsx
├── Dashboard/
│   └── BlinkIT Analysis.pbix
├── Screenshots/
│   └── Dashboard Preview.png
└── README.md
```

Update the file and folder names above to match the files included in
this repository.

## Skills Demonstrated

-   Power BI dashboard development
-   Power Query data cleaning and transformation
-   DAX measures and KPI development
-   Data visualization and reporting
-   Exploratory sales analysis
-   Translating business requirements into analytical views
-   Communicating data-driven business insights

## Author

**Pratyush Ranjan Kumar**\
B.Tech, Mechanical Engineering (Automotive Engineering)\
Delhi Technological University (DTU)

**Interests:** Data Analytics \| Business Intelligence \| Consulting

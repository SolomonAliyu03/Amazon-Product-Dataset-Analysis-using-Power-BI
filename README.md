[Count of product_id by category_level_1.csv](https://github.com/user-attachments/files/21090112/Count.of.product_id.by.category_level_1.csv)# Amazon-Product-Dataset-Analysis-using-Power-BI

## Project Overview

This project demonstrates how to use Power BI to analyze an Amazon product dataset containing information about product categories, pricing, discounts, ratings, and customer reviews. 

## Project Objectives and Key features:

The goal is to showcase data transformation, modeling, and visualization skills using Power Query and DAX.

- Data cleaning and transformation in Power Query

- Category breakdown using split column by Delimiter

- DAX measures for KPIs like average rating, price, and discount

- Visuals: KPI Cards, Pie Charts, Bar Charts

## Dataset

- File: Amazon case study.xlsx
- Columns; product_id, product_name, category discounted_price, actual_price, discount_percentage, rating, rating_count, about_product, user_id, user_name, review_id, review_title, review_content, img_link, product_link

##  Data Cleaning (Power Query)

- Loaded the amazon case study file into the power query, then click on transform data ;

- Split Category column by delimiter | into multiple category levels;
    - Category_Level_1, Category_Level_2, Category_Level_3, Category_Level_4
 
- Changed data types for:

     - discounted_price, actual_price →  Fixed Decimal Number
     - discount_percentage, rating → Decimal Number
     - rating_count → Whole Number

- Removed unnecessary columns; about_product, user_id, user_name, review_id, review_title, review_content, img_link, product_link

- Replaced error column with null

##  DAX Measures Used:

- Total Products = DISTINCTCOUNT('amazon'[product_id])

- Average Rating = AVERAGE('amazon'[rating])

- Total Reviews = SUM('amazon'[rating_count])

- Total Rating = SUM('amazon'[rating])

- Average Price = AVERAGE('amazon'[discounted_price])

- Average Discount (%) = AVERAGE('amazon'[discount_percentage]) * 100

- Total Rating = SUM('amazon'[rating])

#### Step-by-Step: Calculating Total Products Using DAX

    - Open your Power BI file (.pbix)

    - In the Fields pane, select your dataset (e.g. amazon)

    - Click on the Modeling tab from the top ribbon

    - Click New Measure

    - In the formula bar that appears, type: Total Products = DISTINCTCOUNT('amazon'[product_id])

    - Press Enter

    - Go to your report view and insert a Card visual

    - Drag the new measure Total Products into the Card visual

    ✅ You now have a KPI card that shows the total number of distinct products in the dataset!


## 📊 Visualizations

#### KPI CARDS:
![Screenshot 2025-07-06 184413](https://github.com/user-attachments/assets/6beef743-e7ac-428b-869d-5e295e6712df)

#### Bar Chart:
- Top-rated products by rating count

![Screenshot 2025-07-06 193146](https://github.com/user-attachments/assets/61594f23-3d32-46dd-b5e6-88253128b78c)

#### Pie Chart:

- Product distribution by Category_Level_1

[Uploading Ccategory_level_1,Count of product_id
Electronics,526
Computers&Accessories,453
Home&Kitchen,448
OfficeProducts,31
HomeImprovement,2
MusicalInstruments,2
Car&Motorbike,1
Health&PersonalCare,1
Toys&Games,1
ount of product_id by category_level_1.csv…]()

![Screenshot 2025-07-06 200840](https://github.com/user-attachments/assets/b48a5152-b9ab-46de-b549-bb1db4e54ad7)


## Tools Used:

- Power BI Desktop

- Power Query Editor

- DAX (Data Analysis Expressions)


 ## File Structure

 amazon-product-analysis-powerbi/
├── README.md
├── dax-measures.md
├── data-cleaning-steps.md
├── Amazon case study.xlsx
├── PowerBI_Report.pbix
├── screenshots/
    ├── dashboard-overview.png
    ├── kpi-cards.png
    └── price-vs-rating.png


## Author
SOLOMON BABATUNDE ALIYU











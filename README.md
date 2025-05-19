# BTQ-Retail-Store-Analysis
This project analyses five years of BTQ Retail Store data to uncover insights into sales, customer behaviour, returns, and inventory performance. It addresses key business challenges like profitability, overstocking, and retention, and offers actionable strategies for data-driven decision-making.


![BTQ Retail Store](path/to/your-image.jpg)

## Table of Contents

1. [Project Overview](#1-project-overview)  
2. [Business Problems Identified](#2-business-problems-identified)  
3. [Dataset Overview](#3-dataset-overview)  
4. [Data Preparation & Cleaning Process](#4-data-preparation--cleaning-process)  
5. [Power BI Data Preparation](#5-power-bi-data-preparation)  
6. [Calculated Columns and Measures](#6-calculated-columns-and-measures)  
7. [Analytical Strategy](#7-analytical-strategy)  
8. [Final Review and Filtering](#8-final-review-and-filtering)  
9. [Key Strategic Insights & Recommendations](#9-key-strategic-insights--recommendations)  
10. [Customer Profile Dashboard with Interactive Search](#10-customer-profile-dashboard-with-interactive-search)  
11. [Conclusion](#11-conclusion)  

---

## 1. Project Overview

This project involves developing a comprehensive Retail Sales Dashboard using Power BI, based on a relational dataset spanning five years (2019–2024). The dashboard aims to uncover insights into customer purchasing behaviour, product performance, transaction trends, and return patterns. It is designed to address specific business challenges and support informed decision-making across operations, inventory, and customer engagement.

## 2. Business Problems Identified

- **Lack of Data Visibility**: Inability to track and analyse customer behaviour has led to missed sales and ineffective engagement strategies.  
- **Inefficient Inventory Management**: Lack of real-time insights into product demand causes overstocking and understocking.  
- **High Return Rates**: The business lacks a clear understanding of return reasons and patterns.  
- **Unstructured Sales Data**: Data inconsistencies and lack of completeness hinder meaningful analysis.  

## 3. Dataset Overview

The dataset comprises four interconnected tables:

- **Customers Table**: Contains Customer ID, Name, Email, Address, and Registration Date.  
- **Products Table**: Contains Product ID, Product Name, Category, Brand, Price, Supplier Info, and Stock Quantity.  
- **Transactions Table**: Contains Transaction ID, Customer ID, Product ID, Quantity Purchased, Total Price, Transaction Date, Payment Method, and Region.  
- **Returns Table**: Contains Return ID, Transaction ID, Product ID, Return Date, Return Reason, and Refund Status.  

## 4. Data Preparation & Cleaning Process

To ensure quality and consistency of insights:

- **Removed Duplicates**: Verified and confirmed no duplicate entries across datasets.  
- **Handled Missing Values**: Datasets were complete with no missing or null values.  
- **Standardized Date Formats**: All date columns were formatted as Date Time types.  
- **Filtered Date Ranges**: Since data for 2025 only covers Q1, it was excluded to ensure balanced year-over-year analysis. Analysis focuses on 2019–2024.  

## 5. Power BI Data Preparation

**Steps Taken**:

- **Loaded Datasets**: Imported all four sheets (Customers, Products, Transactions, Returns) into Power BI.  
- **Defined Data Types**:  
  - Dates → Transaction Date, Registration Date, Return Date  
  - Numbers → Quantity, Price, Stock, Total Price  
- **Created Relationships**  

## 6. Calculated Columns and Measures

**Excel Preprocessing**:

- Identified inconsistency in Total Price calculation. Used XLOOKUP to match product price from the Products table, multiplied by quantity, and computed:  
  - `Cost Price = Product Price × Quantity`  
  - `Profit = Total Price − Cost Price`  

**Power BI Measures Created**:

- Gross Profit, Total Revenue, Total Cost  
- Return Price column in the Returns table using related values from the Transactions table  
- Loss/Profit Flag for classifying transactions  
- Return Cost, Approved Refund Cost, and customer-based profitability metrics  

## 7. Analytical Strategy

Each dashboard component was designed to answer a key business question and resolve a specific operational pain point.  
Key Dashboard Created:

## 8. Final Review and Filtering

- Filtered out 2025 data to maintain consistent full-year comparisons.  
- Insights reflect only data from 2019–2024.  
- All visuals are interactive, allowing stakeholders to drill down by region, product, or time.  

## 9. Key Strategic Insights & Recommendations

### 💰 Profitability vs. Performance

- **Revenue**: $35.72M  
- **Total Cost Incurred**: $42.83M  
- **Net Loss**: $7.11M  
- **Profit Margin**: -20%  

**Insight**:  
Despite strong sales volume, BTQ Retail Store operates at a significant loss. All product categories are currently unprofitable, with Electronics generating the highest revenue ($5.76M) yet contributing the largest category-level loss of $1.11M.

**Recommendation**:  
Review pricing strategies and operational costs per category. Optimize logistics and renegotiate vendor contracts, particularly in high-volume, low-margin categories.

### 🛒 Stock Management & Overstocking

- **Total Stock Available**: 209,971 units  
- **Units Sold**: 42,615  
- **Total Transactions**: 14,291  

**Insight**:  
BTQ is currently overstocked. With only 18% of inventory sold, inventory turnover is too slow. Products are sitting idle, tying up capital, increasing storage costs, and risking obsolescence or damage (especially in Electronics, which also sees the highest returns).

**Recommendation**:  
Implement inventory optimization practices. Adopt just-in-time restocking and initiate clearance campaigns for stagnant items.

### 🌍 Regional Performance Discrepancies
In Gibraltar, the business generated $194K in revenue, achieved a profit of $47K, and incurred a cost of $147K. The region had 27 customers and 174 units sold. In Congo, revenue reached $376K, but the region reported a loss of $68K due to a cost of $444K, with 51 customers and 407 units sold. Korea recorded the second highest revenue, but also the highest loss at $120.3K, with a cost of $404K. It had 37 customers and 375 units sold.

**Insight**:  
Higher revenue does not equate to higher profitability. Gibraltar, despite being a smaller market, outperformed in cost efficiency. Korea and Congo generated high sales but suffered operational inefficiencies leading to deep losses.

**Recommendation**:  
Use Gibraltar as a case study for low-cost operations. Reassess investment in high-loss regions by improving cost control or downsizing presence.

### 📦 Product Lifecycle Efficiency
The Top 5 Products generated a total revenue of $6.63 million, with a profit margin of -11%, indicating a loss despite high sales volume. A total of 7,616 items were sold, and there were 508 returns, out of which 168 were approved. In comparison, the Bottom 5 Products brought in a total revenue of $3.45 million with a profit margin of -16%, reflecting an even greater loss. These products recorded 4,213 items sold, with 298 returns, of which 94 were approved.

**Insight**:  
Popular products drive volume but are not always profitable. Both high- and low-performing SKUs show negative profit margins and elevated return rates, indicating quality or value issues.

**Recommendation**:  
Perform detailed product audits. Improve quality assurance for top-selling SKUs and phase out consistently underperforming products.

### 🔁 Returns and Refunds Analysis
There was a total of 2,868 returns, accounting for 20% of all transactions, with a resulting return cost of $6.69 million. Out of these, 975 returns were approved for refunds, incurring a refund cost of $2.29 million. The top return reasons were: Late Delivery (619), Defective Product (583), Better Price Found (563), Wrong Product (557), and No Longer Needed (546).

**Insight**:  
Returns represent a major financial burden, costing over $6.69M, with only a portion approved. Late delivery is the top complaint and likely a contributing factor to product damage, which ranks second.

**Recommendation**:  
Improve delivery timelines and packaging quality. Use return reasons data to refine supply chain partnerships and quality assurance protocols.

### 📈 Customer Acquisition & Retention

- **Total Customers**: 4,743 (4,712 active | 269 inactive)
- **Trend**: Gradual growth until 2023, followed by a decline to 988 in 2024

**Insight**:  
Customer growth slowed in 2024, signalling possible retention issues or waning acquisition efforts. This decline could affect lifetime value and recurring sales.

**Recommendation**:  
To revamp customer retention strategies, the business should consider implementing loyalty and referral programs to reward repeat customers and encourage word-of-mouth growth. Additionally, enhancing the onboarding process and post-purchase support can improve customer satisfaction and reduce churn. Lastly, utilizing customer journey data enables targeted lifecycle marketing, allowing for personalized engagement at each stage of the customer relationship.

### 🧍‍♀️ High-Value Customer Contribution

The Top 5 Customers contributed a total revenue of $163.98K, with the top customer, Jonathan Smith, accounting for $42.6K. The highest number of purchases was made by Jennifer Scott, who bought 47 units. Altogether, the top 5 customers purchased 199 units, with only 2 returns recorded among them.

**Insight**:  
While the top 5 customers contribute to a small share of revenue, their engagement levels are high., showing strong potential for value-based segmentation. Their low return rate underscores customer satisfaction.

**Recommendation**:  
Build a VIP rewards program. Profile these customers’ behaviours and use predictive modelling to target similar profiles in campaigns.

### 💳 Payment Method Behaviour

**Insight**:  
Revenue is evenly distributed across payment channels, indicating broad customer preferences. No single method dominates, and all must be retained to avoid losing potential sales.

**Recommendation**:  
Support all major payment methods. Offer small discounts for low-fee options (e.g., bank transfers) to reduce transaction costs over time.

### 📦 Product Category Overview

The top-performing category was Electronics, which generated a total revenue of $5.76 million. Despite high sales, it incurred a loss of $1.11 million. A total of 6,829 units were sold, and there were 452 returns recorded for this category.

**Insight**:  
Even high-performing categories like Electronics are unprofitable. All categories report losses underscoring systemic cost challenges.

**Recommendation**:  
Drill down into category-level operational costs. Identify hidden costs (returns, logistics) and address SKU-level inefficiencies.

## 10. Customer Profile Dashboard with Interactive Search

To enhance actionable insights at the individual customer level, a dedicated dashboard segment was developed featuring cards that display key customer details such as Name, Email, and Address, alongside transactional metrics including the number of purchases, total revenue generated, units bought, and returns made. Users can effortlessly locate any customer using a text-based search filter, which dynamically updates the displayed data.

**Why It Matters**:  

This customer profile feature delivers instant, detailed insights at the individual level, enabling faster, data-driven decisions. It helps identify high-value and at-risk customers, supports personalized marketing and service efforts, and bridges data with customer relationship management all crucial for improving engagement, boosting sales, and reducing returns.
Ultimately, this interactive customer card system transforms the dashboard from a passive reporting tool into an active enabler of customer-centric decision-making, directly addressing the business problem of poor customer engagement and maximizing sales potential through data-driven personalization.


## 11. Conclusion

BTQ Retail is at a critical inflection point. While revenue performance is robust, inefficiencies in cost management, stock control, product quality, and customer satisfaction are cutting into profitability. The data tells a clear story the business is selling but earning little.
Now is the time to shift focus from volume-driven growth to efficiency-driven scaling. Optimize what works, remove what doesn’t, and centre decisions around data-backed customer value.
With strategic interventions particularly in cost control, inventory optimization, customer retention, and return reduction the business can move toward profitability.


**Prepared By**:  
Olowookere Abidemi  
Data Analyst,  
May 2025

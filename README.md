# Supermarket Sales Data Analysis

## 1. Data Overview

The dataset analysed in this project contains supermarket transaction records collected from a fictional retail chain operating across multiple branches and cities. The data provides detailed information about customer purchases, including customer type, product information, purchase quantity, and transaction value. This dataset is appropriate for analysing customer purchasing behaviour, product performance, and overall supermarket sales trends.

Before the cleaning process, the dataset consisted of **253 rows** and **8 columns**:

- `sale_id`
- `branch`
- `city`
- `customer_type`
- `product_name`
- `product_category`
- `quantity`
- `total_price`

The dataset includes both categorical variables and numerical variables, enabling descriptive statistical analysis and business-oriented data visualisation.

---

# 2. Data Cleaning

To improve data quality and ensure reliable analysis results, several preprocessing and cleaning procedures were conducted using **Power Query in Excel**.

## Handling Missing Values

A review of the dataset identified missing values in three variables:

- `customer_type` (**3 missing values**)
- `product_category` (**6 missing values**)
- `quantity` (**3 missing values**)

### Numerical Variable Treatment

For the `quantity` column, missing values were replaced using the **median value** of the dataset to minimise the impact of extreme values and maintain a balanced numerical distribution.

### Categorical Variable Treatment

For categorical variables, missing entries were filled using the **most frequently occurring category** within each column.

Specifically:

- Missing values in `customer_type` were replaced with **"Member"**
- Missing values in `product_category` were replaced with **"Fruits"**

This approach helped preserve transaction records and maintain consistency within the dataset.

---

## Removing Duplicate Records

The dataset also contained several duplicated transaction records.

Duplicate rows were identified and removed using the **"Remove Duplicates"** function in Power Query to avoid repeated transactions influencing the analysis results.

After removing duplicates, the dataset was reduced from **253 rows** to **250 unique transaction records**.

---

## Additional Cleaning Procedures

Additional preprocessing steps were also applied to improve dataset consistency and accuracy, including:

- correcting data types for text and numerical columns
- using **Trim** and **Clean** functions to remove extra spaces and hidden characters
- validating transaction values for inconsistencies
- creating a new calculated column named `unit_price` for pricing analysis

These cleaning procedures improved the reliability of the dataset and prepared the data for descriptive statistics, visualisation, and business insight analysis.

---

# 3. Descriptive Statistics

## Table 1. Descriptive Statistics of Supermarket Transaction Data

<img width="872" height="347" alt="Screenshot 2026-05-17 210036" src="https://github.com/user-attachments/assets/d7509747-ba24-454a-8de9-6ef05c91ee09" />

Table 1 summarises the key statistical characteristics of the supermarket transaction dataset.

- **Average transaction value:** `124.19`
- **Median transaction value:** `95.43`
- **Minimum transaction value:** `2.18`
- **Maximum transaction value:** `427.14`
- **Standard deviation:** `102.98`

The lower median compared to the mean indicates that customer spending is unevenly distributed across transactions.

In addition, the large standard deviation suggests considerable variation in customer purchasing behaviour and basket size.

---

# Insight 1 — Member Customers Generate Higher Business Value

## Figure 1. Revenue and Average Transaction Value by Customer Type

<img width="802" height="439" alt="Screenshot 2026-05-17 234723" src="https://github.com/user-attachments/assets/c1769cc8-272f-4caf-9013-ed4b8982ca3a" />


Figure 1 shows that **Member customers outperform Normal customers** in both total revenue and average transaction value.

### Key Findings

- Member customers generated approximately **$18,000** in total revenue
- Normal customers generated around **$13,000**
- Average transaction value for Members reached approximately **$134 per purchase**

### Business Implication

These findings indicate that loyalty members not only purchase more frequently but also spend more per transaction, making them a highly valuable customer segment for the supermarket.

From a business perspective, strengthening loyalty programs and personalised promotions could help improve customer retention and further increase long-term profitability.

---

# Insight 2 — Product Categories Influence Revenue and Pricing Performance Differently

## Figure 2. Revenue and Average Unit Price by Product Category

<img width="1038" height="489" alt="Screenshot 2026-05-17 234710" src="https://github.com/user-attachments/assets/5eda7be5-34ce-43e9-8464-2d3684327eaf" />

Figure 2 demonstrates that product categories contribute differently to supermarket performance.

### Key Findings

- **Fruits** generated the highest total revenue at approximately **$8,000**
- **Beverages** recorded the highest average unit price at around **$12.5 per item**

### Business Implication

This suggests that business performance is driven by both sales quantity and pricing value across product categories.

From a managerial perspective, the supermarket should:

- prioritise high-demand categories such as **Fruits** to maintain stable revenue
- leverage higher-priced categories like **Beverages** to improve profit margins and pricing strategy effectiveness

---

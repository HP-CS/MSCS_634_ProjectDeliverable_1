# MSCS_634_ProjectDeliverable_1

## 1. Dataset Summary
- **Dataset**: UCI Online Retail
- **Records**: 541,909 rows, **Attributes**: 8 (InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country)
- **Source**: UCI Machine Learning Repository
- **Reason for Selection**:
  - A transactional dataset with sufficient size and diversity
  - Enables various data mining techniques such as regression, classification, clustering, and association rule mining

## 2. Data Cleaning Summary
- **Missing Values**: Removed rows with missing CustomerID
- **Duplicates**: Dropped duplicate rows based on InvoiceNo and StockCode
- **Outliers**: Filtered out rows where Quantity <= 0 or UnitPrice <= 0
- **Reasoning**:
  - CustomerID is essential for segmentation
  - Clean data improves the quality of exploratory analysis and future models

## 3. EDA Insights
- **Quantity and UnitPrice Distributions**: Highly skewed; log scale visualization used to normalize
- **Country Analysis**: UK and Germany show the highest transaction volumes
- **Correlation Analysis**: Weak correlation between Quantity and UnitPrice
- **RFM Metrics**:
  - Recency, Frequency, Total Quantity, and Average Unit Price calculated for each customer
  - Insights suggest potential for customer segmentation and clustering

## 4. Challenges and Solutions
- **Large Dataset**: Managed memory constraints during data loading and visualization by using sampling
- **Time-Based Data**: Converted InvoiceDate for recency calculations
- **Outliers**: Detected extreme values in Quantity and UnitPrice, to be handled carefully during modeling

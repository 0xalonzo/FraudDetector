# Fraudify  
**Fraudify**: Simplifying fraud detection by visualizing and analyzing transaction patterns.

## Project Overview
Fraud detection is essential in the financial industry, where fraudulent transactions pose significant risks. **Fraudify** explores patterns and relationships between transaction data using various visualizations to identify trends and anomalies that can indicate fraudulent behavior.

This project analyzes transaction data through:
- **Correlation heatmaps**
- **Violin plots for amount distribution**
- **Pie charts for class imbalance visualization**
- **Time-series bar charts for hourly fraud activity**
- **Bar charts comparing fraud and non-fraud transactions across states**

##Visualizations Included
### 1. **Correlation Matrix**
- **What it shows:**  
  Linear relationships between numeric features (e.g., `amt`, `city_pop`, `merch_lat`, and `merch_long`).  
- **Purpose:**  
  Identifies redundant features to avoid multicollinearity, improving model performance.

### 2. **Violin Plot: Transaction Amounts by Fraud Status**  
- **What it shows:**  
  The **distribution** of transaction amounts for fraud (red) vs. non-fraud (green).  
- **Purpose:**  
  Higher transaction amounts are **more likely to be fraudulent**, providing insights into fraud trends.

### 3. **Pie Chart: Fraud vs. Non-Fraud Transactions**  
- **What it shows:**  
  The **proportion** of fraudulent and non-fraudulent transactions.  
- **Purpose:**  
  Highlights class imbalance, helping to plan for data balancing strategies in machine learning models.

### 4. **Bar Chart: Transactions by Hour of the Day**  
- **What it shows:**  
  The number of fraud and non-fraud transactions at each hour of the day.  
- **Purpose:**  
  Identifies **patterns in fraudulent activity**, which can be useful for scheduling security measures or monitoring.

### 5. **Bar Chart: Top 10 States with Fraud and Non-Fraud Transactions**  
- **What it shows:**  
  Fraud and non-fraud transaction counts for the **top 10 states** with the highest fraud activity.  
- **Purpose:**  
  Detects **geographic trends** and helps in focusing fraud prevention efforts on high-risk regions.

## Technologies Used
- **Python**: Data manipulation and analysis
- **Pandas**: For data wrangling and preprocessing
- **NumPy**: For numerical operations
- **Matplotlib**: For creating static visualizations
- **Seaborn**: For advanced statistical plots
- **Regular Expressions (`re`)**: To clean corrupted data

# Coffee Sales Dataset Analysis
## Project Overview
The Coffee Sales Dataset contains transactional information about coffee sales, including coffee types, sale times, payment methods, and monetary amounts. It is designed for data analysis, visualization, and predictive modeling to understand sales trends and customer preferences.

## Dataset Columns
- `hour_of_day`	: Indicates the hour (0–23) when the coffee transaction occurred. Useful for identifying peak sales hours.
- `cash_type` : Represents the mode of payment used by the customer (e.g., Cash, Card, Online).
- `money` : The total amount (in currency) spent by the customer during the transaction.
- `coffee_name` :	The name or type of coffee purchased (e.g., Latte, Cappuccino, Espresso).
- `Time_of_Day` :	The general time segment when the transaction occurred — typically categorized as Morning, Afternoon, or Evening.
- `Weekday` :	The name of the day on which the transaction occurred (e.g., Monday, Tuesday, etc.).
- `Month_name` :	The name of the month in which the sale was made (e.g., January, February, etc.).
- `Weekdaysort` :	A numerical representation of weekdays (Monday=1, Tuesday=2, ..., Sunday=7) used for sorting or time-series plotting.
- `Monthsort` :	A numerical representation of months (January=1, February=2, ..., December=12) used for sorting or trend analysis.
- `Date` :	The specific date when the transaction occurred, in YYYY-MM-DD format.
- `Time` : The exact time of the transaction (HH:MM:SS), providing finer granularity for sales analysis.

## Analysis and Processing Steps
1. Data Understanding and Cleaning
- Handle Missing Values: Identify and address missing or inconsistent entries in columns like money, coffee_name, or cash_type. Use imputation or removal techniques where necessary.
- Date & Time Conversion: Convert Date into a standard datetime format and Time into time objects. Create derived features such as hour_of_day if not already present.
- Remove Duplicates: Eliminate duplicate transaction records to maintain data integrity.

2. Feature Engineering
- Temporal Features: Use Date and Time to extract hour_of_day, Weekday, Month_name, and Time_of_Day.
- Spending Patterns: Group by coffee_name to identify high-revenue periods and popular products.
<img width="540" height="540" alt="image" src="https://github.com/user-attachments/assets/19900537-66c5-45c7-b079-a6c1648e5476" />

3. Data Transformation
- Categorical Encoding: Apply Label Encoding for ordinal data (e.g., Time_of_Day).Apply One-Hot Encoding for nominal variables like coffee_name.
- Scaling Numerical Data: Standardize or normalize numeric features such as money StandardScaler or MinMaxScaler to maintain proportionality in statistical models.
- Outlier Detection: Detect extreme values in money using boxplots to ensure robust analysis.
<img width="540" height="540" alt="image" src="https://github.com/user-attachments/assets/2eb11222-a313-40dd-94fd-86b9f72540f0" />

4. Exploratory Data Analysis (EDA)
- Time-Based Trends: Analyze total sales (money) by hour_of_day, Weekday, and Month_name.
- Seasonal Patterns: Explore monthly trends using Monthsort and Weekdaysort for chronological visualizations.
<img width="540" height="540" alt="image" src="https://github.com/user-attachments/assets/37a41a67-2316-44f6-b29e-34d7184ee94b" />

5. Predictive and Statistical Analysis
- Correlation & Association Analysis: Identify relationships between features such as money and hour_of_day.
<img width="540" height="540" alt="image" src="https://github.com/user-attachments/assets/f5b50408-17ea-421d-a065-1bce9a640544" />

## Techstack
- Python: Core programming language for data analysis.
- Pandas:	Data loading, cleaning, and manipulation.
- NumPy:	Numerical computations and array operations.
- Matplotlib:	Creating static visualizations and plots.
- Seaborn:	Statistical and categorical visualizations.
- Scikit-learn:	Data preprocessing and machine learning tasks.

## Conclusion
The Coffee Sales Dataset provides valuable insights into customer behavior, sales patterns, and operational trends in a coffee retail environment. Through this analysis, it is possible to:
- Identify peak sales hours and high-demand periods.
- Determine the most popular coffee types .
- Understand customer spending patterns and trends over time.
Overall, this dataset demonstrates the power of data-driven insights in improving business performance and enhancing customer satisfaction in the coffee industry.

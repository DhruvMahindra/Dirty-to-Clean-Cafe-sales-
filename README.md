Cafe Data Analysis - Data Cleaning Documentation
Overview
This project focuses on cleaning a dataset for cafe transactions. The dataset includes transaction details with columns for Transaction ID, Item, Quantity, Price Per Unit, Total Spent, Payment Method, Location, and Transaction Date. The goal of data cleaning was to ensure accuracy and consistency in preparation for analysis while handling missing or incomplete data responsibly.

Data Columns
Transaction ID: Unique identifier for each transaction.

Item: The name of the item sold.

Quantity: The quantity of the item sold.

Price Per Unit: The price of a single unit of the item.

Total Spent: Total cost for the transaction (Quantity * Price Per Unit).

Payment Method: The method used for payment (e.g., Cash, Credit Card, Digital Payment).

Location: The location of the transaction (e.g., Cafe branch or region).

Transaction Date: The date the transaction occurred.

Data Cleaning Steps
The following steps were taken to handle missing or incorrect information:

1. Handling Missing Item Names
Problem: Some rows had missing or "unknown" item names despite having a price listed.

Solution: Items with the same price but missing or "unknown" item names were marked as "Unknown". This was done because assigning a random item name could skew analysis and affect the accuracy of results.

2. Handling Missing Transaction Dates
Problem: Some transactions had missing transaction dates.

Solution: These rows were kept in the dataset with the transaction date field marked as "Unknown". Since the transaction date was not crucial for the analysis and there was no reliable way to determine it, these rows were preserved for completeness.

3. Handling Missing Payment Methods
Problem: Some transactions had missing or "unknown" payment methods.

Solution: Similar to transaction dates, these rows were labeled as "Unknown" in the Payment Method column. As payment method was not crucial for core analysis, these rows were retained without any further modification.

4. Dealing with Items Having the Same Price
Problem: Some rows contained multiple items with the same price but no identifying information (i.e., the item name was missing or labeled as "unknown").

Solution: Rows where items had the same price but missing or unknown names were marked as "Unknown". Providing a random item name could lead to incorrect conclusions in subsequent analysis, so the decision was made to retain them as "Unknown."

5. Handling Missing Locations
Problem: Some rows had missing or incorrect location information.

Solution: The missing location was marked as "Unknown" to maintain completeness. No further assumptions were made about the location since it could affect regional sales insights.

Data Integrity and Analysis
The objective of the data cleaning process was to prepare the dataset for insightful analysis while maintaining the integrity of the data. Missing or incomplete entries were handled transparently by labeling them as "Unknown" rather than making random imputation, which could lead to inaccurate results.

Key Assumptions and Decisions
Item names with missing values and matching prices were marked as "Unknown" to prevent random assignment.

Missing transaction dates and payment methods were labeled as "Unknown" because they were not critical to the core analysis.

Location and invalid entries were flagged as "Unknown" to ensure the dataset remained intact for analysis without making assumptions about missing values.

Conclusion
By handling missing or incomplete data thoughtfully and documenting the steps taken, this dataset remains useful for performing meaningful analysis while minimizing any distortions caused by imputed values. The dataset is now ready for insights on customer preferences, transaction patterns, and sales performance.

This is a screenshot of the raw dataset before any cleaning was applied. As seen below, it contains several issues:
1) Missing Item names
2) Unknown or blank transaction dates
3) Missing item, price per unit, quantity and total price.

![Cafe_Sales_Dirty Dataset](https://github.com/user-attachments/assets/b1ab8861-91ca-42cc-ac5b-695854320468)


After Applying data cleaning techniques in excel using filters and conditonal replacements the dataset is cleaned.
![Cafe-Sales Clean Dataset](https://github.com/user-attachments/assets/67a9bb20-a34d-47fb-8f9d-bbfdd487fa45)



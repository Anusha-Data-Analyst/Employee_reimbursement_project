# 📊 Employee_reimbursement_project
Employee reimbursement analysis project completed as part of the Codebasics Power BI course, co-created by Dhaval Patel and Hemanand Vadivel.

 ## 🗂️ Data Cleaning & Transformation (Power Query)
- Imported the fact_reimbursement dataset from Excel and structured the schema by assigning explicit data types across all fields, including dates, monetary amounts, and ID attributes. 
- Performed text normalization and data cleaning to standardize naming inconsistencies across dimensions—correcting typos in expense categories (e.g., fixing values like .Miscellaneous and TRANsporTAation) and standardizing project naming formats (e.g., ProjectA and ProjectB_ to Project_A and Project_B).
- Handled missing values by replacing null entries in the Currency field with a default value of INR. 
- Finally, performed a relational merge (Left Outer Join) with the Dim_employee lookup table on Employee_ID to enrich the reimbursement records with employee names.

## 🗂️ Data Transformation & Conditional Logic (Power Query)
- Connected directly to the Excel table reimbursement and configured the schema by setting correct data types for IDs, dates, text, and numerical values.
- To resolve missing currency information, applied custom conditional logic to infer and populate missing currency codes based on claim amounts—defaulting null entries to INR for amounts of 1,000 or greater, and USD for values below 1,000.

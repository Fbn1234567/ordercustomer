Day 9 – Processed E-commerce Dataset
Objective
Create a processed e-commerce dataset from Orders, Customers, and Products using Pandas.
Files
`Day9_Processed_Ecommerce.ipynb` – complete notebook
`Day9_Orders.csv` – input Orders dataset
`Day9_Customers.csv` – input Customers dataset
`Day9_Products.csv` – input Products dataset
`Day9_Processed_Ecommerce.csv` – final processed dataset
Operations demonstrated
Loaded all three CSV files with Pandas.
Inspected columns, data types, missing values, and duplicate rows.
Converted `Order_Date` to DateTime.
Used `merge()` to connect Orders with Customers and Products.
Used `concat()` to combine dataset summary DataFrames.
Used `apply()` to calculate `Total_Amount` and classify quantity levels.
Extracted year, month, day, month name, and day of week from the order date.
Organized the final columns and exported the processed CSV.
Dataset result
The final processed dataset contains 120 order records and 22 columns.
How to run
Open `Day9_Processed_Ecommerce.ipynb` in Jupyter Notebook, JupyterLab, Google Colab, or VS Code and run the cells from top to bottom.
GitHub submission
Create a repository and upload all five files listed above. Then submit the repository URL through the LMS.

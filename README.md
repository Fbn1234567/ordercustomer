# Day 9 – Processed E-commerce Dataset

## 📌 Project Overview

This project focuses on creating a **Processed E-commerce Dataset** using three CSV files:

* Orders
* Customers
* Products

The datasets were loaded and processed using **Python and Pandas**. Related information was combined using `merge()`, DataFrames were combined using `concat()`, useful columns were created using `apply()`, and DateTime operations were performed on the order date.

---

## 🎯 Objectives

The main objectives of this assignment are:

* Load CSV datasets using Pandas.
* Inspect and understand the datasets.
* Identify and handle duplicate records.
* Combine related datasets using `merge()`.
* Demonstrate the use of `concat()`.
* Create and transform columns using `apply()`.
* Convert order dates into DateTime format.
* Extract useful date information such as:

  * Year
  * Month
  * Day
  * Month Name
  * Day of Week
* Create a clean and meaningful final DataFrame.
* Export the processed dataset as a CSV file.

---

## 📂 Datasets Used

### 1. Orders Dataset

Contains information about customer orders, including:

* Order ID
* Order Date
* Customer ID
* Product ID
* Quantity
* Payment Method
* Order Status

### 2. Customers Dataset

Contains customer-related information such as:

* Customer ID
* Customer Name
* City
* Region
* Membership Type

### 3. Products Dataset

Contains product information such as:

* Product ID
* Product Name
* Category
* Brand
* Unit Price

---

## 🛠️ Technologies Used

* Python
* Pandas
* Jupyter Notebook / Google Colab
* GitHub

---

## 🔄 Data Processing Steps

### Step 1: Load the Datasets

The three CSV files were loaded using Pandas:

```python
pd.read_csv()
```

### Step 2: Data Inspection

The datasets were inspected using functions such as:

```python
.head()
.info()
.shape
.isnull().sum()
.duplicated().sum()
```

### Step 3: Remove Duplicate Records

Duplicate records were identified and removed using:

```python
.drop_duplicates()
```

### Step 4: Merge the Datasets

Orders were combined with Customers using `Customer_ID` and with Products using `Product_ID`.

```python
orders.merge(customers, on="Customer_ID", how="left")
```

```python
processed.merge(products, on="Product_ID", how="left")
```

### Step 5: Demonstrate `concat()`

`concat()` was used to demonstrate combining DataFrames vertically.

```python
pd.concat([df1, df2], ignore_index=True)
```

### Step 6: Use `apply()`

The total order amount was calculated using:

```python
Total_Amount = Quantity × Unit_Price
```

An additional quantity classification was also created:

* Low
* Medium
* High

using `apply()`.

### Step 7: DateTime Processing

The order date was converted into DateTime format:

```python
pd.to_datetime()
```

Additional date information was extracted:

```python
Order_Year
Order_Month
Order_Day
Order_Month_Name
Order_Day_Name
```

### Step 8: Create Final Dataset

The final dataset was organized into meaningful columns containing:

* Order information
* Customer information
* Product information
* Quantity and price
* Total amount
* Date-related information
* Quantity classification
* Payment and order status

### Step 9: Export Dataset

The final processed dataset was exported as:

```text
Day9_Processed_Ecommerce.csv
```

---

## 📊 Final Dataset

The processed dataset contains:

* **120 records**
* **22 columns**
* **0 missing values**

The final dataset combines information from all three original datasets into a single clean dataset.

---

## 📁 Repository Structure

```text
Day9-Processed-Ecommerce/
│
├── Day9_Processed_Ecommerce.ipynb
├── Day9_Orders.csv
├── Day9_Customers.csv
├── Day9_Products.csv
├── Day9_Processed_Ecommerce.csv
└── README.md
```

---

## ▶️ How to Run

1. Download or clone this repository.
2. Open `Day9_Processed_Ecommerce.ipynb`.
3. Make sure all three input CSV files are in the same folder.
4. Run the notebook cells from top to bottom.
5. The processed dataset will be generated as:

```text
Day9_Processed_Ecommerce.csv
```

---

## 📌 Conclusion

The three separate e-commerce datasets were successfully loaded, cleaned, merged, transformed, and combined into one meaningful processed dataset. Pandas functions such as `merge()`, `concat()`, `apply()`, and DateTime operations were used to complete the data-processing workflow.

The final dataset is ready for further **data analysis and visualization**.

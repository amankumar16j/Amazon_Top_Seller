---

# **Amazon Best Sellers Dataset Creation**

## **Project Overview**
The aim of this project was to leverage the **RapidAPI Amazon Online Data API** to create a comprehensive dataset of Amazon's best-selling products across 40 different departments. This dataset captures real-time data for the top-selling products and includes valuable details like product title, price, ratings, and more. The resulting dataset can be used for market research, trend analysis, or machine learning applications.

---

## **Features**
- Real-time data from Amazon's best-seller pages.
- Covers 40 departments/categories, including **Books**, **Electronics**, **Beauty & Personal Care**, **Software**, and more.
- Two pages of data per department for a broader coverage of best-sellers.
- Details for each product, including:
  - Product Title
  - Rank
  - Price
  - Number of Ratings
  - Reviews
  - Product URL
  - Department
  - Page Number

---

## **Project Steps**

### 1. **Setup and API Integration**
- Registered on **RapidAPI** and subscribed to the **Amazon Online Data API**.
- Retrieved the API key for secure access.
- Explored the API documentation to understand its endpoints and parameters.

### 2. **Defining the Scope**
- Compiled a list of 40 Amazon departments/categories to fetch data for.
- Limited the scope to the top 2 pages of each department for manageable yet comprehensive data collection.

### 3. **Data Collection**
- Used Python's `requests` library to query the API.
- Looped through the list of departments and fetched data for both pages.
- Checked the API responses for validity and handled any errors or failures gracefully.

### 4. **Data Transformation**
- Extracted the relevant data fields from the JSON responses.
- Created a pandas DataFrame using the extracted data.
- Enriched the dataset by adding the department name and page number for each product.

### 5. **Data Consolidation**
- Combined the data from all departments and pages into a single DataFrame.
- Ensured consistency in field names and cleaned the data where necessary.

### 6. **Exporting the Dataset**
- Saved the consolidated DataFrame as a CSV file using `pandas.DataFrame.to_csv()` for easy access and sharing.

---

## **Tech Stack**
- **Python**: Primary programming language.
- **Libraries**:
  - `requests`: For API calls.
  - `pandas`: For data manipulation and storage.
- **RapidAPI**: API platform used for accessing Amazon Online Data API.

---

## **How to Use**
1. Clone the repository to your local machine.
2. Install the required Python libraries:
   ```bash
   pip install pandas requests
   ```
3. Replace the placeholder API key in the script with your RapidAPI key.
4. Run the script to fetch data and save the dataset:
   ```bash
   python fetch_amazon_best_sellers.py
   ```
5. The dataset will be saved as a CSV file in the working directory.

---

## **Dataset Fields**
- `product_title`: Name of the product.
- `product_link`: URL to the Amazon product page.
- `rank`: Product's rank in its category.
- `price`: Price of the product (if available).
- `ratings`: Number of customer ratings.
- `reviews`: Total number of reviews.
- `department`: Amazon department/category the product belongs to.
- `page`: The page number where the product was listed.

---

## **Acknowledgments**
- **RapidAPI** for providing the Amazon Online Data API.
- Amazon for being the source of the data.

---

## **Future Enhancements**
- Extend the scope to more pages for each department.
- Automate regular updates to the dataset.
- Visualize product trends using Python libraries like `matplotlib` and `seaborn`.

---

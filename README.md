# 🚗 Car Dekho Market Trends Analysis

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** on the Car Dekho used-car dataset to understand the factors influencing car selling prices and identify important trends in the used-car market.

The analysis focuses on variables such as **selling price, present price, manufacturing year, kilometers driven, fuel type, seller type, transmission, and number of previous owners**.

Various statistical techniques and data visualizations are used to uncover relationships, distributions, trends, and patterns within the dataset.

---

## 🎯 Objectives

The main objectives of this project are:

* Understand the structure and characteristics of the Car Dekho dataset.
* Perform descriptive statistical analysis.
* Identify missing values and duplicate records.
* Analyze the distribution of numerical variables.
* Analyze categorical variables such as fuel type, seller type, and transmission.
* Study the relationship between present price and selling price.
* Analyze the impact of kilometers driven on resale price.
* Investigate the relationship between car age and selling price.
* Compare selling prices across different fuel types and transmission types.
* Analyze depreciation and depreciation percentage.
* Identify the most frequently listed and highest-priced cars.
* Generate meaningful visualizations to communicate market trends.

---

## 📊 Dataset

The dataset contains information about used cars listed on Car Dekho.

### Dataset Features

| Column          | Description                              |
| --------------- | ---------------------------------------- |
| `Car_Name`      | Name/model of the car                    |
| `Year`          | Manufacturing year of the car            |
| `Selling_Price` | Price at which the car was sold          |
| `Present_Price` | Current/existing market price of the car |
| `Kms_Driven`    | Total kilometers driven                  |
| `Fuel_Type`     | Type of fuel used by the car             |
| `Seller_Type`   | Type of seller                           |
| `Transmission`  | Transmission type                        |
| `Owner`         | Number of previous owners                |

The dataset contains **301 records and 9 original features**.

---

## 🛠️ Technologies Used

The following Python libraries and tools were used:

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Jupyter Notebook** – Development and analysis environment

---

## 🔍 Exploratory Data Analysis

The project includes the following stages of analysis.

### 1. Data Understanding

* Dataset shape
* Column names
* Data types
* Statistical summary
* Unique values
* Missing-value analysis
* Duplicate-value analysis

### 2. Univariate Analysis

The distributions of individual variables were analyzed using:

* Histograms
* KDE plots
* Boxplots
* Countplots
* Pie charts

Variables analyzed include:

* Selling Price
* Present Price
* Kilometers Driven
* Manufacturing Year
* Fuel Type
* Seller Type
* Transmission
* Previous Owners

### 3. Bivariate Analysis

Relationships between variables were explored using:

* Scatter plots
* Regression plots
* Boxplots
* Violin plots
* Bar charts

Important relationships include:

* Present Price vs Selling Price
* Kms Driven vs Selling Price
* Car Age vs Selling Price
* Selling Price vs Fuel Type
* Selling Price vs Transmission
* Selling Price vs Seller Type

### 4. Multivariate Analysis

Multiple variables were analyzed together using:

* Correlation heatmaps
* Pair plots
* Grouped visualizations
* Pivot tables
* Categorical cross-tabulations

---

## 📈 Feature Engineering

Additional variables were created to improve the analysis.

### Car Age

```python
df['Car_Age'] = 2026 - df['Year']
```

This represents the approximate age of the vehicle.

### Depreciation

```python
df['Depreciation'] = (
    df['Present_Price'] - df['Selling_Price']
)
```

### Depreciation Percentage

```python
df['Depreciation_Percentage'] = (
    (df['Present_Price'] - df['Selling_Price'])
    / df['Present_Price']
) * 100
```

These derived variables help analyze how vehicle age and other factors affect resale value.

---

## 📊 Visualizations

The project contains several types of visualizations, including:

* 📊 Bar charts
* 📈 Line charts
* 🔵 Scatter plots
* 📦 Boxplots
* 🎻 Violin plots
* 🥧 Pie charts
* 🌡️ Correlation heatmaps
* 🔲 Pair plots
* 📉 KDE plots
* Regression plots

Some of the key visualizations include:

### Selling Price Distribution

Shows the overall distribution and spread of used-car selling prices.
<img width="847" height="546" alt="Screenshot 2026-08-30 115934" src="https://github.com/user-attachments/assets/91474458-0222-4dc1-8e23-1ea884fb6c6e" />


### Present Price vs Selling Price

Examines the relationship between the current market price and the actual selling price.
<img width="835" height="542" alt="image" src="https://github.com/user-attachments/assets/4bc1f77d-14eb-44be-b2ac-ea796dd7238c" />


### Kms Driven vs Selling Price

Analyzes whether higher mileage is associated with lower resale prices.
<img width="836" height="542" alt="image" src="https://github.com/user-attachments/assets/a34cd861-118c-45c2-b3eb-52844614da93" />


### Car Age vs Selling Price

Examines how vehicle age affects resale value.
<img width="837" height="546" alt="image" src="https://github.com/user-attachments/assets/626a0d52-72e3-40c1-bca1-b6b4ace25333" />


### Selling Price by Fuel Type

Compares the selling-price distribution of different fuel categories.
<img width="761" height="542" alt="image" src="https://github.com/user-attachments/assets/ae3ccdc3-e56f-4038-8947-e35e0b46ba8d" />


### Correlation Heatmap

Shows relationships among numerical variables and helps identify variables strongly associated with selling price.
<img width="852" height="602" alt="image" src="https://github.com/user-attachments/assets/4871dc94-931b-4582-8e9c-c5fab2ad88aa" />


---

## 💡 Key Questions Explored

The analysis attempts to answer questions such as:

1. Which fuel type is most common in the dataset?
2. Which transmission type is most prevalent?
3. Which seller type has the most listings?
4. Which car models are listed most frequently?
5. How is selling price distributed?
6. Does present price have a strong relationship with selling price?
7. Does higher mileage reduce resale value?
8. Does vehicle age affect selling price?
9. Which fuel type has the highest average selling price?
10. Which transmission type has the highest average selling price?
11. How does seller type affect selling price?
12. Which cars have the highest resale prices?
13. Which cars experience the greatest depreciation?
14. Which cars retain their value relatively well?
15. What numerical variables have the strongest relationship with selling price?

---

## 🔑 Key Insights

The analysis can be used to derive insights such as:

* **Present Price is an important factor in determining Selling Price.**
* Older cars generally tend to have lower resale values.
* Kilometers driven can have an influence on resale value.
* Selling prices vary across fuel types.
* Transmission type can be associated with differences in resale prices.
* Different seller types may show different pricing patterns.
* Depreciation varies considerably across vehicles.
* A small number of vehicle models may account for a significant portion of the listings.

> Note: The exact numerical conclusions should be updated based on the final analysis results generated from the notebook.

---

## 📁 Project Structure

```text
Car-Dekho-Market-Trends-Analysis/
│
├── data/
│   └── car_dekho.csv
│
├── notebooks/
│   └── Car_Dekho_EDA.ipynb
│
├── images/
│   ├── selling_price_distribution.png
│   ├── price_relationship.png
│   ├── correlation_heatmap.png
│   └── car_age_vs_price.png
│
├── README.md
│
└── requirements.txt
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/car-dekho-market-analysis.git
```

Navigate to the project directory:

```bash
cd car-dekho-market-analysis
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Or install them from the requirements file:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/Car_Dekho_EDA.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and visualizations.

---

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
pandas
numpy
matplotlib
seaborn
jupyter
```

---

## 📌 Conclusion

This project demonstrates how **Exploratory Data Analysis can be used to understand the used-car market**.

By combining descriptive statistics with visual analysis, the project identifies relationships between vehicle characteristics and resale prices. Variables such as **present price, car age, kilometers driven, fuel type, transmission, and seller type** provide useful information for understanding used-car pricing patterns.

The analysis provides a foundation for further work such as **predictive modeling**, where machine learning algorithms can be used to predict the selling price of a used car based on its characteristics.

---

## 🚀 Future Improvements

Possible extensions of this project include:

* Build a machine learning model to predict selling price.
* Compare Linear Regression, Random Forest, Decision Tree, and Gradient Boosting models.
* Perform feature importance analysis.
* Apply hyperparameter tuning.
* Deploy the prediction model using Streamlit.
* Build an interactive dashboard using Power BI or Tableau.
* Add more recent used-car market data.
* Perform advanced statistical testing.
* Develop a recommendation system for buyers.

---

## 👨‍💻 Author

**Devi Sri Surya Sankar Chollangi**

Data Analytics / Data Science Project

---

## ⭐ Acknowledgements

This project was created for educational and analytical purposes using the Car Dekho used-car dataset.

If you found this project useful, consider giving the repository a ⭐ on GitHub.

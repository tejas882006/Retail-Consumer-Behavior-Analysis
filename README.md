# Retail Consumer Behavior Analysis

## Project Overview

Retail Consumer Behavior Analysis is an end-to-end data analytics project developed to explore customer shopping behavior and identify patterns that can support data-driven business decisions.

The project uses Python, Pandas, MySQL, and Power BI to process retail data, perform structured business analysis, and visualize customer behavior through an interactive dashboard.

The analysis focuses on customer demographics, purchasing patterns, product preferences, discount usage, subscription behavior, and customer segmentation.

This project demonstrates a complete data analytics workflow, from data preprocessing and exploratory data analysis to SQL-based analysis and interactive visualization.

## Project Objectives

- Analyze customer purchasing behavior and spending patterns.
- Explore relationships between customer demographics and purchasing activity.
- Identify highly rated products and frequently purchased items.
- Investigate discount usage and promotional patterns.
- Compare purchasing behavior across subscription groups.
- Segment customers according to their previous purchase history.
- Examine purchasing patterns across different shipping types.
- Develop an interactive Power BI dashboard.
- Translate analytical observations into practical business recommendations.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data analysis and preprocessing |
| Pandas | Data cleaning, transformation, and exploration |
| Jupyter Notebook | Interactive analysis and documentation |
| MySQL | Database management and SQL-based analysis |
| MySQL Workbench | Executing SQL queries and examining results |
| Power BI Desktop | Dashboard development and visualization |
| Git and GitHub | Version control and project hosting |

## Repository Structure

```text
Retail-Consumer-Behavior-Analysis/
│
├── Dashboard/
│   └── Retail_Consumer_Behavior_Dashboard.pbix
│
├── Data/
│   └── customer_shopping_behavior.csv
│
├── Notebook/
│   └── Retail Consumer Behavior Analysis.ipynb
│
├── SQL/
│   └── retail_analysis.sql
│
├── .gitignore
├── LICENSE
├── README.md
├── Retail-Consumer-Behavior-Analysis.pdf
└── Retail-Consumer-Behavior-Analysis.pptx
```

The PDF report and PowerPoint presentation are stored in the root directory of the repository.

Note: The filenames shown above are examples. Ensure that the names match the actual files uploaded to GitHub.

## Dataset Description

**Dataset Name:** Shopping Trends and Customer Behaviour Dataset

**Dataset Source:** [Kaggle - Shopping Trends and Customer Behaviour Dataset](https://www.kaggle.com/datasets/sahilislam007/shopping-trends-and-customer-behaviour-dataset)

The dataset contains information about customer demographics, purchases, product categories, discounts, ratings, shipping preferences, and subscription status.

It was used for educational purposes to perform data cleaning, exploratory data analysis, SQL-based analysis, and Power BI visualization.

Please refer to the original Kaggle page for the dataset's licence and usage conditions. Attribution is provided to the original dataset uploader.

## Project Workflow

### 1. Data Loading and Exploration

The dataset was imported into a Pandas DataFrame for initial inspection and analysis.

Key activities:
- Loaded the CSV dataset using Pandas.
- Examined data types and dataset structure using `df.info()`.
- Generated descriptive statistics using `df.describe()`.
- Inspected missing values and explored numerical and categorical variables.

### 2. Data Cleaning and Preprocessing

The dataset was cleaned and transformed to improve consistency and prepare it for further analysis.

Key activities:
- Identified missing values in the review rating column.
- Imputed missing review ratings using the median rating of the corresponding product category.
- Standardized column names using snake_case.
- Created an `age_group` feature for demographic analysis.
- Derived `purchase_frequency_days` from purchase-frequency categories.
- Examined potential redundancy between discount and promotional-code information.

### 3. Database Integration Using MySQL

The prepared dataset was loaded into MySQL for structured analysis.

**Database Name:** `customer_behavior`

**Table Name:** `customer`

MySQL was used to execute analytical queries, aggregate data, compare customer groups, examine product-level patterns, and investigate purchasing behavior.

### 4. SQL-Based Business Analysis

SQL queries were developed to investigate key business questions, including:

- How does revenue vary across customer demographics?
- Which discount users spend above the average purchase amount?
- Which products receive the highest average ratings?
- How does purchasing behavior vary by shipping type?
- How do subscribers and non-subscribers differ in purchasing behavior?
- Which products have the highest discount rates?
- How can customers be segmented using previous purchase history?
- Which products are frequently purchased within their respective categories?
- How does subscription status vary among repeat buyers?
- How does revenue differ across customer age groups?

The SQL analysis demonstrates the use of filtering, aggregation, conditional logic, grouping, subqueries, and ranking techniques to investigate retail business questions.

## Customer Segmentation

Customers were classified using the `previous_purchases` column.

### Segmentation Rules

| Customer Segment | Condition | Description |
|---|---|---|
| New | `previous_purchases <= 1` | Records with zero or one previous purchase |
| Returning | `previous_purchases BETWEEN 2 AND 5` | Records with two to five previous purchases |
| Loyal | `previous_purchases > 5` | Records with more than five previous purchases |

This segmentation helps organize purchasing records according to previous purchase history and supports further analysis of customer behavior.

The segmentation results and detailed interpretation are documented in the project report.

## Power BI Dashboard

An interactive Power BI dashboard was developed to present customer behavior patterns and key business metrics visually.

### Dashboard Features

- KPI cards for customer count, average purchase amount, and average review rating.
- Subscription-status visualization.
- Sales and revenue analysis by product category.
- Revenue comparisons across age groups.
- Customer-count comparisons across age groups.
- Interactive slicers for subscription status, gender, category, and shipping type.

The dashboard enables users to explore different customer groups and examine purchasing patterns through interactive filters.

## Business Recommendations

The analytical workflow supports the investigation of several potential business opportunities.

### Customer Subscription

Evaluate subscriber benefits and targeted campaigns to explore opportunities for improving subscription conversion and customer retention.

### Customer Loyalty

Consider loyalty programs and rewards for repeat purchasers. Monitor changes in customer segments over time.

### Discount Strategy

Review discount patterns across products and investigate their relationship with sales performance and profitability.

### Product Marketing

Use product ratings and purchasing patterns to identify products that may be suitable for targeted marketing campaigns.

### Customer Segmentation

Use customer purchase history and demographic characteristics to develop more targeted customer engagement strategies.

### Shipping Preferences

Investigate purchasing patterns across shipping types to support decisions about shipping options and customer experience.

These recommendations are potential areas for further investigation rather than proven causal conclusions.

## How to Run the Project

### Prerequisites

Prepare the following tools:

- Python 3.x
- Jupyter Notebook
- Pandas
- MySQL Server
- MySQL Workbench
- Power BI Desktop

### Step 1: Clone the Repository

```bash
git clone https://github.com/tejas882006/Retail-Consumer-Behavior-Analysis.git
```

Navigate to the project directory:

```bash
cd Retail-Consumer-Behavior-Analysis
```

### Step 2: Install Python Dependencies

Install the main Python dependencies:

```bash
pip install pandas sqlalchemy pymysql jupyter
```

Install any additional packages required by the notebook.

### Step 3: Prepare the Dataset

Place the dataset CSV file inside the `Data/` directory.

If the dataset is obtained separately, review the original Kaggle page for its licence and usage conditions.

### Step 4: Run the Python Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the following file:

`Notebook/Retail Consumer Behavior Analysis.ipynb`

Execute the cells in order to inspect, clean, transform, and prepare the dataset.

### Step 5: Configure MySQL

1. Start MySQL Server.
2. Create the `customer_behavior` database if it does not already exist.
3. Configure the database connection using environment variables or another secure method.
4. Execute the notebook's database integration steps to load the prepared data.

Do not commit database passwords or other credentials to GitHub.

### Step 6: Execute SQL Queries

Open `SQL/retail_analysis.sql` in MySQL Workbench.

Select the `customer_behavior` database and execute the queries.

Ensure that the table and column names match those created by the Python notebook.

### Step 7: Open the Power BI Dashboard

Open the Power BI file located at:

`Dashboard/Retail_Consumer_Behavior_Dashboard.pbix`

Configure the data source if prompted and refresh the dashboard as required.

## Project Deliverables

| Deliverable | Description |
|---|---|
| Python Notebook | Data exploration, cleaning, preprocessing, and feature engineering |
| SQL Script | Business queries and customer behavior analysis |
| Power BI Dashboard | Interactive visualization of customer behavior |
| Project Report | Detailed methodology, analytical findings, and recommendations |
| Project Presentation | PowerPoint presentation summarizing the project workflow and key insights |

## Limitations

- The analysis is based on the supplied dataset and may not represent all retail customers.
- The findings describe observed patterns and do not establish causal relationships.
- Customer segmentation is based on previous purchase history and the rules defined in the SQL query.
- Purchase-frequency days are derived from the mapping applied to the original frequency categories.
- Business recommendations should be validated using additional data and appropriate experiments.

## Future Enhancements

Potential future improvements include:

- Customer lifetime value analysis.
- Customer retention and churn analysis.
- Customer segmentation using clustering algorithms.
- Predictive modeling for purchase behavior.
- Automated data refresh and dashboard updates.
- Profitability analysis to evaluate promotional effectiveness.

## Author

**Tejas Singh Nirvan**

GitHub: [tejas882006](https://github.com/tejas882006)

## License

Refer to the `LICENSE` file in this repository for the terms governing the project code.

The dataset is sourced separately from Kaggle and may have its own licensing and usage restrictions. The repository's code licence does not automatically grant permission to redistribute the dataset.

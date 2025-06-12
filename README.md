# 🚀 Olist E-commerce Data Analysis: Unlocking Business Growth through Customer Insights
## 📌 Project Overview
This project dives deep into the Olist E-commerce Public Dataset, using Exploratory Data Analysis (EDA) and Machine Learning (K-Means Clustering) to uncover key shopping trends and customer behaviors. Our main goal is to turn these data discoveries into actionable business recommendations. This will help Olist boost customer satisfaction, fine-tune sales strategies, and improve overall business performance.

## 🎯 Key Objectives
This analysis is structured to achieve these core objectives:

* 📈 **Understand Overall Shopping Trends:** We'll analyze sales patterns over time, pinpoint popular product categories, and look at preferred payment methods.
* ⭐ **Evaluate Product & Seller Performance:** We'll check the quality and performance of both product categories and individual sellers based on customer reviews and sales figures.
* 🌍 **Analyze Regional Shopping Behaviors:** We'll identify high-spending regions and understand if customers tend to buy from local or distant sellers.
* 👥 **Perform Customer Segmentation with K-Means Clustering**: We'll split Olist's customers into distinct groups based on their purchasing behavior (Recency, Frequency, Monetary value). This will help create highly targeted marketing campaigns.
* 💡 **Formulate Actionable Business Recommendations:** We'll combine all our findings to give Olist clear, practical strategies they can use to increase sales, keep customers longer, and make operations more efficient.
## 🛠️ Tools & Libraries
This project uses the following key technologies and Python libraries:

* **Python:** The core programming language for all data manipulation and analysis.
* **Jupyter Notebook:** For an interactive environment to explore, analyze, and visualize data.
* **Pandas:** Essential for loading, cleaning, and managing large datasets.
* **NumPy:** Used for high-performance numerical computations.
* **Matplotlib & Seaborn:** Powerful libraries for creating clear and insightful data visualizations.
* **Scikit-learn:** Utilized for machine learning tasks, specifically for implementing K-Means clustering and data preprocessing techniques like scaling.
## 📊 Data Source
* This project uses the comprehensive Olist E-commerce Public Dataset. It contains real-world order data from customers on the Olist marketplace in Brazil, covering 2016 to 2018. You can find this dataset on Kaggle. It includes several interconnected CSV files with details on orders, customers, products, sellers, payments, and customer reviews.

## 🛠️ Methodology & Techniques
Our analysis follows a robust data science pipeline:

### 1. Data Loading & Preprocessing:
* Loading and merging all relevant CSV files into one complete dataset.
* Carefully handling missing values (NaNs) by using appropriate methods for each column (e.g., date imputation, categorical filling).
* Converting data types correctly, especially for datetime objects, which is crucial for time-series analysis.
### 2. Feature Engineering:
* Creating important new features like item_total_price (price + freight per item) and order_total_value (total value of all items in an order).
* Deriving delivery durations (actual_delivery_days, delivery_delay_days) and detailed time-based features (purchase_year, purchase_month, purchase_hour, etc.) from timestamps.
### 3. Deep Exploratory Data Analysis (EDA):
* **Time-Series Analysis:** Visualizing monthly and yearly sales trends, and identifying best-selling product categories over time.
* **Categorical Analysis:** Finding the top 10 most purchased product categories by how many items were sold.
* **Payment Method Distribution:** Understanding which payment types are most common.
* **Review Performance Analysis:** Looking at average review scores for product categories and sellers to highlight both strong and weak performers.
* **Geographical Trends:** Mapping high-shopping regions and seeing if customers prefer buying from local sellers (in the same state).
### 4. Customer Segmentation with Machine Learning:
* **RFM Feature Calculation:** Calculating Recency, Frequency, and Monetary values for each unique customer.
* **Data Scaling:** Applying the right scaling techniques to RFM features to make clustering work best.
* **K-Means Clustering:** Using the K-Means algorithm to group customers into distinct segments based on their RFM profiles.
* **Cluster Profiling:** Analyzing and explaining the characteristics of each customer segment (e.g., "Champions," "Loyal Customers," "At-Risk Customers").
### 5. Interpretation & Recommendations:
* Bringing together all the key insights from EDA and customer segmentation.
* Translating these analytical findings into concrete, actionable business strategies for Olist, covering marketing, sales, and operations.
## 📁 Project Structure
```Plaintext

olist-e-commerce-analysis/
│
├── data/
│   ├── olist_customers_dataset.csv
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_sellers_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_order_reviews_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
│
├── notebooks/
│   └── olist_eda_and_segmentation.ipynb # Main Jupyter Notebook for analysis
│
├── reports/
│   ├── figures/ # Folder to save generated plots and images from EDA/ML
│   │   ├── monthly_sales_trend.png
│   │   ├── top_categories_by_item_count.png
│   │   └── ... (other relevant plots)
│   └── README_insights.md # Optional: A separate markdown file for detailed insights/recommendations
│
├── .gitignore # Specifies intentionally untracked files to ignore
├── requirements.txt # Lists all required Python libraries
└── README.md
```
## 💻 Setup & Installation
To run this analysis, make sure you have Python installed (preferably Python 3.8+). You can set up your environment and install the necessary libraries using pip:

```Bash

# Clone the repository
git clone https://github.com/nkhanh0104/olist-data-science.git
cd olist-data-science
```
(Optional) Create and activate a virtual environment for a clean setup
```Bash
python -m venv venv
source venv/bin/activate # On Windows: `venv\Scripts\activate`

# Install required libraries
# It's a good practice to create a requirements.txt file by running 'pip freeze > requirements.txt'
# after installing necessary libraries in your environment.
pip install pandas matplotlib seaborn scikit-learn jupyter
# Or install directly from a requirements.txt file:
# pip install -r requirements.txt
```
## 🏃 How to Run the Analysis
### 1. Download the Dataset:
* Get the Olist E-commerce Public Dataset from Kaggle. Extract all the .csv files and put them into a sub-directory called data/ inside your project folder.
### 2. Launch Jupyter Notebook:
```Bash

jupyter notebook
```
### 3. Open the Main Notebook:
* Go to and open the main analysis notebook (e.g., olist_eda_and_segmentation.ipynb) in your Jupyter environment.
### 4. Execute Cells Sequentially:
* Run all the cells in the notebook from top to bottom. This will perform the data loading, preprocessing, EDA, customer segmentation, and generate all visualizations.
## ✨ Results & Key Insights
Based on our analysis of the Olist E-commerce dataset, we've found several crucial insights:

* **Sales Trends & Seasonality:** E-commerce sales clearly grew from late 2016 to mid-2018. Sales often peaked late in the year and dipped in early months, suggesting seasonal patterns or marketing cycles.
* **Dominant Product Categories:** "Health & Beauty," "Bed, Bath & Table," and "Sports & Leisure" consistently sold the most items and generated the highest revenue, showing strong consumer demand in these areas.
* **Payment Preferences:** Credit cards are by far the most popular payment method. This means Olist needs to keep their credit card processing secure and reliable.
* **Review Landscape:** While most reviews are positive, some product categories (like "Computers" or "Books") and specific sellers frequently get lower ratings. This points to areas where Olist could improve quality or manage vendors better.
* **Geographical Concentration:** Most customers and sales revenue come from Brazil's Southeast region (especially São Paulo and Rio de Janeiro states). This highlights its vital importance to Olist. Interestingly, many purchases happen between customers and sellers in different states, indicating a good national logistics network, though local purchases offer faster delivery.
* **Customer Segments (K-Means):** Our K-Means clustering model identified three distinct customer groups:
  * **Champions:** These are Olist's most valuable customers. They've bought recently, frequently, and spent a lot. They're likely very loyal.
  * **New/Engaging Customers:** These are relatively new buyers who buy somewhat often and spend a moderate amount. They have high potential for future growth.
  * **At-Risk/Churning Customers:** These customers haven't bought recently, don't buy often, and haven't spent much. They're less engaged and might stop buying from Olist soon.
## 💡 Actionable Business Recommendations
Drawing from these insights, we propose the following concrete actions for Olist:

### 1. Optimize Seasonal Campaigns:
* **Action:** Plan and launch targeted marketing campaigns for peak sales months (like Q4). Offer special deals on popular categories such as "Health & Beauty" and "Bed, Bath & Table."
* **Impact:** Boost revenue during busy periods by aligning promotions with proven customer buying habits.
### 2. Enhance Credit Card Experience:
* **Action:** Continuously monitor and improve the reliability and security of credit card payment systems. Consider giving incentives for using credit cards.
* **Impact:** Capitalize on the most preferred payment method, making transactions smoother and increasing successful purchases.
### 3. Improve Underperforming Categories/Sellers:
* **Action:** Investigate categories and sellers that consistently get low review scores (e.g., "Computers"). Work with these sellers to improve product quality, refine descriptions, or provide better customer service training.
* **Impact:** Reduce negative customer experiences, improve Olist's overall reputation, and potentially grow sales in currently weaker areas.
### 4. Tailored Customer Engagement Strategies:
* **For "Champions":** Create loyalty programs, offer exclusive early access to new products, or send personalized recommendations for high-value items to keep them engaged and loyal.
* **For "New/Engaging Customers":** Focus on retention efforts with personalized follow-up emails, "welcome back" discounts, or cross-selling suggestions based on their first purchases to encourage them to buy again.
* **For "At-Risk/Churning Customers":** Develop re-engagement strategies like win-back promotions, surveys to understand their dissatisfaction, or special offers on products they've bought before to prevent them from leaving.
* **Impact:** Maximize the Customer Lifetime Value (CLV) by making sure marketing efforts match the specific needs and behaviors of each customer group.
### 5. Strategic Regional Focus & Logistics:
* **Action:** While maintaining a national presence, consider putting extra marketing and logistics resources into the dominant Southeast region to fully use its high buying power. Also, analyze delivery times and costs for cross-state orders to find ways to make them more efficient.
* **Impact:** Grow market share in high-potential areas and potentially improve overall customer satisfaction through better delivery experiences.
## ✍️ Author
Nguyen Nhu Khanh
Aspiring Data Scientist with a strong software development background, currently leveraging data to grow the business and optimize customer experience.

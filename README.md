# amazon-data-cleaning-task1
# Task 1: Data Cleaning and Preprocessing (Amazon Sales Dataset)

## Objective
The goal of this project was to clean, format, and prepare a raw Amazon sales dataset for downstream data analysis and visualization. The pipeline was built step-by-step using Python and the Pandas library in a Jupyter Notebook.

## Data Cleaning Steps Taken
1. **Header Standardization:** Converted all column names to lowercase and replaced spaces with underscores (`_`) for standard formatting.
2. **Data Type Correction:** - Stripped currency characters (`₹`) and commas from `actual_price` and `discounted_price` and cast them to floats.
   - Cleaned percentage signs (`%`) from `discount_percentage`.
   - Handled non-numeric anomalous characters in `rating` and `rating_count`, converting them into numeric formats.
3. **Missing Value Treatment:** Checked for null values using `.isnull()`. Replaced missing data fields in numeric ratings with the median values of those columns to maintain distribution sanity.
4. **Deduplication:** Checked and dropped structural duplicates using `.drop_duplicates()`.
5. **Text Standardization:** Extracted a primary category feature (`main_category`) by parsing complex string categorization chains.

## Deliverables
- `data/amazon.csv`: Raw, uncleaned source data.
- `data/amazon_cleaned.csv`: Final processed dataset ready for analytics.
- `data_cleaning_notebook.ipynb`: Complete documented step-by-step Jupyter Notebook.

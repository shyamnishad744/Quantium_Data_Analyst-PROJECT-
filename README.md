Quantium Data analyst project [ Source- FORAGE ]

📘 quantium1.ipynb – Data Cleaning, Feature Engineering & Visualization
In this notebook, I started by loading two datasets:

QVI_purchase_behaviour.csv (customer data)

QVI_transaction_data.xlsx (transaction data)

I merged them using the LYLTY_CARD_NBR column to get one complete dataset for analysis.

🔍 What I did:
Checked for null values and duplicates and cleaned the data.

Converted the Excel-style date to a proper datetime format.

Created a new unit_price column by dividing TOT_SALES by PROD_QTY.

Extracted PACK_SIZE and BRAND from the product name as part of feature engineering.

Grouped the data by PREMIUM_CUSTOMER and LIFESTAGE to calculate:

Total sales

Average sale per transaction

Number of transactions

Average pack size

Average price per unit

Saved the summarized segment data to a CSV file.

📊 Visualizations:
Created a barplot to show total spend by lifestage and premium customer type.

Used a boxplot to visualize segment spend per unit across different groups.

This notebook helped me understand how different customer segments behave, and set the base for deeper analysis in the next notebook.


#QUANTIUM SECOND PROJECT  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📘 quantium2.ipynb – Trial Store Analysis & Store Matching
In this notebook, I focused on analyzing store performance over time and identifying a control store to compare with trial stores. The main goal was to evaluate the impact of a trial campaign on sales, transactions, and customer behavior.

🔍 What I did:
Loaded the combined data (QVI_data.csv).

Removed duplicates and converted the date column to proper datetime format.

Extracted MONTH from the DATE column to make monthly-level analysis easier.

Created monthly metrics for each store:

Total spend

Number of customers (unique loyalty cards)

Number of transactions

Average transactions per customer

Created a new column avg_txn_per_customer for better insight into repeat purchases.

🔎 Trial vs Control Store Matching:
I wrote a custom function get_control_store() to identify a control store for a given trial store. The function:

Compared each store’s trends in the pre-trial period.

Measured similarity using correlation of:

Total spend

Number of customers

Average transactions per customer

Selected the store with the most similar trends as the control store.

This logic helped simulate a natural comparison to evaluate how well the trial worked without running it in all stores.

📊 Visualizations:
Monthly trends of key metrics like sales and transactions.

Compared trial vs control stores visually to confirm similarity before the campaign.

📈 Outcome:
Successfully identified control stores for trial evaluation.

Prepared data for final impact analysis and strategic decision-making.



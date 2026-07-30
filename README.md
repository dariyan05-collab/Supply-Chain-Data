# Supply-Chain-Data
Supply chain data set
Before cleaning - Checked for missing values across all 24 columns dataset was complete with no nulls, so no imputation or row-dropping was required.
#   Column                   Non-Null Count  Dtype  
---  ------                   --------------  -----  
 0   Product type             100 non-null    object 
 1   SKU                      100 non-null    object 
 2   Price                    100 non-null    float64
 3   Availability             100 non-null    int64  
 4   Number of products sold  100 non-null    int64  
 5   Revenue generated        100 non-null    float64
 6   Customer demographics    100 non-null    object 
 7   Stock levels             100 non-null    int64  
 8   Lead times               100 non-null    int64  
 9   Order quantities         100 non-null    int64  
 10  Shipping times           100 non-null    int64  
 11  Shipping carriers        100 non-null    object 
 12  Shipping costs           100 non-null    float64
 13  Supplier name            100 non-null    object 
 14  Location                 100 non-null    object 
 15  Lead time                100 non-null    int64  
 16  Production volumes       100 non-null    int64  
 17  Manufacturing lead time  100 non-null    int64  
 18  Manufacturing costs      100 non-null    float64
 19  Inspection results       100 non-null    object 
 20  Defect rates             100 non-null    float64
 21  Transportation modes     100 non-null    object 
 22  Routes                   100 non-null    object 
 23  Costs                    100 non-null    float64
 Data columns (total 24 columns):
 #   Column                   Non-Null Count  Dtype  
---  ------                   --------------  -----  
 0   product_type             100 non-null    object 
 1   sku                      100 non-null    object 
 2   price                    100 non-null    float64
 3   availability             100 non-null    int64  
 4   number_of_products_sold  100 non-null    int64  
 5   revenue_generated        100 non-null    float64
 6   customer_demographics    100 non-null    object 
 7   stock_levels             100 non-null    int64  
 8   lead_times               100 non-null    int64  
 9   order_quantities         100 non-null    int64  
 10  shipping_times           100 non-null    int64  
 11  shipping_carriers        100 non-null    object 
 12  shipping_costs           100 non-null    float64
 13  supplier_name            100 non-null    object 
 14  location                 100 non-null    object 
 15  lead_time                100 non-null    int64  
 16  production_volumes       100 non-null    int64  
 17  manufacturing_lead_time  100 non-null    int64  
 18  manufacturing_costs      100 non-null    float64
 19  inspection_results       100 non-null    object 
 20  defect_rates             100 non-null    float64
 21  transportation_modes     100 non-null    object 
 22  routes                   100 non-null    object 
 23  costs                    100 non-null    float64
dtypes: float64(6), int64(9), object(9)
memory usage: 18.9+ KB
lead_times	lead_time
0	7	29
1	30	23
2	10	12
3	13	24
4	3	5
5	27	10
6	15	14
7	17	22
8	10	13
9	27	29

# Text Columns
product_type	sku	price	availability	number_of_products_sold	revenue_generated	customer_demographics	stock_levels	lead_times	order_quantities	...	location	lead_time	production_volumes	manufacturing_lead_time	manufacturing_costs	inspection_results	defect_rates	transportation_modes	routes	costs
0	Haircare	SKU0	69.808006	55	802	8661.996792	Non-Binary	58	7	96	...	Mumbai	29	215	29	46.279879	Pending	0.226410	Road	Route B	187.752075
1	Skincare	SKU1	14.843523	95	736	7460.900065	Female	53	30	37	...	Mumbai	23	517	30	33.616769	Pending	4.854068	Road	Route B	503.065579
2	Haircare	SKU2	11.319683	34	8	9577.749626	Unknown	1	10	88	...	Mumbai	12	971	27	30.688019	Pending	4.580593	Air	Route C	141.920282
3	Skincare	SKU3	61.163343	68	83	7766.836426	Non-Binary	23	13	59	...	Kolkata	24	937	18	35.624741	Fail	4.746649	Rail	Route A	254.776159
4	Skincare	SKU4	4.805496	26	871	2686.505152	Non-Binary	5	3	56	...	Delhi	5	414	3	92.065161	Fail	3.145580	Air	Route A	923.440632
5 rows × 24 columns
 
# Supply Chain Data Cleaning & Analysis

## Overview
This project involved cleaning and validating a supply chain dataset containing 100 product records across 24 attributes — including pricing, inventory, shipping, manufacturing, and quality metrics.

## Tools Used
- Python (pandas) — data cleaning and validation
- Google Colab — development environment
- Git/GitHub — version control

## Process
1. **Data inspection** — reviewed structure, data types, and completeness across all 24 columns
2. **Integrity checks** — verified no missing values or duplicate rows existed in the dataset
3. **Column standardization** — normalized column names to lowercase, underscore-separated format for consistency
4. **Redundancy check** — identified two similarly named columns (`lead_time` and `lead_times`) and investigated whether they represented duplicate information
5. **Text standardization** — cleaned inconsistent casing/whitespace across categorical fields (product type, shipping carrier, location, etc.)
6. **Logical validation** — filtered for impossible values (e.g., negative price, revenue, or availability)

## Key Finding
The dataset was already largely clean — 0 missing values and 0 duplicate rows across all columns. The cleaning process focused on standardization and validation rather than fixing broken data, which is itself a meaningful checkpoint before analysis.

## Files
- `supply_chain_data.csv` — original raw dataset
- `cleaned_supply_chain_data.csv` — cleaned, standardized dataset ready for analysis/visualization
- `cleaning_notebook.ipynb` — full Python cleaning process 
## Next Steps
Building a Power BI dashboard to visualize supply chain KPIs (lead times, shipping costs, defect rates) using this cleaned dataset.

<img width="1282" height="725" alt="image" src="https://github.com/user-attachments/assets/014020f1-b92f-4ec1-93d7-12cf29020f67" />


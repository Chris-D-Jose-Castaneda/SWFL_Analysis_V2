# SWFL Housing Market (2020–Present)

Data‑driven dashboard tracking residential real‑estate trends across Southwest Florida (Bradenton ➜ Everglades City) from Jan 2020 onward. Powered by Redfin data, Python 3.10, and Streamlit.

## Goals
- Measure COVID‑era housing shifts  
- Map & compare price hot‑spots  
- 12‑month SARIMA price forecast  
- Scalable pipeline for statewide → national roll‑out  

## Data
- **Source:** Redfin listings (scraped)  
- **Range:** 2020‑01‑01 → today  
- **Counties:** Manatee, Sarasota, Charlotte, Lee, Collier  
- **File:** `data/cleaned_redfin_data.csv`  

## Method
1. Scrape & clean (Selenium + pandas)  
2. EDA & visuals (matplotlib / seaborn)  
3. Geo‑clusters (k‑means)  
4. SARIMA forecast (statsmodels)  
5. Option‑style valuation (QuantLib)  
6. Streamlit UI  

## Visualizations
- Interactive EDA maps that are clusters like the other SWFL project
- 12 month forecast
- Option Pricing Module

## Quick Start
```bash
git clone https://github.com/Chris-D-Jose-Castaneda/SWFL_Analysis_V2.git
cd SWFL_Analysis_V2
conda create -n swfl python=3.10 -y && conda activate swfl
pip install -r requirements.txt
streamlit run app.py

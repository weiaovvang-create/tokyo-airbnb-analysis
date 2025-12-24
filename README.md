## Interactive Map

An interactive heatmap of Airbnb listings in Tokyo is available here:

https://weiaovvang-create.github.io/tokyo-airbnb-analysis/tokyo_airbnb_heatmap.html

# Tokyo Airbnb Data Analysis

This project analyzes pricing patterns, room types, host behavior, and geographic distribution of Airbnb listings in Tokyo.  
Using real-world data from Inside Airbnb, the analysis aims to extract practical business insights relevant to the short-term rental market.

The project focuses on exploratory data analysis (EDA) and visualization, emphasizing interpretability and decision-oriented insights rather than predictive modeling.

---

## Objectives

- Explore Airbnb price distribution and market structure in Tokyo  
- Compare pricing differences across room types and neighborhoods  
- Identify host concentration and professional hosting behavior  
- Visualize geographic clustering of listings using static and interactive maps  
- Derive business-relevant insights for hosts, platforms, and regulators  

---

## Dataset

- **Source:** Inside Airbnb (Tokyo listings)
- **Content:** Listing-level data including price, room type, host ID, neighborhood, and geographic coordinates
- **Format:** CSV

The original dataset (~69MB) is excluded from version control and not included in this repository.

The notebook assumes the dataset is available locally at `data/listings.csv`.

---

## Data Cleaning & Preprocessing

The following preprocessing steps were applied:

- Converted price values from string format (e.g. "$12,345.00") to numeric
- Removed extreme price outliers above the 99th percentile to improve visualization clarity
- Retained missing values unless directly affecting analysis validity

These steps ensure clearer interpretation while preserving the overall market structure.

---

## Exploratory Data Analysis

### 1. Price Distribution
- Prices exhibit a strong right-skewed, long-tail distribution
- A small number of luxury listings significantly exceed the average market price
- Log-scaled visualization improves interpretability

### 2. Room Type Analysis
- Entire home/apartment listings command significantly higher prices than private or shared rooms
- This reflects strong demand from short-term tourists and group travelers

### 3. Host Concentration
- A small number of hosts control a disproportionately large share of listings
- This suggests the presence of professional or semi-professional hosting behavior

### 4. Neighborhood Price Comparison
- Central neighborhoods show higher average prices
- Location plays a critical role in pricing power

---

## Geographic Analysis

Two complementary approaches were used:

- **Scatter Plot:** Overall spatial distribution of listings across Tokyo  
- **Interactive Heatmap (Folium):** High-density clusters around major wards such as  
  **Shinjuku, Shibuya, and Minato**, closely aligned with transportation hubs and tourist centers

The interactive heatmap is exported as an HTML file for external viewing.

---

## Key Business Insights

- Airbnb listings in Tokyo are highly concentrated in central wards and near major transportation hubs  
- Entire home/apartment listings consistently achieve higher price levels than other room types  
- Hosting activity is unevenly distributed, with high-volume hosts dominating supply  
- The market displays a long-tail price structure driven by a minority of premium listings  

---

## Business Implications

- New hosts may face strong competition in central Tokyo and could explore underserved outer neighborhoods  
- Platform regulators may need to monitor high-volume hosts to ensure compliance and market fairness  
- Pricing strategies should prioritize location and room-type differentiation rather than uniform pricing models  

---

## Tools & Technologies

- Python 3  
- pandas, numpy  
- matplotlib, seaborn  
- folium (interactive geospatial visualization)  
- Jupyter Notebook  

---

## How to Run

```bash
cd notebooks
jupyter notebook airbnb_eda.ipynb
```

The interactive heatmap can also be opened directly via:
```text
tokyo_airbnb_heatmap.html
```

---

## Project Structure
```text
tokyo-airbnb-analysis/
├── README.md
├── .gitignore
├── notebooks/
│   └── airbnb_eda.ipynb
└── tokyo_airbnb_heatmap.html
```
---

## Notes

This project emphasizes real-world data interpretation and business-oriented analysis rather than predictive modeling.

It serves as a foundation for further extensions, such as:
- demand forecasting
- location optimization
- pricing strategy analysis
- interactive dashboard development (e.g. Streamlit or Plotly)

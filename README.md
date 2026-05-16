# 🏡 Data-Driven Airbnb Hosting Intelligence: Pricing, Occupancy & Neighborhood Analytics

Analyzed San Diego Airbnb listings, calendar, and review data to uncover pricing patterns, seasonal fluctuations, and neighborhood-level demand. Identified key amenity and local host effects on ratings and booking rates, equipping hosts with actionable revenue strategies and guiding investors toward high-profitability markets.

---

## 📌 Overview

This project analyzes **San Diego Airbnb market data** across three datasets: Listings, Calendar, and Reviews to surface actionable hosting strategies and investment insights. Using Python-based EDA, NLP, and geospatial analysis, we investigated how pricing, amenities, seasonality, and neighborhood dynamics drive occupancy and guest satisfaction.

---

## 🎯 Project Objectives

| # | Objective |
|---|-----------|
| 1 | Assess Airbnb hosting strategies across diverse San Diego neighborhoods through data analysis |
| 2 | Uncover patterns in listing prices, occupancy rates, and the influence of amenities on revenue |
| 3 | Evaluate seasonality, local events, and neighborhood effects on demand and profitability |
| 4 | Equip hosts with actionable strategies for optimizing pricing and enhancing guest experience |
| 5 | Guide investors toward high-demand neighborhoods for profitable short-term rental investments |

---

## 📊 Dataset

- **Source:** [Inside Airbnb](https://insideairbnb.com/get-the-data) — San Diego, California, USA
- **Datasets Used:**

| Dataset | Description |
|---------|-------------|
| **Listings** | Detailed data on individual listings including price, bedrooms, amenities, host info, and ratings |
| **Calendar** | Daily availability and pricing for each listing over a specified time period |
| **Reviews** | Guest reviews per listing including date, reviewer info, and review text |

---

## 🔍 Key Insights

1. **Keyword Association with Review Scores & Popularity**: NLP analysis of review text to identify language patterns correlated with high ratings and booking frequency
2. **Neighborhood Influence on Prices & Availability**: Geospatial analysis revealing which San Diego neighborhoods command premium pricing and higher occupancy
3. **Seasonal Fluctuations in Listing Prices**: Calendar data analysis exposing demand cycles and optimal pricing windows across quarters
4. **Effect of Amenities on Average Ratings**: Quantified the impact of specific amenities (WiFi, parking, pool, etc.) on guest satisfaction scores
5. **Impact of Local Hosts on Booking Rates & Review Scores**: Compared local vs. non-local host performance on key revenue and experience metrics

---

## 🏗️ Analysis Pipeline

```
Raw Data (Listings + Calendar + Reviews)
        │
        ▼
  Data Cleaning & Preprocessing
  (Null handling, type conversion, price parsing)
        │
        ├──────────────────────────────────┐
        ▼                                  ▼
Structured Analysis                   NLP Analysis
(Pricing, Occupancy,                  (Review Text →
 Amenities, Seasonality)               Word Cloud, CountVectorizer,
        │                               Keyword-Rating Correlation)
        ▼                                  │
Geospatial Mapping                         │
(Folium + MarkerCluster)  ◄────────────────┘
        │
        ▼
  Insights & Visualizations
  (Matplotlib, Word Cloud, Interactive Maps)
```

---

## 📁 File Structure

```
├── notebooks/
│   ├── 01_data_exploration.ipynb          # EDA across all three datasets
│   ├── 02_pricing_seasonality.ipynb       # Calendar-based price trend analysis
│   ├── 03_neighborhood_analysis.ipynb     # Geospatial pricing & availability maps
│   ├── 04_amenity_impact.ipynb            # Amenity effect on ratings & revenue
│   └── 05_review_nlp.ipynb                # Keyword association & word cloud analysis
├── data/
│   ├── listings.csv
│   ├── calendar.csv
│   └── reviews.csv
├── visuals/
│   └── maps/, charts/, wordclouds/
├── requirements.txt
└── README.md
```

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Data Processing | Python, Pandas, NumPy |
| Visualization | Matplotlib, WordCloud |
| Geospatial | Folium, Folium MarkerCluster |
| NLP | sklearn CountVectorizer, WordCloud |
| Date/Time Analysis | datetime |
| Environment | Jupyter Notebook |

---

## ⚙️ Setup & Installation

```bash
# Clone the repository
git clone https://github.com/your-username/airbnb-host-strategy.git
cd airbnb-host-strategy

# Install dependencies
pip install -r requirements.txt

# Launch notebooks
jupyter notebook
```

---

## 💡 Key Takeaways

- **Hosts** can optimize pricing by aligning with seasonal demand windows and prioritizing high-impact amenities that directly correlate with 5-star ratings
- **Investors** can use neighborhood-level availability and pricing heatmaps to identify underserved, high-demand areas in San Diego
- **Local hosts** consistently outperform non-local hosts on review scores and booking rates, signaling the value of personalized guest engagement
- **Review language** is a strong leading indicator of occupancy listings with positive keyword clusters around cleanliness and location see measurably higher booking rates

---

## 🔭 Future Work

- Expand analysis to additional cities for cross-market comparison
- Build a **dynamic pricing recommendation engine** using ML regression models
- Integrate **external event data** (concerts, conferences, holidays) to quantify local event impact on demand spikes
- Deploy an **interactive Streamlit dashboard** for hosts to simulate pricing strategies in real time

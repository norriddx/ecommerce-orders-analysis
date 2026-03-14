# Olist E-Commerce: Exploratory Data Analysis (EDA)

Exploratory analysis of ~100k Brazilian e-commerce orders (revenue, delivery, customer satisfaction and payments).

## Dataset

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) – 8 related tables covering orders, products, customers, sellers, reviews, payments and geolocation (2016-2018).

## Tools

Python, pandas, seaborn, matplotlib

## Project structure
```
ecommerce-orders-analysis/
├── data/                 # CSV files (8 tables + category translation)
├── notebooks/
│   └── eda.ipynb         # Main analysis notebook
├── README.md 
└── requirements.txt
```

## Key findings

**Revenue:** health_beauty leads by revenue, bed_bath_table by order count. watches_gifts ranks 2nd by revenue despite being 6th by orders – driven by the highest average check (~201). No correlation between average check and customer state.

**Seasonality:** No clear seasonal pattern. Order growth from 2017 to 2018 reflects Olist's platform growth. Some category-level trends exist (computers_accessories peaks early in the year, sports_leisure declines mid-year) but incomplete 2018 data limits conclusions.

**Delivery:** Olist overestimates delivery time – orders arrive faster than promised. Most sellers are in SP, so remote northeastern states wait longer. Top states by late delivery share: AL (22%), MA (18%), SE, PI, CE (~14%). All are geographically remote.

**Customer Satisfaction:** Delivery time is the strongest driver of 1-star reviews (5-10% at 0-10 days vs 70-100% at 50+ days). Every order status other than 'delivered' has over 50% negative reviews. Product category and payment method have no effect on scores.

**Payments:** Credit card dominates (74%), boleto second (19%). Installments are credit card only, mostly 1-5 payments. Higher order values correlate with more installments. computers_accessories has unusually high boleto usage.

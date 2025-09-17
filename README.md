# Loan-Credit-Card-Prediction

## 📌 Project Overview  
This project provides a **comprehensive analysis of a financial dataset**. The focus is on constructing a robust **basetable** for predictive modeling, applying systematic **data processing, feature engineering, and exploratory analysis** to extract insights.  

The predictive tasks are:  
- **Whether a client was granted a loan in the dependent variable time window (1997).**  
- **Whether a client (owner or disponent) was issued a credit card in the dependent variable time window (1997).**  

---

## 📂 Basetable Variables  
The basetable contains **100+ engineered variables**, covering:  

- **Account features** – account opening year, length of relationship (LOR), frequency of statements.  
- **Loan features** – loan amount, duration, payments, status, and categorized bins.  
- **Transaction features** – monthly averages, total credits/withdrawals, balance change, spending flag, credit-to-withdrawal ratio.  
- **Order features** – household, loan, insurance, leasing, and other orders (amounts, counts, and flags).  
- **Card features** – card issuance dates, type, LOR of card, card flags (2016–2017).  
- **Client & demographic features** – age, gender, region, salary categories, unemployment rates, crime data, economic scores.  

---

## ⚙️ Data Transformation  
Extensive preprocessing was performed, including:  

- **Account data**: date conversion, frequency mapping, LOR calculation.  
- **Disposition data**: aggregation of unique client IDs, filtering for account owners.  
- **Card data**: merging with client roles, card LOR, issuance filtering.  
- **Loan data**: standardized columns, categorization by payment and amount.  
- **Transactions**: monthly averages, balance change, spending flags, aggregated totals.  
- **Orders**: aggregation by type, creation of flags for each order category.  
- **District & client data**: demographic categorization, salary bands, crime bins, economic score, age groups, gender encoding.  

---

## 📊 Analysis & Insights  

### 🔹 Feature Selection  
Used **correlation matrix + feature importance** to avoid overfitting.  

- **Loan model key features**: LOR of Account, Spending Flag, Balance Change, Age Group, Average Salary Category, Loan Flag 2016, Card Flag 2016, Household Flag.  
- **Credit card model key features**: Average Salary Category, Balance Change, Age Group, Spending Flag, Inhabitant Category, Gender.  

### 🔹 Key Findings  
- **Demographic effects** – Salary and crime highly correlated; crime excluded to avoid redundancy. High-salary groups showed higher loan and credit card approvals.  
- **Age & Gender** – Age groups showed strong predictive power (30s for loans, 50s for cards). Gender had little effect due to even distribution.  
- **Household Orders** – Middle-aged groups (40s–60s) had the highest salaries and household orders, influencing approval likelihood.  
- **LOR (Length of Relationship)** – Cards were often issued within the first year of opening an account, despite longer relationships being more common.  
- **Balance Change & Spending Flag** – Over 56% of clients ended 1996 with higher balances; positive spending behavior was strongly linked to approvals.  
- **2016 Loan & Card Flags** – Only a small proportion (8–13%) had existing loans/cards in 2016, and none of these opened new ones in 2017.  

---

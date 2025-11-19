# Enterprise Sales Performance – Power BI Dashboard

This repository contains a Power BI report that analyzes enterprise-wide sales performance, targets, and sales representative efficiency.  
The project is built using a star-schema model with separate dimension and fact tables and includes Row-Level Security (RLS) for regions and sales reps.

---

## 🔍 Project Overview

**Goal:** Provide executives and sales leadership with a consolidated view of:

- Overall sales performance vs. targets  
- Regional performance and variance  
- Sales representative performance with drill-through to rep-level details  
- Product & category insights (pricing vs volume, channel mix)  

---

## 📂 Repository Structure

```
.
├─ README.md
├─ .gitignore
│
├─ pbix/
│   └─ Enterprise Sales Dashboard.pbix
│
├─ data/
│   ├─ dim_channel.csv
│   ├─ dim_customer.csv
│   ├─ dim_date.csv
│   ├─ dim_product.csv
│   ├─ dim_region.csv
│   ├─ dim_salesrep.csv
│   ├─ fact_sales.csv
│   ├─ fact_targets.csv
│   ├─ sec_user_region.csv
│   ├─ sec_user_rep.csv
│   └─ bridge_rep_region.csv
│
└─ docs/
    ├─ measures.md
    └─ rls_setup.md
```

---

## 🧱 Data Model

Star schema with:

- fact_sales  
- fact_targets  
- dim_date  
- dim_customer  
- dim_product  
- dim_channel  
- dim_region  
- dim_salesrep  
- bridge_rep_region  
- security tables used for RLS  

---

## 📊 Report Pages

- Executive KPIs  
- Forecast vs Actual  
- Sales Rep Performance  
- Sales Rep Details (Drill-through)  
- Product & Category Analysis  
- Mobile Layout  

---

## 🔐 Row-Level Security (RLS)

### RegionalManager Role

```
sec_user_region[UserEmail] = USERPRINCIPALNAME()
```

### SalesRep Role

```
sec_user_rep[UserEmail] = USERPRINCIPALNAME()
```

---

## 🧮 Key Measures (DAX)

Includes KPIs such as:

- Total Sales  
- MoM %  
- Rolling 3M Sales  
- Target Attainment %  
- Variance %  
- Category sales measures  
- Product & channel insights  

---

## 🚀 How to Use

1. Clone or download the repository  
2. Add your CSVs into the `/data` folder  
3. Open the `.pbix` file from `/pbix`  
4. Test roles using `Modeling → View as`  

---

## 📌 Designed For

- Executive decision-making  
- Sales performance monitoring  
- BI & analytics portfolios  
- Power BI learning and demonstration  


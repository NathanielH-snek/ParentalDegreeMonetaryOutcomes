# Effects of Parental Degrees on Degree Selection Outcomes

Analyzes how parental education levels influence college students’ choice of financially valuable degree majors.

---

## 🔍 Overview

This project investigates whether students with more highly educated parents are more likely to choose financially valuable college degrees (e.g., STEM or Business). 

- It addresses the gap in educational research on how **specific combinations** of parental education levels (by gender) influence students’ **degree selection**, beyond just performance or attainment.
- This is a data science/statistical learning project based on the **2021 National Survey of College Graduates**.
- It was designed as an academic exploration and a causal inference exercise using **mediation analysis**.

---

## 🛠️ Tech Stack

- R (Base, Tidyverse, skimr, dagitty, mediation, MatchIt, cem, cobalt, GGally)
- National Survey of College Graduates (2021)
- CSV / fixed-width data parsing
- DAGs and causal inference tools

---

## 🚀 Features

- Constructs a directed acyclic graph (DAG) to model mediation pathways
- Implements **Coarsened Exact Matching (CEM)** to balance treatment groups
- Performs **causal mediation analysis** to assess indirect and direct effects
- Visualizes results and checks matching quality using **love plots**
- Categorizes degree fields and parental education into interpretable metrics

---

## 📁 Project Structure

```
├── data_layout.csv            # Fixed-width column definitions
├── EPCG21.DAT                 # Raw NSCG data
├── major_keys.csv             # Maps degree field codes to categories
├── Paper.qmd                  # Main R script performing all steps
├── README.md                  # This file
```

---

## 📈 Results

- **ACME (indirect effect via loans):** 0.00089  
- **ADE (direct effect of parental education):** 0.00631  
- **Total effect:** 0.00719  
- **Proportion mediated by loans:** ~12%  
- All effects are **statistically significant** but **substantively small**

> _These results suggest a small but significant influence of parental education on high-value degree selection, with minimal mediation through student loan amounts._

---

## 🧠 What I Learned

- Developed experience with **causal DAG modeling** and identifying valid adjustment sets
- Practiced **mediation analysis** in R using real-world educational survey data
- Learned the value and limitations of large-sample significance vs. practical impact
- Improved understanding of **Coarsened Exact Matching (CEM)** and balancing diagnostics

---

## 📦 Installation & Usage

To run the project:

```bash
# Clone the repo and move into it
git clone https://github.com/NathanielH-snek/ParentalDegreeMonetaryOutcomes.git
cd parental-education-degree-selection
```
Unzip files
Open RStudio
Install packages as prompted
Run all cells

> _Note: You must have access to the NSCG 2021 data (`EPCG21.DAT`) and the supporting `data_layout.csv` and `major_keys.csv` files._

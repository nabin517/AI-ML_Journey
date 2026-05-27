# Day 07: Bivariate and Multivariate Exploratory Data Analysis (EDA)

## Project Overview
This module focuses on Bivariate (comparing two variables) and Multivariate (combining three or more variables) analysis using the Titanic dataset. Moving past single-column summaries, this project focuses on layering demographic, economic, and family data together to discover deep interaction patterns, hidden context, and complex relationships before building predictive models.

## Visualizations Covered & Purpose

### 1. Simple Comparisons (Bivariate Analysis)
* **Gender Matters Most (`Sex` vs `Survived`):** The old saying "Women and children first" was completely true. About 74% of all women survived, while only 19% of men did.
* **Money Bought Safety (`Pclass` vs `Survived`):** First-class passengers had a massive advantage. The higher your ticket class, the more likely you were to make it out alive, mostly because their cabins were closer to the top decks.
* **The Boarding Port Trick (`Embarked` vs `Survived`):** People who hopped on the ship at Cherbourg had a much higher survival rate than other ports. But here is the trick: it wasn't the city that saved them. It turns out a huge chunk of the rich, first-class passengers boarded there.
* **Protecting the Kids (`Age` vs `Survived`):** When looking at age, toddlers and young kids (ages 0–5) survived at a much higher rate than any other age group. On the flip side, older passengers had a very hard time escaping.
* **The Rich Outliers (`Fare` vs `Survived`):** Most people who died paid very cheap fares (under \$20). However, the data shows a few "outlier" passengers who paid crazy high prices (up to \$512) for luxury suites. Every single one of them survived.

### 2. Combining the Factors (Multivariate Analysis)
* **Gender beat Wealth (`Pclass` + `Sex` vs `Survived`):** What happens when you compare a poor woman to a rich man? The data shows that poor women in 3rd class still survived at a higher rate (~50%) than wealthy men in 1st class (~36%). Being female gave you a better chance than being rich, though rich women still had the absolute best survival rate (nearly 100%).
* **The Ultimate Shield (`Age` + `Fare` vs `Survived`):** If you paid a high fare (over \$100), your age didn't matter—young or old, you almost certainly lived. The most dangerous situation was being an adult who bought a cheap ticket. Poor kids, however, were still rescued at a high rate.
* **The Large Family Trap (`SibSp` + `Fare` vs `Survived`):** Traveling with a spouse or 1–2 siblings was relatively safe if you had money. But truly large families (4 to 8+ members) were almost all in 3rd class, and sadly, almost none of them survived. In the panic and chaos, keeping a massive family together in the lower decks was logistically impossible.

## Repository Structure

AI-ML_Journey/
└── Day-07_Bivariate-Multivariate-EDA/
    └── README.md               # Advanced EDA documentation (this file)
    └── titanic_eda.ipynb       # Jupyter Notebook with bivariate & multivariate analysis

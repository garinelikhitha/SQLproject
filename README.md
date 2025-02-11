# 📊 COVID-19 Data Analysis Project  

This project explores COVID-19 data using **SQL** to analyze key trends, including infection rates, death rates, and vaccination progress across different countries and continents. The dataset is sourced from **Our World in Data** and is structured in **SQL Server**.  

## 📌 Project Overview  
The project aims to answer important questions, such as:  
✅ What is the likelihood of dying from COVID-19?  
✅ What percentage of the population was infected in each country?  
✅ Which countries and continents had the highest infection and death rates?  
✅ What percentage of the population received at least one vaccine dose?  

## 🗂️ Dataset Used  
We use two main tables:  
- **CovidDeaths** – Contains data on cases, deaths, and population.  
- **CovidVaccinations** – Contains data on vaccination progress.  

## 🛠️ SQL Queries and Insights  
The following SQL queries were used for analysis:  
- **Total Cases vs Total Deaths** – Calculates the death percentage for each country.  
- **Total Cases vs Population** – Determines the infection rate per country.  
- **Highest Infection Rates** – Finds countries with the highest infections compared to their population.  
- **Highest Death Counts** – Identifies countries and continents with the most COVID-19 deaths.  
- **Global Trends** – Aggregates worldwide cases, deaths, and fatality rates.  
- **Vaccination Analysis** – Tracks the percentage of the population that received at least one dose.  

## 🔍 Key SQL Features Used  
- **Aggregate Functions** (`SUM()`, `MAX()`, `AVG()`)  
- **Window Functions** (`OVER(PARTITION BY ...)`)  
- **Joins** (Combining `CovidDeaths` & `CovidVaccinations`)  
- **CTEs & Temp Tables** for efficient data processing  
- **Views** for storing data for visualization  

## 📊 Visualization & Insights  
The processed data can be used for visualization in **Power BI, Tableau, or Python (Matplotlib/Seaborn)**.  

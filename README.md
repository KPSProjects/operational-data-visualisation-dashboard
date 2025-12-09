# Video Game Sales & Popularity Trends — Data Visualisation Project

This repository contains my submission for the CM4125 Data Visualisation coursework at Robert Gordon University.  
The project examines global video game sales, platform performance, genre trends, and modern Steam metadata to produce a clear, well-designed infographic summarising insights across multiple decades.

---

## Project Aim

The aim of this project is to:

- Explore how video game popularity has evolved from the 1980s to 2024  
- Compare historic physical retail sales with modern digital platform data  
- Identify dominant genres, platforms, and top-selling games  
- Communicate insights through a clean, unbiased infographic  

The project demonstrates the full data visualisation pipeline: data acquisition, cleaning, transformation, aggregation, and final visual design.

---

## Datasets Used

Four independent datasets were used:

1. **vgsales.csv**  
   Historic video game sales across platforms.

2. **best_selling_video_games_of_all_time.csv**  
   Lifetime sales figures for top-selling games.

3. **steam.csv**  
   Steam game metadata including release dates, genres, and metrics.

4. **steamspy_tag_data.csv**  
   SteamSpy tag data for analysing common gameplay themes.

These datasets together represent both the retail era and digital distribution era of gaming.

---

## Data Processing & Methods

All data processing was performed in Python using Pandas inside the Jupyter notebook  
`Data_Viz_Program.ipynb`.

### Data Cleaning
- Converted year, date, and sales fields to numeric or datetime types  
- Dropped rows missing critical identifiers (Name, Year, Genre, Platform)  
- Removed invalid or unreasonable records (e.g., sales <= 0 or invalid Steam dates)

### Feature Engineering
- Created a `Decade` column from `Year`  
- Added a `Sales_Category` column by binning global sales into categories  
- Extracted `Year` from Steam release dates  
- Normalised game names to create a merge key (`Name_key`)  
- Transformed SteamSpy tag data into long format for frequency analysis

### Row Handling
- Removed rows lacking essential data  
- Cleaned date fields using `errors="coerce"` and dropped invalid entries  
- Ensured datasets only included meaningful observations for analysis

### Dataset Merging
- Merged VGSales with the Best-Selling Games dataset using the engineered `Name_key`  
- Steam datasets were analysed separately due to incompatible identifiers

### Aggregation
Produced aggregated summaries for:

- Top 10 games by global sales  
- Top 10 genres  
- Top 10 platforms  
- Global sales by decade and genre  
- Steam games released per year  
- Most frequent Steam tags  

These results were used to construct the infographic’s number stories.

---

## Final Infographic

A high-resolution static infographic produced from the cleaned and aggregated data is included in this repository.

**Infographic link:**  
*(Insert your GitHub image link here after uploading the PNG)*

The infographic visualises major trends such as genre dominance, platform growth, top-selling titles, decade shifts, and Steam ecosystem patterns.

---

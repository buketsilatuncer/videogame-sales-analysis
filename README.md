**Video Game Sales Data Analysis**

I've created this project to demonstrate an end-to-end data analytics workflow using a dataset sourced from Kaggle, loaded into Google BigQuery, processed with SQL, and visualized in Power BI.

> **1. Data Source**

**Data Source:** Kaggle

The dataset was already mostly clean, with only minor formatting adjustments applied.

Original dataset link: [Click here](https://www.kaggle.com/code/upadorprofzs/eda-video-game-sales)

> **2. Upload to BigQuery**

The dataset was uploaded to Google BigQuery.

Steps completed:

- BigQuery automatically detected the schema

- Dataset and table structure were created

- Data types were verified

> **3. SQL Cleaning & Transformation**

Data cleaning and transformation were performed directly in BigQuery.

Main operations included:

Dropping unnecessary columns

Checking for null values

Eliminating N/A records

Code ran:

```
SELECT Name, Platform, Year, Publisher, SUM(Global_Sales) AS total_sales, NA_Sales, JP_Sales, EU_Sales, Genre
FROM alien-aileron-354922.moviedata.video_game_sales
WHERE Year != "N/A" 
GROUP BY Name, Publisher, Year, Platform, NA_Sales, JP_Sales, EU_Sales, Genre
ORDER BY total_sales, Year DESC 
```


> **4. Visualization in Power BI**

Visuals created:

Time-series charts

Category distributions

Interactive filters and slicers

The dashboard highlights the dataset’s key insights and trends.

> **5. Project Structure**

```
📁 videogame-sales-analysis
─ README.md
─ Video Game Sales Dashboard.SemanticModel/
─ Video Game Sales Dashboard.Report/
─ Video Game Sales Dashboard.pbip
─ .gitignore
```

> **6. Tools & Technologies**

Kaggle

Google BigQuery

SQL

Power BI


> **7. Key Insights**

Data between the years of 1980 to 2020 was analysed for this project. My analysis revealed that North America's sales were leading in terms of sales volume, followed by EU and Japan. 2008 was the year of the highest total sales volume, rivaled by 1980, which was the lowest within the dataset. Action was the most popular genre, followed by sports and shooter games.
Top 3 platforms were PS2, X360 and PS3 overall, though more recent years included Wii in this category as well. Overall, the most popular game publishers were Activision, Electronic Arts and Nintendo. It's also visible that average total sales increases when the publisher is Nintendo. 
Each platform and publisher have their own strengths in terms of genre reflected in their sales volume. Since the created dashboard is dynamic, different interpretations based on date range, platform, publisher and genre can be performed.

📎 8. Contact

For questions or suggestions:

Buket Sıla Tuncer
[Find my LinkedIn profile here](https://www.linkedin.com/in/buket-s%C4%B1la-t-065b85149/)

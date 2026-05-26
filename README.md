# Video Game Sales Analysis

## Project Overview

This project presents a comprehensive analysis of the global video game industry using data visualization and exploratory data analysis techniques. The study investigates how platform choice, genre preferences, regional behavior, and publisher strategies influence the commercial success of video games.

The analysis is based on the VGChartz Global Video Game Sales dataset.

---

## Objectives

- Analyze the relationship between platforms, genres, and regional sales
- Examine factors influencing global video game success
- Study regional differences in gaming preferences
- Investigate Japan as a distinct gaming market
- Explore publisher dominance and market concentration
- Derive insights using visualization-driven analysis

---

## Dataset

The dataset used in this project is the VGChartz Global Video Game Sales dataset containing information such as:

- Game Title
- Platform
- Genre
- Publisher
- Release Year
- Regional Sales
- Global Sales

Regions included:
- North America
- Europe
- Japan
- Other Regions

---

## Calculated Fields

The following calculated fields were created in Tableau to support regional and publisher-level analysis.

### Publisher Type

Classifies publishers as Japanese or Foreign publishers.

```sql
IF [Publisher] = "Nintendo"
OR [Publisher] = "Konami Digital Entertainment"
OR [Publisher] = "Capcom"
OR [Publisher] = "Square Enix"
THEN "Japanese Publisher"
ELSE "Foreign Publisher"
END
```

---

### Difference

Measures the relative sales difference between Japan and North America.

```sql
(SUM([JP_Sales]) - SUM([NA_Sales])) / SUM([Global_Sales])
```

---

### Favour

Categorizes whether a game or genre is more favored in Japan or North America.

```sql
IF [Difference] > 0 THEN "JP Favored"
ELSE "NA Favored"
END
```

---

### JP Share

Calculates Japan's contribution to global sales.

```sql
SUM([JP_Sales]) / SUM([Global_Sales])
```

---

### EU Share

Calculates Europe's contribution to global sales.

```sql
SUM([EU_Sales]) / SUM([Global_Sales])
```

---

### NA Share

Calculates North America's contribution to global sales.

```sql
SUM([NA_Sales]) / SUM([Global_Sales])
```

---

## Tools and Technologies

- Tableau
- Python
- Pandas
- NumPy
- Matplotlib
- Exploratory Data Analysis (EDA)
- Data Visualization

---

## Key Analysis Areas

### 1. Platform Dominance and Sales Trends

- Platform-wise sales distribution
- Platform lifecycle analysis
- Genre-platform interactions

### 2. Regional Market Preferences

- Genre popularity across regions
- Regional divergence analysis
- Cross-regional appeal of genres

### 3. Japan as an Independent Market

- Japan vs Global sales comparison
- Regional outlier analysis
- Publisher origin influence

### 4. Winner-Takes-All Industry Structure

- Publisher revenue concentration
- Market dominance analysis
- Portfolio vs blockbuster strategy

---

## Key Insights

- Global success is primarily driven by North American and European markets
- Japan behaves as a distinct gaming ecosystem with unique preferences
- Platform and genre interactions significantly impact sales performance
- A small number of publishers dominate global revenue
- Success depends on the alignment of multiple factors rather than a single variable

---

## Visualizations Included

- Correlation Heatmaps
- Sales Distribution Plots
- Platform Market Share Trends
- Genre Comparison Charts
- Regional Analysis Dashboards
- Publisher Concentration Analysis

---

## Tableau Dashboard

Tableau Public dashboard link

```text
https://public.tableau.com/views/GlobalVideoGameSalesAnalysis_17792845537000/Hypothesis4?:language=en-GB&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
```

---

## Project Report

The detailed project report is available in:

```text
Project Report.pdf
```

---

## Team Members

- Saachi Garg
- Anusha Singh
- Jay Patel
- Keshav Gangwani

---

## Conclusion

This project demonstrates how interactive visualization and data-driven storytelling can uncover meaningful patterns in the gaming industry. The findings highlight the importance of regional alignment, platform strategy, and publisher dynamics in determining commercial success.

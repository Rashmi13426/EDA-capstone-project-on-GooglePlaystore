# Playstore EDA Project

## Overview
This project performs **Exploratory Data Analysis (EDA)** on the Google Playstore dataset to uncover insights about app categories, ratings, installs, and more. The goal is to clean, analyze, and visualize the data to better understand trends in the app ecosystem.

---

## Project Files
- `Rashmi_playstore_EDA_project.ipynb` → Google Colab with complete analysis and visualizations  
- `README.md` → Project documentation (this file)  

---

## Features
- Data cleaning and preprocessing  
- Handling missing values and outliers  
- Exploratory Data Analysis (EDA) with charts & plots  
- Insights about app categories, ratings, and installs  
- Visualizations with Matplotlib/Seaborn  

---

## Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Google Colab

## Data Cleaning and Insights:

- Removed misaligned row at Index 10472 where columns were misplaced from playstore data.
- Standardized Size column (converted to bytes), handling:
  * M → Megabytes
  * K → Kilobytes
  *  * Varies with device → replaced with NaN
   
 - Filled missing values:
   * Rating → filled with mean
   * Size_in_Bytes → filled with median

 - Cleaned Installs by removing + and converting to integer.
 - Cleaned Price by removing $ and converting to float.
 - Converted Reviews to integer.
 - Dropped rows with missing values in critical columns (Current Ver, Android Ver, and Type).

 - Out of 64k reviews, 26k were missing review text and corresponding sentiment values. These rows were dropped since they provide no meaningful insights for sentiment analysis. The cleaned dataset now contains ~38k valid reviews.


## Key Insights from EDA:

## Insights from Visualization 3: Paid vs Free Apps Installs(bar plot):
Free apps dominate installs: The median installs for free apps are far higher than paid apps.

## Insihghts from Visualization 5: Sentiment Analysis of Reviews(count plot):
- The majority of reviews are positive, showing that users are generally satisfied with Play Store apps.
- A significant number of negative reviews exist, highlighting areas for improvement such as bugs, ads, or performance issues.
- Neutral reviews are fewer, suggesting that most users express clear opinions rather than indifference.

## Insights from Visualization 7: Top 10 Installed Apps(bar plot):
- Subway Surfers is the standout, crossing 6 billion installs, ahead of other major apps.
- Google’s own ecosystem apps — Drive, Photos, News, Maps, Hangouts — are strongly represented, proving the success of cross-platform integration.
- Social and Communication apps (Instagram, Messenger, WhatsApp) continue to dominate user attention, indicating their importance in daily engagement.

## Insights from Visualization 9: Correlation Heatmap
Reviews ↔ Installs (0.64): Strong positive correlation — more installs lead to more reviews, which is logical since a bigger user base creates more engagement.

## Insights from Visualization 10: Price Distribution of Paid Apps Only(histplot):
- Most paid apps are priced very low (under $10).
- There are very few apps priced above $20, and they form long-tail outliers.
- The distribution is highly skewed → majority of developers avoid premium pricing.
Suggests a “race-to-the-bottom” pricing strategy in app stores, where affordability drives adoption.

## Insights from Chart - 11: Distribution of App Ratings(histogram):
Most apps are rated between 4.0 and 4.5, which suggests that the majority of users are generally satisfied.

## Insights from Chart - 12: Top 15 App Categories by Total Installs(bar plot):
Game, Communication, and Tools dominate with the highest total installs. This shows where user engagement and demand are concentrated.

## Visualization Techniques

* Bar Charts:  Category distribution, top apps, missing values
* Histograms:  Ratings, installs, reviews, app sizes
* Boxplots:  Ratings, installs, reviews by category/type
* Scatter Plots:  Correlations between key metrics
* Heatmaps:  Correlation analysis of numeric features

## Project Environment

This project was developed and executed in **Google Colab**.  
All notebooks, data analysis, and visualizations were created using Python libraries such as pandas, matplotlib, seaborn, and plotly within the Colab environment.






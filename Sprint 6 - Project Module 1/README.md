# Video games analysis for marketing purposes | Project 6 - Tripleten
This project was part of my Data Scientist bootcamp at Tripleten

## Introduction
This project focuses on analyzing historical video game sales data from the fictional online store "Ice" to predict trends that could determine the success of an advertising campaign for the next year. Our dataset comprises user and expert reviews, genres, platforms (e.g., Xbox or PlayStation), and sales data from various regions, up to December 2016.

## Tasks
### 1. Data preparation
- The data was imported and loaded into a DataFrame. Several missing values were treated accordingly.
- A new column called 'total_sales' was added to sum up all the sales from the different regions for each video game.

### 2. Data Analysis
Aspects of the data were examined:

- Distribution of games released per year
- Distribution of games released per platform
- Total sales per year for each platform
- User rating correlation with total sales
- Critic rating correlation with total sales
- Analyzed the popularity of platforms in each region

Visual representations were created for the above analyses, including bar charts, scatter plots, boxplots, and pie charts.

### 3. Hypothesis testing
Two hypotheses were tested:

1. Average user ratings of the Xbox One and PC platforms are the same.
   - Rejected the null hypothesis for the first, suggesting the average user ratings for Xbox One and PC are different.
2. Average user ratings for the Action and Sports genres are different.
   - Failed to reject the null hypothesis for the second, suggesting no significant difference in average user ratings between Action and Sports genres.

### 4. Conclusion
After analyzing all the data, we are now ready to plan a targeted marketing campaign. If our objective is to allocate a marketing budget to drive additional sales, we could assign it to the PS4 platform, as it is the console showing consistent growth and has the highest sales potential in the NA, EU, and Other regions. We could also increase advertising for Action games with an M rating, as they represent a strong opportunity for additional revenue.

On the other hand, for the JP region, we may consider a different campaign strategy, since the 3DS platform performs best in this market. Action games also show strong potential in this region, so increasing advertising for titles within this genre could help boost sales.

These represent the most relevant conclusions we can draw from the current dataset. However, if we are asked about a specific game, we will now be able to assess its sales success probability and provide a recommendation backed by data.

# Accenture-Data-Analytics-and-Visualization

A free job simulation on Forage. All credits go to Accenture. Check out the simulation here: https://www.theforage.com/simulations/accenture-nam/data-analytics-mmlb

# Category Analysis and Visualization

This project analyzes and visualizes data related to various categories based on user reactions. The goal is to clean, process, and visualize the data to identify trends and insights, such as the top-performing categories and the distribution of scores.

## Project Overview

The project involves:
1. **Data Cleaning**: Processing raw data to prepare it for analysis.
2. **Data Merging**: Combining multiple datasets to create a comprehensive view.
3. **Data Aggregation**: Summarizing data to determine key insights.
4. **Visualization**: Creating charts to represent data in a meaningful way.

## Data Files

1. **Reactions.csv**: Contains user reactions with columns `Content ID`, `User ID`, `Reaction Type`, and `Datetime`.
2. **ReactionTypes.csv**: Contains details about reaction types with columns `Type`, `Sentiment`, and `Score`.
3. **Content.csv**: Contains content details with columns `Content ID`, `User ID`, `Content Type`, `Category`, and `URL`.

## Data Processing

### Steps Taken:

1. **Renaming Columns**:
   - Renamed 'Type' to 'Reaction Type' in `Reactions` and 'Type' to 'Content Type' in `Content`.

2. **Cleaning Data**:
   - Removed quotations from the 'Category' column in `Content`.
   - Dropped rows with missing 'Reaction Type' values in `Reactions`.
   - Removed 'User ID' and 'URL' columns from `Content` and `Reactions`.

3. **Merging Datasets**:
   - Merged `Reactions` with `Content` on 'Content ID'.
   - Merged the resulting dataset with `ReactionTypes` on 'Reaction Type'.

4. **Aggregation and Visualization**:
   - Aggregated scores for each category.
   - Grouped the lowest 10 categories under the label 'Others'.
   - Created a pie chart to visualize the proportion of scores for each category.

## Analysis

### Key Insights:

1. **Number of Unique Categories**:
   - Total count of distinct categories.

2. **Reactions to the Most Popular Category**:
   - Number of reactions associated with the most popular category.

3. **Month with the Most Posts**:
   - Identified the month with the highest number of posts.

### Pie Chart

- **Description**: Displays the proportion of scores for each category, with the lowest 10 categories combined under 'Others'.

## Dependencies

- `pandas`
- `matplotlib`

## Acknowledgments

This project was part of a free job project simulation offered by Accenture on Forage.

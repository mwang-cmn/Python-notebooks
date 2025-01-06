## Investigating Goal Scoring Trends in Men's and Women's FIFA World Cup Matches

#### Project Overview

This project investigates whether more goals are scored in women's FIFA World Cup matches compared to men's. The analysis focuses exclusively on official FIFA World Cup matches (excluding qualifiers) since January 1, 2002. By applying statistical hypothesis testing, we aim to provide data-driven insights into scoring patterns in international soccer.

**Hypotheses**

Null Hypothesis (H₀): The mean number of goals scored in women's international soccer matches is the same as in men's.

Alternative Hypothesis (H₁): The mean number of goals scored in women's international soccer matches is greater than in men's.

Datasets

The datasets used for this analysis were scraped from a reliable online source and contain results of official international soccer matches:

women_results.csv: Contains results of women's matches.

men_results.csv: Contains results of men's matches.

Dataset Structure

Both CSV files have the following columns:

date: Date of the match.

team_1: Name of the first team.

team_2: Name of the second team.

goals_1: Goals scored by the first team.

goals_2: Goals scored by the second team.

tournament: Name of the tournament.

Methodology

Data Preprocessing

Filtered the datasets to include only matches played on or after January 1, 2002.

Selected matches from FIFA World Cup tournaments (excluding qualifiers).

Calculated the total number of goals scored per match by summing goals_1 and goals_2.

Statistical Tests

Levene's Test: Assessed the equality of variances between men's and women's datasets.

p-value: 0.3411 (no significant difference in variances).

Shapiro-Wilk Test: Tested for normality of the goal distributions.

Women's p-value: 3.89e-13 (not normal).

Men's p-value: 8.89e-13 (not normal).

One-Tailed T-Test: Compared the mean goals scored in men's and women's matches.

p-value: 0.0051 (statistically significant difference).

Results

The null hypothesis was rejected at the 10% significance level.

There is strong evidence that the mean number of goals scored in women's FIFA World Cup matches is greater than in men's matches.

Conclusion

The analysis suggests that women's FIFA World Cup matches are, on average, higher scoring than men's. This finding highlights intriguing differences in scoring patterns that could stem from various factors, such as tactical approaches, game dynamics, or defensive strategies.

How to Run the Analysis

Install the required Python libraries:

pip install pandas scipy matplotlib seaborn

Run the analysis script (available in analysis_notebook.ipynb or analysis_script.py).

Review the output, including statistical test results and visualizations.

Visualizations

Histograms and boxplots comparing the distribution of goals in men's and women's matches.

Summary statistics for both datasets.

Limitations

The analysis only includes World Cup matches since 2002, excluding qualifiers.

Potential confounding factors (e.g., regional differences, tournament format) are not considered.

Future Work

Expand the analysis to include other tournaments and qualifiers.

Investigate temporal trends in scoring patterns over different World Cup editions.

Explore other aspects of match statistics, such as possession, shots on target, or fouls.

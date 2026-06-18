# Lecture 10: 
AQ1 – Descriptive Statistics for turns and rating_diff

The dataset contains 20,058 chess games.

Turns

The average game length is approximately 60.5 turns, with a median of 55 turns. The standard deviation is 33.6 turns, indicating substantial variation in game length. Half of all games contain between 37 and 79 turns. The shortest game lasted only 1 turn, while the longest reached 349 turns, suggesting the presence of some extreme values and a right-skewed distribution.

Rating Difference

The average rating difference between players is 7.8 points, while the median is 3 points, indicating that most games involve players with similar ratings. The standard deviation is 249 points, showing considerable variability across matches. The middle 50% of games have rating differences between −108 and 122 points. The minimum and maximum values (−1605 and 1499) reveal a small number of matches with very large rating gaps.
AQ2 – Distribution Analysis of Chess Game Turns

The distribution of turns was examined using histograms, skewness, and the Shapiro–Wilk normality test.

The original distribution was positively skewed (skewness = 0.897), with a long right tail caused by a small number of exceptionally long games. A log transformation was applied to reduce this skewness.

After transformation, the distribution became more compact and visually closer to a bell shape. However, the skewness changed to −1.371, indicating that the transformation over-corrected the original right skew and introduced left skewness.

The Shapiro–Wilk test produced extremely small p-values for both distributions (original: p = 2.25 × 10⁻³⁴, transformed: p = 5.00 × 10⁻⁴⁷), providing strong evidence against normality.
AQ3 – WHO Correlation Analysis

A correlation matrix was computed using the numerical variables in the WHO Life Expectancy dataset.

The three variables most positively correlated with life expectancy were:

Schooling (r ≈ 0.75)
Income composition of resources (r ≈ 0.72)
BMI (r ≈ 0.57)

These results suggest that countries with higher education levels, stronger economic resources, and better nutritional status tend to have higher life expectancy.

Confounder Discussion

A potential confounder is Income Composition of Resources. Wealthier countries generally provide better education, healthcare, sanitation, and nutrition. As a result, part of the observed relationship between schooling and life expectancy may actually be driven by overall economic development rather than education alone.

Therefore, correlation does not imply causation, and the observed associations should be interpreted carefully.
AQ4 – Chi-Squared Test: Rating Group vs Winner

A chi-squared test of independence was conducted to examine whether game outcomes are associated with player rating groups.

The test produced a highly significant result (p = 1.29 × 10⁻⁷⁹), indicating that rating group and game outcome are not independent. Therefore, the distribution of winners differs across rating groups.

To assess practical significance, Cramér's V was calculated and yielded a value of 0.098. This represents a very small effect size, suggesting that although the relationship is statistically significant, its practical strength is weak.
AQ5 – Confidence Intervals for Rated vs Unrated Games

A 95% bootstrap confidence interval was calculated for the mean number of turns in rated and unrated chess games.

For rated games, the 95% confidence interval was [61.43, 62.50] turns. For unrated games, the 95% confidence interval was [53.20, 55.30] turns.

The intervals do not overlap, indicating a clear difference in average game length between the two groups. Rated games consistently last longer than unrated games by approximately 7–9 turns on average.

Conclusion

- Most chess games in the dataset are moderately long, with a typical length of around 55–60 turns. Player ratings are generally balanced, although a few games involve opponents with substantially different skill levels.
- The turns variable is not normally distributed. Although the log transformation changed the shape of the distribution, it did not achieve normality and may not be necessary for subsequent analyses.
- There is a statistically significant association between rating group and game outcome (p < 0.001), but the effect size is very small (Cramér's V = 0.098). Rating group influences outcomes, though the magnitude of this influence is limited.
- Rated chess games tend to be longer than unrated games, and the confidence intervals provide strong evidence that this difference is statistically meaningful and not due to random variation.
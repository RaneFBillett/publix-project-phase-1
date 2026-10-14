# Evaluating the Evaluations: A Longitudinal Sentiment Analysis of Publix Employee Discussions

## Overview

Is sentiment toward Publix employee evaluations getting worse over time?

This project investigates that question by analyzing public discussions on Reddit's r/Publix community across four years: 2021, 2023, 2025, and 2026. The goal was to explore whether employee discussions showed a consistent shift toward more negative sentiment, rather than relying on individual experiences alone.

## Methodology

I collected and validated 64 Reddit parent posts from July 25 through August 10 of each study year. After excluding four deleted posts with no usable text, I analyzed 59 posts using **Python and VADER**, a sentiment analysis tool designed for social media text.

The analysis compared sentiment scores, positive/neutral/negative classifications, and changes over time. I also calculated 95% confidence intervals to assess uncertainty around yearly average sentiment scores.

## Key Findings

- **60 posts analyzed** across four study years.
- **29 positive, 17 negative, and 13 neutral** sentiment classifications overall.
- Average sentiment increased from **0.134 in 2021 to 0.275 in 2026** on VADER's scale of -1 to +1.
- The percentage of negative posts also increased, from **21.4% in 2021 to 28.6% in 2026**.
- Sentiment varied considerably between years, with 2023 showing a less positive pattern than 2025 and 2026.

**Conclusion:** The findings do not establish a consistent worsening trend. Although the share of negative posts increased between 2021 and 2026, average sentiment also became more positive. The results suggest a mixed pattern rather than a straightforward shift toward negativity.

## Limitations and Next Steps

This is an exploratory study of public Reddit posts, not a representative survey of Publix employees. The small sample, potential selection bias, and VADER's limitations with sarcasm and context all affect interpretation. Parent posts may also differ from the more detailed experiences expressed in their comments.

A potential second phase would analyze comments to capture additional context and compare the sentiment of original posts with the discussions they generate.

## Tools

Python · Pandas · NLTK/VADER · Jupyter Notebook · Matplotlib · Git/GitHub

## Project Files

- [Analysis notebook](notebooks/dataExploration1.ipynb) — data exploration, sentiment scoring, and longitudinal analysis.
- [Full portfolio case study](https://ranedomain.wordpress.com/2026/10/10/evaluating-the-evaluations-an-analysis-of-publix-employee-sentiment/) — detailed methodology, results, visualizations, and limitations.

*Note: Research datasets are excluded from this repository, so reproducing the full analysis requires the original CSV files.*

# Evaluating the Evaluations: A Longitudinal Sentiment Analysis of Publix Employee Discussions

## Overview

Is sentiment toward Publix employee evaluations getting worse over time?

This project investigates that question by analyzing public discussions on Reddit's r/Publix community across four years: 2021, 2023, 2025, and 2026. The goal was to explore whether employee discussions showed a consistent shift toward more negative sentiment, rather than relying on individual experiences alone.

## Methodology

I initially collected and validated 64 Reddit parent-post records across four study years: 2021, 2023, 2025, and 2026. The intended collection window was July 25 through August 10, corresponding to the period surrounding Publix's employee evaluations. The 2021 dataset includes broader date coverage to retain relevant discussions surrounding a transition in the evaluation and raise cycle.

After removing one duplicate record and excluding four deleted 2026 posts with no usable text, I analyzed 59 posts using Python, Liu's opinion lexicon, and VADER, a sentiment analysis tool designed for social media text.

I compared classifications from both sentiment methods and used VADER compound scores for the longitudinal analysis. I also calculated 95% confidence intervals around yearly mean compound scores to assess uncertainty.

## Key Findings

- 59 parent posts analyzed across four study years.

- 29 positive, 17 negative, and 13 neutral VADER classifications overall.

- Average sentiment increased from 0.134 in 2021 to 0.275 in 2026 on VADER's compound scale of -1 to +1.

- The percentage of negative posts increased from 21.4% in 2021 to 28.6% in 2026.

- 2023 showed the most negative pattern, with 35.0% negative classifications and an average compound score of 0.046.

- All four 95% confidence intervals for yearly mean compound scores included zero.

**Conclusion**: The findings do not establish a consistent worsening trend. Although the share of negative posts increased between 2021 and 2026, average sentiment also became more positive. Sentiment varied across the study years, with 2023 showing the most negative pattern and 2026 the highest average compound score. These results are exploratory and should not be interpreted as representative of all Publix employees.

## Limitations and Next Steps

This is an exploratory study of public Reddit posts, not a representative survey of Publix employees. The small, uneven sample sizes, potential selection bias, and VADER's limitations with sarcasm, context, and informal language affect interpretation. Parent posts may also differ from the more detailed experiences expressed in their comments.

A potential second phase would analyze comments from the same threads, if feasible with Reddit API access, to capture additional context and compare the sentiment of original posts with the discussions they generate.

## Tools

Python · Pandas · NLTK · VADER · Liu Opinion Lexicon · SciPy · Jupyter Notebook · Matplotlib · Git/GitHub
## Project Files

- [Analysis notebook](notebooks/dataExploration1.ipynb) — data exploration, sentiment scoring, and longitudinal analysis.
- [Full portfolio case study](https://ranedomain.wordpress.com/2026/10/10/evaluating-the-evaluations-an-analysis-of-publix-employee-sentiment/) — detailed methodology, results, visualizations, and limitations.

## Data Files

The repository includes the raw Reddit data collected for the project and the validated datasets used for analysis.

- **Raw data (`data/raw/`)**: The collected Reddit parent-post records for 2021, 2023, 2025, and 2026.
- **Validated data (`data/processed/`)**: The datasets after validation and duplicate removal, prepared for analysis.
- **Analysis notebook (`notebooks/dataExploration1.ipynb`)**: The Python notebook used for data exploration, sentiment scoring, and longitudinal analysis.

The final sentiment analysis includes 59 posts with usable text. Four deleted 2026 posts were excluded from sentiment scoring because their text was unavailable.

## Running the Analysis

1. Clone or download this repository.
2. Install Python and Jupyter Notebook or JupyterLab.
3. Install the required libraries listed in the Tools section.
4. Open `notebooks/dataExploration1.ipynb` and run the cells in order.

The notebook's file paths must match the locations of the CSV files in your downloaded repository.

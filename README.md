# Movie economics

By Swadha Patel

## Business question

A large production budget may help a film reach a wider audience, but spending more is not the same as earning a better return. This project investigates which recorded movie attributes are associated with box-office gross, then separates the statistical patterns from the business conclusions they can support.

## Data and scope

The repository includes movies.csv and a Jupyter notebook covering historical films from 1980–2020. Fields include budget, gross, viewer score, vote count, genre, studio, release year, and runtime. The notebook’s complete-case analysis displays 5,421 rows after removing records with missing values.

## Workflow

### Prepare the data

Inspect missing values and data types, retain complete records, convert budget and gross to numeric integers, and sort films by gross earnings. Missing-data exclusions define the sample used for the correlations.

### Explore relationships

Use scatterplots and a fitted regression line to inspect budget versus gross, then a Pearson correlation matrix and heatmap to compare numeric variables.

### Interpret the evidence

The saved numeric correlation output reports budget–gross r = 0.740, votes–gross r = 0.615, and score–gross r = 0.223. These are recorded notebook results, not a refreshed market analysis or a predictive accuracy score.

## Takeaway

In the historical sample, production budget and audience vote count have stronger associations with gross than viewer score does. A useful strategy question is what sits behind those relationships: distribution scale, franchise strength, marketing, release timing, or audience reach. The notebook does not isolate those mechanisms.

## Interpretation and limitations

Gross is not profit: the analysis does not deduct marketing, exhibitor shares, distribution fees, or other costs. Monetary values are not adjusted for inflation, complete-case filtering can introduce selection bias, and vote count can accumulate after release. Arbitrary numeric codes for studio or genre are not meaningful ordered quantities, so their Pearson correlations are not used as substantive findings here. Correlation does not establish causation.

Based on the original notebook and its saved outputs, reviewed October 2026. The notebook contains mixed execution states; the results above refer specifically to its 5,421-row numeric correlation output.

## Explore the artifacts

- [Read the original notebook](https://github.com/Swadha-Patel/Movie-Correlation-Project/blob/main/Movie%20Correlation%20Project.ipynb)
- [Inspect the source dataset](https://github.com/Swadha-Patel/Movie-Correlation-Project/blob/main/movies.csv)

## Reproduction notes

Install Python, Jupyter, pandas, numpy, seaborn and matplotlib. Put `movies.csv` alongside the notebook and replace its original absolute CSV path with `movies.csv`. Restart the kernel and run all cells in order; saved outputs contain mixed execution states. The initial scatter plot has its axis labels reversed (x is budget and y is gross); the later Seaborn plot labels them correctly. Category codes should not be interpreted as ordinal business quantities. The original notebook is preserved.

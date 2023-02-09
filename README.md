<div id="bootcamp"><img style="display: none;" src="https://static.bc-edx.com/data/dl-1-1/m20/lms/img/banner.jpg" alt="lesson banner" />

This activity is broken down into three parts:

* Part 1: Prepare the Data.

* Part 2: Apply Dimensionality Reduction.

* Part 3: Perform a Cluster Analysis with K-means.

#### Part 1: Prepare the Data

1. I read `myopia.csv` into a Pandas DataFrame.

2. I removed the "MYOPIC" column from the dataset.

    * **Note:** The target column is needed for supervised machine learning, but it will make an unsupervised model biased since the target column is effectively providing clusters already!

3. Standardized the dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

#### Part 2: Apply Dimensionality Reduction

1. Perform dimensionality reduction with PCA. How did the number of the features change?

    > For this model, I preserved 90% of the explained variance in dimensionality reduction.

2. Further reduced the dataset dimensions with t-SNE and visually inspect the results. To do this, I ran t-SNE on the principal components, which is the output of the PCA transformation.

3. Created a scatter plot of the t-SNE output.

#### Part 3: Perform a Cluster Analysis with K-means

Created an elbow plot to identify the best number of clusters.

* I used a `for` loop to determine the inertia for each `k` between 1 through 10.

* I then determined where the elbow of the plot is, and at which value of `k` it appears.

### References

Reduced dataset from [Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute](https://clinicaltrials.gov/ct2/show/NCT00000169)

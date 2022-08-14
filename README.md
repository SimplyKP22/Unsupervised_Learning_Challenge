# Unsupervised_Learning_Challenge

## Overview:
	Machine learning uses software to predict specific outcomes based on a particular dataset by using different algorithms and parameters of the data. Depending on the data and the user's desired objective, different types of machine learning can be utilized. In this exercise, we will take a look at Unsupervised Machine Learning. This type of machine learning considers that the potential outcomes are unknown and unlabeled ahead of time. This way, the model will make inferences from the data without relying on guidance from predefined outcomes or labels, such as knowing that the result can only be true/false or a number within a set range (i.e., 1-5). 
    
    Compared to Supervised Machine Learning, Unsupervised Machine Learning allows data clusters to be formed and provide insights about hidden or otherwise unknown patterns within the data.

	For this exercise, we will use  Dimensionality Reduction with PCA. This statistical technique helps to increase the model's performance by removing unnecessary features that do not add a specific amount of value to the data analysis. t-SNE is another tool we will use, which is an analytical tool that further reduces the dimensions of the data. We will also use  K-Means. This algorithm is used to separate the data into clusters based on similarity or distance from a centroid. 
	Applying these aspects to our model will help us to make a recommendation based on our findings. 

## Instructions

This activity is broken down into four parts: 

* Part 1: Prepare the Data

* Part 2: Apply Dimensionality Reduction 

* Part 3: Perform a Cluster Analysis with K-means

* Part 4: Make a Recommendation 

### Part 1: Prepare the Data

1. Read `myopia.csv` into a Pandas DataFrame.

2. Remove the "MYOPIC" column from the dataset.

    * **Note:** The target column is needed for supervised machine learning, but it will make an unsupervised model biased. After all, the target column is effectively providing clusters already! 

3. Standardize your dataset so that columns that contain larger values do not influence the outcome more than columns with smaller values.

### Part 2: Apply Dimensionality Reduction

1. Perform dimensionality reduction with PCA. How did the number of the features change?


  * **Hint:** Rather than specify the number of principal components when you instantiate the PCA model, state the desired **explained variance**. For example, say that a dataset has 100 features. Using `PCA(n_components=0.99)` creates a model that will preserve approximately 99% of the explained variance, whether that means reducing the dataset to 80 principal components or 3. For this assignment, preserve 90% of the explained variance in dimensionality reduction.

2. Further reduce the dataset dimensions with t-SNE and visually inspect the results. To do this, run t-SNE on the principal components, which is the output of the PCA transformation. 

3. Create a scatter plot of the t-SNE output. Are there distinct clusters?

### Part 3: Perform a Cluster Analysis with K-means

Create an elbow plot to identify the best number of clusters. Make sure to do the following:

* Use a `for` loop to determine the inertia for each `k` between 1 through 10. 

* If possible, determine where the elbow of the plot is, and at which value of `k` it appears.

### Part 4: Make a Recommendation

Based on your findings, write up a brief (one or two sentences) recommendation for your supervisor in your Jupyter Notebook. Can the patients be clustered? If so, into how many clusters? 
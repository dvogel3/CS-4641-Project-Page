---
layout: default
---

# Project Motivation
------------
>“To transform the world, help people, lift others up, change lives.”
> ― Matshona Dhliwayo 

Modern global dynamics shift rapidly due to continuous geopolitical change in political, social, and diplomatic spheres. To enable positive development, there is a need to ensure all countries have equal opportunity to be informed on their weaknesses and strengths. Our approach is to understand what makes countries underdeveloped, what makes countries exceptionally developed, and understand the underlying geopolitical reasons and trends among countries that classify them as such. This will allow us to compare underdeveloped countries to exceptionally developed countries to inform international policy.

# Methods
--------
The primary method used to analyze and visualize the dataset was K-Means clustering. K-Means clustering is a method of vector quantization that aims to partition observations/data points into **k** clusters in which each observation/data point belongs to the cluster with the nearest mean. Our grouped decided that this was the best method to gain an understanding of the dataset and its trends. To determine the best number of clusters to use for K-Means, we used the elbow method, which allowed us to understand the best trade-off between groupings and loss.

# Algorithmic Outline of K-Means
---------
Given an initial set of k centroids, the algorithm repeats the following process for a pre-determined amount of iterations or until convergence is reached:

1. **Assignment Step:** First, assign each observation/data point to the cluster with the nearest mean. This can be calculated using a variety of different techniques, but the most common one (and the one we used) is establishing distance from point to center by using Euclidean distance.

2. **Update Step:** After assigning each observation/data point to a cluster, recalculate the centroids based on the assignment step.

Ultimately, we try to optimize the objective function for K-Means which is:

![Objective Equation](/Clustering_Images/Kmeans_objective_equation.png)

# Dataset
----------

The dataset that we used for this project is sourced from [Kaggle](https://www.kaggle.com/joniarroba/65-world-indexes-gathered). It is a dataset composed of 65 indices on countries around the world, primarily taken from the World Bank, UNICEF, NATO, and other reputable sources. Indices include Gross Domestic Product, Human Development Index, GINI coefficient, and other economic and social indicators for each country. The dataset creators note that data that is not available is estimated using a kNN approach. Furthermore, it should be noted that some of these indicies are self-reported from the countries of interest. It's well known that several countries in this dataset do not accurately report statistics that reflect the true state of the country, however, most of the data comes from third-party, unbiased sources that seek to improve the world for its citizens.

# Key Indicators and Terms
---------
There are some important global indicators that are used in our dataset that are relevant to point out:

1. **Human Development Index (HDI):** HDI is a measurement of human development, often framed in terms of whether people are able to "be" and "do" desirable things in life. Examples include being well fed, having shelter, being healthy, as well as having the ability to do work, have education, and participate in voting. A country scores a higher HDI when expected lifespan is higher, the mean education level is higher, and the gross national income GNI (PPP) per capita is higher.

2. **GINI:** The GINI coefficient is a measure of statistical dispersion intended to represent the income or wealth distribution of a nation's residents, and is the most commonly used measurement of inequality. A higher GINI coefficient indicates a higher disparity in income distribution.

3. **Gross Domestic Product (GDP):** The OECD defines GDP as "an aggregate measure of production equal to the sum of the gross values added of all resident and institutional units engaged in production and services (plus any taxes, and minus any subsidies, on products not included in the value of their outputs)." GDP is essential in measuring a country's economic power.


# Visualization
------------
![GINI vs. HDI](/Clustering_Images/ginix_hdiy.png)
**Figure 1: GINI coefficient vs. Human Development Index**

![HDI vs. Electrification Rate](/Clustering_Images/HDI_Electricity.png)
**Figure 2: HDI vs. % of population that have electricity**

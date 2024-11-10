### Dataset info

**For what purpose was the dataset created?**

    test

**Additional Information**

These data are the results of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars. The analysis determined the quantities of 13 constituents found in each of the three types of wines.

I think that the initial data set had around 30 variables, but for some reason I only have the 13 dimensional version. I had a list of what the 30 or so variables were, but a.)  I lost it, and b.), I would not know which 13 variables are included in the set.

The attributes are (dontated by Riccardo Leardi, riclea@anchem.unige.it )

1) Alcohol
2) Malic acid
3) Ash
4) Alcalinity of ash
5) Magnesium
6) Total phenols
7) Flavanoids
8) Nonflavanoid phenols
9) Proanthocyanins
10) Color intensity
11) Hue
12) OD280/OD315 of diluted wines
13) Proline

In a classification context, this is a well posed problem with "well behaved" class structures. A good data set for first testing of a new classifier, but not very challenging.

### Implementation

1. Load dataset using url ([https://archive.ics.uci.edu/ml/machine-learning-databases/wine/wine.data]()) then convert it into csv
2. Data exploration
3. In data preprocessing,
   1. remove outliers using zcore method(IQR method also applicable)
   2. check whether highly correlated features,if so remove them.(correlation matrix)
4. Separate feature and target variables
5. Standadization
6. Splitting dataset into train and test data
7. Figure out k value using method cross validation
8. check accuracy

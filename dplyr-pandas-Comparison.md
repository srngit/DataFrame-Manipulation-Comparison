## Indexing and Selecting Data
### In R
```r
library(dplyr)

head(iris, 1)
# Sepal.Length Sepal.Width Petal.Length Petal.Width Species
# 1          5.1         3.5          1.4         0.2  setosa
tail(iris, 1)
# Sepal.Length Sepal.Width Petal.Length Petal.Width   Species
# 150          5.9           3          5.1         1.8 virginica

iris2 <- iris[11:13,]
iris2
# Sepal.Length Sepal.Width Petal.Length Petal.Width Species
# 11          5.4         3.7          1.5         0.2  setosa
# 12          4.8         3.4          1.6         0.2  setosa
# 13          4.8         3.0          1.4         0.1  setosa
```
### In Python
```py
# load iris dataset
from sklearn import datasets
import pandas as pd
iris = datasets.load_iris()
iris = pd.DataFrame(iris.data, columns=iris.feature_names)

iris.head(1)
# sepal length (cm)  sepal width (cm)  petal length (cm)  petal width (cm)
# 0                5.1               3.5                1.4               0.2
iris.tail(1)
# sepal length (cm)  sepal width (cm)  petal length (cm)  petal width (cm)
# 149                5.9               3.0                5.1               1.8
# same results
iris2 = iris.iloc[10:13,]
iris2 = iris.iloc[[10, 11, 12],]
iris2 = iris.iloc[range(10, 13),]
# sepal length (cm)  sepal width (cm)  petal length (cm)  petal width (cm)
# 10                5.4               3.7                1.5               0.2
# 11                4.8               3.4                1.6               0.2
# 12                4.8               3.0                1.4               0.1

iris2 = iris.iloc[10:13, "sepal length"]

```

# Bivariate Analysis in Python

```{.python .input}
%%javascript
IPython.OutputArea.prototype._should_scroll = function(lines) {
    return false;
}
```

```{.python .input}
import warnings
warnings.filterwarnings('ignore')
```

```{.python .input}
%matplotlib inline
```

```{.python .input  n=1}
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```

```{.python .input  n=2}
df = pd.read_csv('data/data.csv')
```

```{.python .input}
C = df.select_dtypes(exclude=['object']).drop(['Id', 'SalePrice'], axis=1).keys()
qualitive = df.select_dtypes(include=['object']).keys()
```

## Correlation Heatmap


```{.python .input  n=4}
corr = df.corr()

plt.figure(figsize=(10, 10))
sns.heatmap(corr);
```

## Quanitative Data

```{.python .input}
f = pd.melt(df, id_vars=['SalePrice'], value_vars=quantitive)


g = sns.FacetGrid(f, col="variable",  col_wrap=2, sharex=False, sharey=False, size=5)
g = g.map(plt.scatter, "value", "SalePrice", alpha=0.1)
```

## Qualitative Data

```{.python .input}
f = pd.melt(df, id_vars=['SalePrice'], value_vars=qualitive)
g = sns.FacetGrid(f, col="variable",  col_wrap=2, sharex=False, sharey=False, size=5)
g = g.map(sns.boxplot, "value", "SalePrice")
```

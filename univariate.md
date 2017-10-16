# Univariate Analysis in Python

```{.python .input  n=1}
import pandas as pd
import seaborn as sns
%matplotlib inline
```

```{.python .input  n=2}
df = pd.read_csv('data/data.csv')
```

```{.python .input  n=3}
df_quantitive = df.select_dtypes(exclude=['object'])
df_quantitive.drop('Id', axis=1, inplace=True)
df_qualitive = df.select_dtypes(include=['object'])
```

## Plotting All Quantitives Variables (Distplot)

```{.python .input  n=4}
f = pd.melt(df_quantitive, value_vars=df_quantitive.keys())

g = sns.FacetGrid(f, col="variable",  col_wrap=3, sharex=False, sharey=False)
g = g.map(sns.distplot, "value")
```

## Plotting All Qualitive Variables (countplot)

```{.python .input  n=5}
f = pd.melt(df_qualitive, value_vars=df_qualitive.keys())

g = sns.FacetGrid(f, col="variable",  col_wrap=3, sharex=False, sharey=False)
g = g.map(sns.countplot, "value")
```

# Univariate Analysis in Python

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
```

```{.python .input  n=2}
df = pd.read_csv('data/data.csv')
```

```{.python .input  n=3}
quantitive = df.select_dtypes(exclude=['object']).drop('Id', axis=1).keys()
qualitive = df.select_dtypes(include=['object']).keys()
```

## Quantitives Variables

### Boxplot

```{.python .input  n=4}
f = pd.melt(df, value_vars=quantitive)

g = sns.FacetGrid(f, col="variable",  col_wrap=2, sharex=False, sharey=False, size=4)
g.map(sns.boxplot, "value");
```

### Distplot

```{.python .input}
g = sns.FacetGrid(f, col="variable",  col_wrap=2, sharex=False, sharey=False, size=4)
g.map(sns.distplot, "value");
```

## Qualitive Variables

### Countplot

```{.python .input  n=5}
f = pd.melt(df, value_vars=qualitive)

g = sns.FacetGrid(f, col="variable",  col_wrap=2, sharex=False, sharey=False, size=4)
g.map(sns.countplot, "value");
```

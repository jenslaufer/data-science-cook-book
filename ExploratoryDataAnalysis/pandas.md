```{.python .input  n=1}
import pandas as pd
import numpy as np
df = pd.DataFrame([(1,-1), (2,-1), (-1,3)], columns=['A','B'])
df = pd.DataFrame([{'C':1, 'D':1}, {'C':-1, 'D':1}])
df
```

```{.json .output n=1}
[
 {
  "data": {
   "text/html": "<div>\n<style>\n    .dataframe thead tr:only-child th {\n        text-align: right;\n    }\n\n    .dataframe thead th {\n        text-align: left;\n    }\n\n    .dataframe tbody tr th {\n        vertical-align: top;\n    }\n</style>\n<table border=\"1\" class=\"dataframe\">\n  <thead>\n    <tr style=\"text-align: right;\">\n      <th></th>\n      <th>C</th>\n      <th>D</th>\n    </tr>\n  </thead>\n  <tbody>\n    <tr>\n      <th>0</th>\n      <td>1</td>\n      <td>1</td>\n    </tr>\n    <tr>\n      <th>1</th>\n      <td>-1</td>\n      <td>1</td>\n    </tr>\n  </tbody>\n</table>\n</div>",
   "text/plain": "   C  D\n0  1  1\n1 -1  1"
  },
  "execution_count": 1,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=2}
df.apply(lambda x:len(x[x==-1]))
```

```{.json .output n=2}
[
 {
  "data": {
   "text/plain": "C    1\nD    0\ndtype: int64"
  },
  "execution_count": 2,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=3}
s = pd.Series([-1,2,3,4,1,-1,-1], index=['A',20,30,40,50,60,70])
s
```

```{.json .output n=3}
[
 {
  "data": {
   "text/plain": "A    -1\n20    2\n30    3\n40    4\n50    1\n60   -1\n70   -1\ndtype: int64"
  },
  "execution_count": 3,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

```{.python .input  n=4}
s[s==-1]
```

```{.json .output n=4}
[
 {
  "data": {
   "text/plain": "A    -1\n60   -1\n70   -1\ndtype: int64"
  },
  "execution_count": 4,
  "metadata": {},
  "output_type": "execute_result"
 }
]
```

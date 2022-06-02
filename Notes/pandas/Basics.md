# Basics

[**Documentation**](https://pandas.pydata.org/docs/)

```python
import pandas as pd
```
### Load files
```python
df = pd.read_csv('filename.csv',
                 sep=',',
                 comment='',
                 na_values=['']
                 nrows=1,
                 header=None)
```
# Basics

**>** [**Documentation**](https://seaborn.pydata.org/api.html)

Seaborn is built on top of Matplotlib so they can interact and mix pretty well.

```python
import matplotlib.pyplot as plt
import seaborn as sns
```

Show plot:

```python
plt.show()
```
Clear plot:

```python
plt.clf()
```

### Univariate Distribution Analysis
The best place to start is *displot()*.

Useful alternatives: *rugplot()*, *kdeplot()*, *ecdfplot()*.

### Regression Analysis
*lmplot()* performs regression analysis and supports facetting.



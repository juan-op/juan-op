# Plot types

## Categorical plots
### Show each observation
* Stripplot:
```python
sns.stripplot(data = df, x = '', y = '', 
              jitter = True/False)
```
* Swarmplot:
```python
sns.swarmplot(data = df, x = '', y = ''
             hue = '')
```
### Abstract representations
* Boxplot:
```python
sns.boxplot(data = df, x = '', y = '',
           hue = '') 
```
* Violinplot:
```python
sns.violinplot(data = df, x = '', y = '',
              palette = '',
              hue = '')
```
* Boxenplot:
```python
sns.boxenplot(data = df, x = '', y = '',
              palette = '',
              hue = '')
```
### Statistical estimates:
* Barplot:
```python
sns.barplot(data = df, x = '', y = '',
           hue = '')
```
* Pointplot:
```python
sns.pointplot(data = df, x = '', y = '',
             hue = '')
```
* Countplot:
```python
sns.countplot(data = df, y = '', 
              hue = '')
```

## Regression plots
* Regplot:
```python
sns.regplot(data = df, x = '', y = '',
            marker = '',
            hue = '',
            col = '',
            order = a,
            x_jitter = .b,
            x_estimator = np.mean/median...,
            x_bins = c,
            fit_reg = True/False)
```
* Residplot:
```python
sns.residplot(data = df, x = '', y = '',
             order = a)
```

## Matrix plots
* Heatmap (requires data to be in a grid format, we can use panda's *crosstab()*) :
```python
sns.heatmap(pd.crosstab(df[''], df[''], values = df[''], aggfunc = ''),
           annot = True/False,
           fmt = '',
           cmap = '',
           cbar = True/False,
           linewidths = .a,
           center = df.loc[b,c])
```
## Multiple plots
### FacetGrid:
```python
g = sns.FacetGrid(df, 
                  col = '',
                  row = '',
                  col_order = [],
                  row_order = [])

g.map(sns.boxplot/plt.scatter..., '', order = ['', ''...])
```
+ Catplot:
```python
sns.catplot(x = '', data = df,
            kind = '',
            col = '',
            row = '',
            col_order = [],
            row_order = [])
```
* Lmplot:
```python
sns.lmplot(data = df, x = '', y = '',
           col = '',
           row = '',
           fit_reg = True/False)
```
### PairGrid:
```python
g = sns.PairGrid(df, vars = ['', '', ...])

g = g.map(sns.scatterplot...)
///
g = g.map_diag(sns.histplot...)
g = g.map_offdiag(sns.scatterplot...)
```
* Pairplot:
```python
sns.pairplot(df, vars = ['', '', ...], x_vars = [], y_vars = [],
             kind = '',
             diag_kind = '',
             hue = '',
             palette = '',
             plot_kws = {'': a}
```
### JointGrid:
```python
g = sns.JointGrid(data = df, x = '', y = '')

g.plot(sns.regpplot..., sns.histplot...)
///
g.plot_joint(sns.kdeplot...)
g.plot_marginals(sns.kdeplot, 
                 shade = True/False)
```
* Jointplot:
```python
sns.jointplot(data = df, x = '', y = '',
              kind = '',
              xlim = (a, b),
              order = c,
            
             )

sns.jointplot(x, y, kind...).plot_joint(sns.kdeplot...)
```
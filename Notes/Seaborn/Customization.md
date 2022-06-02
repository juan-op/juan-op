# Customization

## Styles

Seaborn has default configurations that can be applied with:
```python
# default style:
sns.set()
# choose style:
sns.set_style()
```
Styles: *darkgrid*, *whitegrid*, *dark*, *white*, *ticks*.

These styles can override matplotlib and pandas plots as well.

## Remove axes

You can remove the axes with:

```python
sns.despine(left = True/False
            right = True/False
            top = True/False
            bottom = True/False)
```


## Colors

Seaborn supports assigning colors to plots using *matplotlib* color codes:

```python
sns.set(color_codes = True)
sns.displot(df['x'], color = 'g')
```

Palettes can be defined:

```python
sns.set_palette()
```
Palettes: *deep*, *muted*, *pastel*, *bright*, *dark*, *color blind*.

Display a palette:

```python
sns.palplot()
```

Return the current palette:

```python
sns.color_palette()
```

Custom palettes:
* Circular colors:  when the data is not ordered
* Sequential colors: when the data has a consistent range from high to low.
* Diverging colors: when both the low and high values are interesting.

## Matplotlib Axes
Most customization available through *matplotlib* **Axes** objects, they can be passed to seaborn functions.

```python
fig, ax = plt. subplots()
sns.histplot(df['x'], ax = ax)
ax.set(xlabel = ''
       ylabel = ''
       xlim = (a , b)
       title = '' ...)
```
Multiple plots can be combined and configured:

```python
fig, (ax0, ax1) = plt.subplots(nrows = 1, ncols = 2, 
                               sharey = True, figsize = (a,b)
sns.histplot(df['x'], ax = ax0)
sns.histplot(df['y'], ax = ax1)
ax1.set(xlabel = ''
       ylabel = ''
       xlim = (a , b)
       title = '' ...)
ax1.axvline(x = , label = '', linestyle = '')
ax1.legend()
```

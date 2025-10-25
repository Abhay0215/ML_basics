# Seaborn Cheat Sheet (Minimal & Clean)

## Importing Libraries

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
```

## Loading Sample Dataset

```python
df = sns.load_dataset('iris')
```

## Setting Style & Palette

```python
sns.set_style('whitegrid')  # Options: white, dark, whitegrid, darkgrid, ticks
sns.set_palette('pastel')    # Options: deep, muted, bright, pastel, dark
```

## Scatter Plot

```python
sns.scatterplot(data=df, x='sepal_length', y='sepal_width', hue='species')
plt.show()
```

## Line Plot

```python
sns.lineplot(data=df, x='sepal_length', y='petal_length', hue='species')
plt.show()
```

## Histogram

```python
sns.histplot(df['sepal_length'], bins=20, kde=True)
plt.show()
```

## KDE Plot

```python
sns.kdeplot(df['sepal_length'], shade=True)
plt.show()
```

## Box Plot

```python
sns.boxplot(data=df, x='species', y='sepal_length')
plt.show()
```

## Violin Plot

```python
sns.violinplot(data=df, x='species', y='sepal_length')
plt.show()
```

## Pair Plot

```python
sns.pairplot(df, hue='species')
plt.show()
```

## Heatmap

```python
corr = df.corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.show()
```

## Count Plot

```python
sns.countplot(data=df, x='species')
plt.show()
```

## Regression Plot

```python
sns.regplot(data=df, x='sepal_length', y='petal_length')
plt.show()
```

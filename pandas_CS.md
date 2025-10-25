# Pandas Cheat Sheet (Minimal & Clean)

## Importing Pandas

```python
import pandas as pd
```

## Creating DataFrames

* From dictionary:

```python
data = {"Name": ["A", "B"], "Age": [20, 25]}
df = pd.DataFrame(data)
```

* From CSV:

```python
df = pd.read_csv("data.csv")
```

* From Excel:

```python
df = pd.read_excel("file.xlsx")
```

## Inspecting Data

* `df.head()` – First 5 rows
* `df.tail()` – Last 5 rows
* `df.info()` – Summary (rows, cols, types)
* `df.describe()` – Stats summary
* `df.shape` – (rows, cols)
* `df.columns` – Column names
* `df.dtypes` – Data types

## Selecting Data

* Column: `df['col']` or `df[['col1','col2']]`
* Row by index: `df.iloc[0]`
* Row by label: `df.loc["row_label"]`
* Filter: `df[df['Age'] > 18]`

## Adding & Modifying Data

* Add column: `df['New'] = ...`
* Update values: `df.loc[0,'Age'] = 30`
* Rename columns:

```python
df = df.rename(columns={"Old":"New"})
```

## Handling Missing Values

* Check missing: `df.isna().sum()`
* Drop missing rows: `df.dropna()`
* Fill missing:

```python
df.fillna(0)
df.fillna(df['Age'].mean())
```

## Sorting & Grouping

* Sort:

```python
df.sort_values("Age")
df.sort_values(["Age", "Score"], ascending=[True, False])
```

* Groupby:

```python
df.groupby("City")["Salary"].mean()
```

## Merging & Joining

```python
pd.concat([df1, df2])              # Stack
pd.merge(df1, df2, on="id")       # Join on column
```

## Exporting Data

```python
df.to_csv("out.csv", index=False)
df.to_excel("out.xlsx", index=False)
```

## Common Useful Functions

* Unique values: `df['col'].unique()`
* Value counts: `df['col'].value_counts()`
* Drop columns: `df.drop(columns=['col'])`
* Apply function: `df['col'].apply(lambda x: x*2)`

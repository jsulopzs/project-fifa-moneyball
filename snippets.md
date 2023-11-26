## DataFrame Operations

- DataFrame: multiple columns
- Series: a column of a DataFrame

![](src/01_table_dataframe.svg)

![](src/02_io_readwrite.svg)

### Series

#### Selecting a series

```python
s = df['column_name']
s
```

#### Sorting rows

```python
s.sort_values(ascending=False)
```

#### Select top 10 rows

```python
s.head(10)
```

#### Select bottom 10 rows

```python
s.tail(10)
```

### DataFrame

#### Filtering rows

```python
condition = df['column_name'] == 'value' # condition (mask)
df_filtered = df[condition]
df_filtered
```

#### Grouping by unique categories of a column

```python
s_grouped = df.groupby('column_categorical')['column_numerical'].mean()
s_grouped
```

**Other DataFrame Operations**

- `mean()`
- `size()`
- `sum()`
- `max()`
- `min()`
- ... and more: [see CheatSheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf) (page 2 "Summarize Data")

## Data Visualization

### Series

Plotting one Series:

```python
s.plot.bar()
```

- `line()`
- `area()`
- `barh()`
- ... and more: see full list of plots [here](https://pandas.pydata.org/docs/reference/api/pandas.Series.plot.html).

### DataFrame

Plotting multiple Series at once:

```python
df.plot.line()
```

One plot per Series:

```python
df.plot.line(subplots=True)
```
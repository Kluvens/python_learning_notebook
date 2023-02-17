## Creating data

### DataFrame
A dataframe is a table.
It contains an array of individual entries,
each of which has a certain value.
Each entry corresponds to a row and a column.

```
pd.DataFrame({'Yes': [50, 21], 'No': [131,2]})
```

![image](https://user-images.githubusercontent.com/95273765/219207825-cad209bd-8cbc-4cec-93a5-489bffdae851.png)

```
pd.DataFrame({'Bob': ['I liked it.', 'It was awful.'], 
              'Sue': ['Pretty good.', 'Bland.']},
             index=['Product A', 'Product B'])
```

![image](https://user-images.githubusercontent.com/95273765/219208281-719abedb-6bcf-48ae-90f3-04b2fa742b8b.png)

### Series
A series, by contrast, is a sequence of data values.
If a dataframe is a table, a series is a list.

![image](https://user-images.githubusercontent.com/95273765/219208506-31e638b7-0a5e-4e1e-a8e6-5499dc379aba.png)

A series is, in essence, a single column of a dataframe.
So we can assign row labels to the series the same way as before, using an `index  parameter.
However, a series does not have a column name, it only has one overall `name`.

![image](https://user-images.githubusercontent.com/95273765/219208837-93449377-a30c-484c-8350-923e58f8c2c8.png)

## Reading data files
Read CSV file:
``` python
wine_reviews = pd.read_csv("../input/wine-reviews/winemag-data-130k-v2.csv")
```

We can use the `shape` attribute to check how large the resulting DataFrame is:
```
wine_reviews.shape

# it tells how many records split across a certain number of different columns
```

We can examine the contents of the resultant DataFrame using the `head()` command, which grabs the first five rows.
``` python
wine_reviews.head()
```

## Native accessors
In python, we can access the property of an object by accessing it as an attribute.
A `book` object, for example, might have a `title` property, which we can access by calling `book`.

Hence to access the `country` property of `reviews` we can use:
```
reviews.country
```

![image](https://user-images.githubusercontent.com/95273765/219213679-7daeb44a-5917-42df-94a9-24ed9e0dcfa0.png)

We can also do 
```
reviews['country']
```

## Indexing in pandas
The indexing operator and attribute selection are nice because they work just like they do in the rest of the Python ecosystem.

### Index-based selection
Pandas indexing works in one of two paradigms.
The first is index-based selection:
selecting data based on its numerical position in the data.
Both `loc` and `iloc` are row-first, column-second.

`loc` and `iloc` are two important indexing methods in Pandas that allow selecting rows and columns of a DataFrame.

`loc` is used to select data based on labels of rows or columns. It takes the form `df.loc[row_label, column_label].`
The `row_label` and `column_label` can be a single label, a list of labels, or a slice of labels.

``` python
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
        'age': [25, 28, 19, 31, 22],
        'gender': ['F', 'M', 'M', 'M', 'F']}

df = pd.DataFrame(data)
df.set_index('name', inplace=True)

print(df.loc['Bob', 'age']) # Output: 28
```

`iloc` is used to select data based on the integer position of rows or columns.
It takes the form `df.iloc[row_index, column_index]`.

The `row_index` and `column_index` can be a single index, a list of indexes, or a slice of indexes.

``` python
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
        'age': [25, 28, 19, 31, 22],
        'gender': ['F', 'M', 'M', 'M', 'F']}

df = pd.DataFrame(data)
df.set_index('name', inplace=True)

print(df.iloc[1, 1]) # Output: 28
```

On its own, the `:` operator, which also comes from native Python, means 'everything'.
``` python
reviews.iloc[:3, 0]
```

![image](https://user-images.githubusercontent.com/95273765/219215404-05bb3082-5b2a-4f1f-a381-f251c6ac2b87.png)

## Manipulating the index
Label-based selection derives its power from the labels in the index. Critically, the index we use is not immutable. We can manipulate the index in any way we see fit.

The `set_index()` method can be used to do the job.

## Info about the data
The DataFrames object has a method called `info()`, that gives us more information about the data set.

``` python
print(df.info())
```

The `info()` method also tells us how many non-null values there are present in each column.

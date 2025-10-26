```bash
pip install pandas
```

```python
import pandas as pd
print(pd.__version__)
```
# Read File
```python
import pandas as pd 
pd.options.display.max_rows = 9999 # Set maximum rows number
df = pd.read_csv('data.csv')  # df = pd.read_json('data.json') 
print(df.to_string())
```
Without `to_string()`, if you have a large DataFrame with many rows, Pandas will only return the first 5 rows, and the last 5 rows.

# Series
Like a column in a table. It is a one-dimensional array holding data of any type.
```python
import pandas as pd
a = [1, 7, 2]
myvar = pd.Series(a)
print(myvar)
print(myvar[0])
```
If nothing else is specified, the values are labeled with their index number. First value has index 0,..
```python
myvar = pd.Series(a, index = ["x", "y", "z"]) # Create labels
```
_[[Python - Object|Key/Value Objects]]_ are Series
```python
calories = {"day1": 420, "day2": 380, "day3": 390}

myvar = pd.Series(calories)
myvar = pd.Series(calories, index = ["day1", "day2"]) # To select only some of the items in the dictionary
```

# DataFrames
Series is like a column, a DataFrame is the whole table.
```python
import pandas as pd
data = {
  "calories": [420, 380, 390],
  "duration": [50, 40, 45]
}
df = pd.DataFrame(data, index = ["day1", "day2", "day3"])
print(myvar)
```
## Locate
```python
print(df.loc[0]) # Locate Row: Return Series
print(df.loc[[0, 1]]) # Return DataFrame
print(df.loc["day2"]) # Locate Named Indexs
```

## Analyzing
```python
print(df.head(10)) # Print the first 10 rows
print(df.tail(10)) # Print the last 10 rows

print(df.info()) # Print information about the data
```

# Cleaning Data
## Empty Cells
**Remove Rows**
```python
new_df = df.dropna() # Return a new DataFrame
df.dropna(inplace = True) # Change the original DataFrame
```
**Replace Empty Values**
```python
df.fillna(130, inplace = True) # Replaces all empty cells in the whole Data Frame.
df.fillna({"Calories": 130}, inplace=True) # Only replace empty values for one column
```
**Mean**: the average value (the sum of all values divided by number of values).
```python
x = df["Calories"].mean()  
df.fillna({"Calories": x}, inplace=True)
```
**Median**: the value in the middle, after you have sorted all values ascending.
```python
x = df["Calories"].mode()[0]
```
**Mode**:  the value that appears most frequently.
```python
x = df["Calories"].mode()[0]
```

##  Wrong Format
**Date**
```python
df['Date'] = pd.to_datetime(df['Date'], format='mixed') # Convert Into a Correct Format
df.dropna(subset=['Date'], inplace = True) # Removing Rows
```

## Wrong Data
```python
df.loc[7, 'Duration'] = 45 # Replacing Values
    df.drop(x, inplace = True) # Removing Rows
```

## Removing Duplicates
```python
print(df.duplicated()) # Discovering Duplicates
df.drop_duplicates(inplace = True) ## Removing Duplicates
```

# Data Correlations
```python
df.corr()
"""
		Duration     Pulse  Maxpulse  Calories
  Duration  1.000000 -0.155408  0.009403  0.922721
  Pulse    -0.155408  1.000000  0.786535  0.025120
  Maxpulse  0.009403  0.786535  1.000000  0.203814
  Calories  0.922721  0.025120  0.203814  1.000000
"""
```
The number varies from _-1 to 1_:
- 1 means that there is a 1 to 1 relationship (a perfect correlation), and for this data set, each time a value went up in the first column, the other one went up as well.
- 0.9 is also a good relationship, and if you increase one value, the other will probably increase as well.
- -0.9 would be just as good relationship as 0.9, but if you increase one value, the other will probably go down.
- 0.2 means NOT a good relationship, meaning that if one value goes up does not mean that the other will.
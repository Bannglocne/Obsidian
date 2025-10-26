```shell
pip install seaborn
!pip install seaborn
conda install seaborn
```

```python
import matplotlib.pyplot as plt
import seaborn as sns
```
_Example_
```python
import seaborn as sns
exercise = sns.load_dataset("exercise")
exercise.head()
```

# Plot Types
**Three main categories**
	- Univariate – x 
	- Bivariate – x, y
	- Trivariate – x, y, z
![[Seaborn_plot_types.png]]

**Common plot types**:
- `scatterplot()`: Scatter Plot
- `lineplot()`: Line Plot
- `barplot()`: Bar Plot
- `hisplot()`: Histogram
- `kdeplot()`: Density Plot
- `boxplot()`: Box Plot
- `violinplot()`: Violin Plot
- `heatmap()`: Heatmap
- `pairplot()`: Pair Plot
- `jointplot()`: Join Plots

## Face Grid
Visualizing the distribution of one variables as well as the relationship between two variables, across level of additional categorical variables
```python
g = sns.FacetGrid(tips, col="day") 
g.map(sns.histplot, "total_bill")
```
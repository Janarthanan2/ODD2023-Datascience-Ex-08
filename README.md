# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
- STEP 1:
 Read the given Data
- STEP 2:
 Clean the Data Set using Data Cleaning Process
- STEP 3:
 Apply Feature generation and selection techniques to all the features of the data set
- STEP 4:
 Apply data visualization techniques to identify the patterns of the data.

# PROGRAM:
```
Developed By: JANARTHANAN V K
Reg No: 212222230051
```

```python
import pandas as pd
df=pd.read_csv("/content/Superstore (3).csv",encoding='unicode_escape')
df.head()
```
### DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
- <B>_LINE PLOT:_</B>
```
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
- <B>_SCATTERPLOT:_</B>
```
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```

- <B>_BOXPLOT:_</B>
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```

- <B>_VIOLIN PLOT:_</B>
```
sns.violinplot(x="Profit",data=df)
```

- <B>_BARPLOT_</B>
```
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```

- <B>_POINTPLOT_</B>
```
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```

- <B>_COUNT PLOT_</B>
```
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```

- <B>_HISTOGRAM_</B>
```
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 

- <B>_KDE PLOT_</B>
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```

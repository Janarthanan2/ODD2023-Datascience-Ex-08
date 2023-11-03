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
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/ebf5d018-c31c-4610-b26e-6395daeb5448" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/f50bd4c8-8840-4d61-afa9-f090d98716d2" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/dddc0ce1-5d37-463d-af9d-d9a39cf33def" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/23b30b9e-cb60-4dd5-a7a7-be941b7e291d" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/e422342a-4fff-487e-9780-aa92e2db6b19" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/8f9e780a-bcdd-47e0-a21e-25e8dca37cab" height=300 width=350>

- <B>_BOXPLOT:_</B>
```
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/68af3f52-c256-452b-b987-afc6767d09ac" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/27f1e245-2725-436d-a68b-df3b3c5c1660" height=300 width=350>

- <B>_VIOLIN PLOT:_</B>
```
sns.violinplot(x="Profit",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/19b590d7-641d-47ed-af0f-40e52df39587" height=300 width=350>

- <B>_BARPLOT_</B>
```
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/16ece634-b224-42df-82be-c4a731f908af" height=500 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/32fcf2ae-85be-4bfa-bacb-0839304efe5b" height=300 width=350>

- <B>_POINTPLOT_</B>
```
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
<img src="" height=300 width=350>

- <B>_COUNT PLOT_</B>
```
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
<img src="" height=300 width=350>
<img src="" height=300 width=350>

- <B>_HISTOGRAM_</B>
```
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
<img src="" height=300 width=350>

- <B>_KDE PLOT_</B>
```
sns.kdeplot(x="Profit", data = df,hue='Category')
```
<img src="" height=300 width=350>

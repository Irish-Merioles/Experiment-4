# 📊 Programming Assignment - Data Wrangling and Data Visualization

This repository contains my programming assignments for **ECE 2112: Advanced Computer Programming and Algorithms**
---

## ✧˖°. Contents

### ✨ [Experiment 4 –Data Wrangling and Data Visualization](EXPERIMENT 4 - Data Wrangling and Data Visualization.ipynb)  

---

### Problem 1: ECE BOARD PROBLEM

#### 1. Import the required libraries.

#### 2. Load the dataset board2.xlsx using pandas.read_excel().


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
#### 3. Create Filtered DataFrames
   Example:
```python
Vis = df.query('Hometown == "Visayas" & Math < 70')[["Name","Gender","Track","Math"]]
print(Vis)
```
  A.  Instru = [“Name”, “GEAS”, “Electronics >70”];
```python
Instru = df.query('Track == "Instrumentation" & Hometown == "Luzon" & Electronics > 70')[["Name","GEAS","Electronics"]]
print(Instru)
```
  B.  Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; 
```python
df["Average"] = df[["Math","GEAS","Electronics","Communication"]].mean(axis=1)
Mindy = df.query('Hometown == "Mindanao" & Gender == "Female" & Average >= 55')[["Name","Track","Electronics","Average"]]
print(Mindy)
```
#### 4. Check whether Track, Gender, or Hometown contributes to a higher average score by plotting bar charts.

A. Average score by track
```python
plt.figure(figsize=(6,4))
sns.barplot(x="Track", y="Average", data=df)
plt.title("Average Score by Track")
plt.show()

```
  B. Average score by gender
```python
plt.figure(figsize=(6,4))
sns.barplot(x="Gender", y="Average", data=df)
plt.title("Average Score by Gender")
plt.show()

```  
  C. Average score by hometown
```python
plt.figure(figsize=(6,4))
sns.barplot(x="Hometown", y="Average", data=df)
plt.title("Average Score by Hometown")
plt.show()
```

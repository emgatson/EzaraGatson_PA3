# **GATSON_EMR_PA3**

# **ECE Programming Assignment 3**
## **PROBLEM 1**
This program performs basic data exploration on automotive performance data. It loads vehicle specifications from a CSV file

---
This loads the automotive dataset from 'cars.csv' and displays all vehicle models with their specifications including mpg, cylinders, horsepower, and other metrics.
```python
import pandas as pd    #Import pandas library for data manipulation
cars = pd.read_csv('cars.csv')   #Load the automotive dataset from CSV file
cars
```

This shows first five vehicles in the dataset to quickly understand the data structure and content and last five vehicles in the dataset to examine the end portion of the data.
```python
cars.head()    #Show the first five rows to understand data structure
cars.tail()    #Display the last five rows to examine the dataset's end
```

## **PROBLEM 1**
This program demonstrates advanced data filtering and selection techniques on the automotive dataset. It shows how to extract specific columns, filter rows based on conditions, and select particular data subsets

---
This loads the automotive dataset from 'cars.csv' and displays all vehicle models with their specifications including mpg, cylinders, horsepower, and other metrics.
```python
import pandas as pd    #Import pandas for data analysis
cars = pd.read_csv('cars.csv')   #Load the dataset for advanced filtering operations
cars
```
This selects every second column starting from position 1 (odd-indexed columns) to create a simplified dataset with fewer features and extracts only the first row of the dataset.
```python
odd_columns = cars.iloc[:,1::2]   #Select every second column starting from position 1 (odd-indexed columns)

result = odd_columns.head()       #Display first five rows of the filtered columns
result

cars[0:1] 
```

This filters the dataset to find the 'Camaro Z28' model and returns only its name and cylinder count for specific analysis.
```python
cars.loc[cars['Model']=='Camaro Z28', ['Model', 'cyl']]    #Filter dataset to find specific vehicle 'Camaro Z28' and return only name and cylinders
```

This selects three specific vehicles by their row indices and returns their model names, cylinder counts, and gear information for comparison.
```python
cars.loc[[1,28,18],['Model', 'cyl', 'gear']]     #Select three specific vehicles by row indices and return their model, cylinders, and gears
```

---
-VERSION 2-

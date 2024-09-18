# EXPERIMENT 4 - DATA WRANGLING AND DATA VISUALIZATION 

This repository features Python scripts designed to solve various problems in ECE2112. Below is a summary of the scripts. 

## ECE BOARD EXAM PROBLEM
  ##### Using data wrangling and data visualization with storytelling, analyze and present: (i) data frames; and (ii) visuals using the dataset given.

**Function:**

```python
#access pandas ibrary 
import pandas as pd

#load ".csv" file to notebook
board = pd.read_csv('board2.csv')
board

```
**Output:**

![image](https://github.com/user-attachments/assets/ad93cf9c-33d6-4dcb-8940-f44131423ee8)
![image](https://github.com/user-attachments/assets/5e76c488-912e-44be-8891-c7e8605fffea)

**Function:**
```python

#output description of data frame
board.describe()
```

**Output:**

![image](https://github.com/user-attachments/assets/acc891d7-2c19-40f8-865b-b3e24b02d60f)


### Problem 1
###### Create the following data frames based on the format provided 

### a. Instru 

**Function:**
```python

#set Instrumentation as track and Luzon as hometown, as the constant features for data wrangling 
Instru = board.loc[(board['Track']=='Instrumentation')&(board['Hometown']=='Luzon')&(board['Electronics']>70), ['Name', 'GEAS', 'Electronics']]
Instru

```

**Output:**

![image](https://github.com/user-attachments/assets/5df7843c-a58e-4f66-8a19-143f44081f3b)

### b. Mindy

**Function:**
```python

#set Mindanao as hometown and Female as gender, as the constant features for data wrangling 
Mindy = board.loc[(board['Hometown']=='Mindanao')&(board['Gender']=='Female')&(board['Electronics']>55), ['Name', 'Track', 'Electronics']]
Mindy

```

**Output:**

![image](https://github.com/user-attachments/assets/e09f3910-a299-44e9-b769-be0cf761b417)

### Problem 2

###### Create a visualization that shows how the different features contributes to average grade. 

**Function:**

```python

#college track as feature
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 5))
plt.bar(board['Track'], board['Electronics'])

```

**Output:** 

![image](https://github.com/user-attachments/assets/77e89088-0d33-4d0f-b167-00f90e46c150)

**Function:**

```python

#gender as feature
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 5))
plt.bar(board['Gender'], board['Electronics'])

```

**Output:** 

![image](https://github.com/user-attachments/assets/76bb7ee0-7783-4fc2-8dcc-98a489d09f69)


**Function:**

```python

#hometown as feature
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 5))
plt.bar(board['Hometown'], board['Electronics'])

```

**Output:** 

![image](https://github.com/user-attachments/assets/3365e9f0-131f-4db8-901b-f81b0bce5b27)


  

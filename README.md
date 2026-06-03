## NAME: Thaarakeshwar
## REGISTER NO: 212225040466

## EX 21:NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
```
import numpy as np

arr = np.array([
    [9, 4, 7],
    [2, 8, 1],
    [5, 3, 6]
])

sorted_arr = np.sort(arr, axis=0)

print(f"The original array is:\n{arr}")
print(f"\nThe column-wise sorted array is:\n{sorted_arr}")
```
## Output

<img width="515" height="356" alt="{EE4F4C97-DDD8-4E86-8E63-7E6B64F18B2F}" src="https://github.com/user-attachments/assets/8246c63a-42a7-47d9-9ce8-1f5a4f538b57" />

## Result
Thus, the Python NumPy program to sort the elements of each column in a 2D array in ascending order was successfully implemented and executed, and the output was verified.

## EX 22:NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program
```
import numpy as np

x = np.array([4, 7, 2, 9, 5])
y = np.array([3, 7, 5, 1, 5])

indices = np.where(x >= y)

print(f"The array x is: {x}")
print(f"The array y is: {y}")
print(f"The indices where x is greater than or equal to y are: {indices}")
```
## Output

<img width="886" height="223" alt="{4E299779-D613-405C-9AF8-E2885D5E3021}" src="https://github.com/user-attachments/assets/be9b5481-6a9d-4c5f-b322-595b3dc780f9" />

## Result
Thus, the Python NumPy program to find the indices where elements of array x are greater than or equal to the corresponding elements of array y was successfully implemented and executed, and the output was verified.

## EX 23:NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program
```
import numpy as np

arr = np.array([
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
])

new_column = np.array([100, 200, 300])

arr = np.delete(arr, 1, axis=1)
arr = np.insert(arr, 1, new_column, axis=1)

print(f"The original array after replacing the second column is:\n{arr}")
```
## Output

<img width="636" height="234" alt="{82EF5BC1-A445-48B0-B171-AC4FC6004A00}" src="https://github.com/user-attachments/assets/6ce89906-90d3-47f0-b87a-951c8abb99a8" />

## Result
Thus, the Python NumPy program to delete the second column from a 2D array and insert a new column at the same position was successfully implemented and executed, and the output was verified.

## EX 24:Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

## 💻 Program
```
import pandas as pd
import numpy as np

exam_data = {
    'name': ['Alex', 'Bob', 'Clarke', 'David', 'Eva'],
    'score': [85, 90, 78, 92, 88],
    'attempts': [1, 2, 1, 3, 2],
    'qualify': ['Yes', 'Yes', 'No', 'Yes', 'Yes']
}

labels = ['a', 'b', 'c', 'd', 'e']

df = pd.DataFrame(exam_data, index=labels)

print(f"The DataFrame is:\n{df}")
```
## Output

<img width="437" height="314" alt="{62CAB888-5408-41E5-A373-333AE275C945}" src="https://github.com/user-attachments/assets/293abff5-3c39-4d80-9606-d46e4b58a36a" />

## Result
Thus, the Python Pandas program to create and display a DataFrame using a dictionary with custom index labels was successfully implemented and executed, and the output was verified.

## EX 25:🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

## 💻 Program
```
import pandas as pd

student_data1 = {
    'Name': ['Alex', 'Bob'],
    'Marks': [85, 90]
}

student_data2 = {
    'Name': ['Clarke', 'David'],
    'Marks': [78, 92]
}

df1 = pd.DataFrame(student_data1)
df2 = pd.DataFrame(student_data2)

new_df = pd.concat([df1, df2], axis=0)

print(f"The first DataFrame is:\n{df1}\n")
print(f"The second DataFrame is:\n{df2}\n")
print(f"The combined DataFrame is:\n{new_df}")
```
## Output

<img width="467" height="513" alt="{C183085E-9DC4-4E21-822E-C68AAF6E689D}" src="https://github.com/user-attachments/assets/6c9947aa-1d35-4498-b5c2-30a7a7c9df9d" />

## Result
Thus, the Python Pandas program to join two DataFrames row-wise using pd.concat() was successfully implemented and executed, and the output was verified.

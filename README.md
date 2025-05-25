## NumPy Program: Column-wise Sorting of a 2D Array

##  Aim
To write a *NumPy* program that sorts the elements of a given 2D array in ascending order.
## Case 1: Sort array by the second row
## Case 2: Sort the array by the second column

##  Algorithm
```
1.Start
2.Input a 2D list from the user (as a string, e.g., [[...], [...], [...]])
3.Convert the input string to a NumPy array
4.Print the original array
5.Sort by second row (row index 1):
a. Get the sort order of columns using argsort() on the second row
b. Rearrange the columns accordingly
c. Print the sorted array
6.Sort by second column (column index 1):
a. Get the sort order of rows using argsort() on the second column
b. Rearrange the rows accordingly
c. Print the sorted array
7.End the program
```
##  Program
```
import numpy as np
a = np.array(eval(input()))
print("Printing Original array")
print(a)
sorted_by_row = a[:, a[1].argsort()]
print("Sorting Original array by second row")
print(sorted_by_row)
sorted_by_col = a[a[:, 1].argsort()]
print("Sorting Original array by second column")
print(sorted_by_col)
```
## Output
![Screenshot 2025-05-24 161130](https://github.com/user-attachments/assets/1919ef72-b6ab-43e9-ad08-f3c36128449a)

## Result
Thus the *NumPy* program that sorts the elements of a given 2D array in ascending order is executed successfully.
 
## NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## Aim
To write a Python program using *NumPy* that finds the indices where elements in array x are greater than or equal to their corresponding elements in array y.

##  Algorithm
1. *Import NumPy*: Import the NumPy library.
2. *Define Arrays*: Define two NumPy arrays, x and y, with the same shape (i.e., same number of elements).
3. *Use Boolean Indexing*: 
   - x > y gives a boolean array where elements of x are greater than y.
   - x == y gives a boolean array where elements of x are equal to y.
4. *Find Indices*: Use np.where() to get the indices where the conditions x >= y are satisfied.
5. *Print Indices*: Print the indices where the condition holds true.

##  Program
```
import numpy as np
a=np.array(eval(input()))
b=np.array(eval(input()))
gr=np.where(a>b)
eq=np.where(a==b)
print(gr)
print(eq)
```
## Output
![image](https://github.com/user-attachments/assets/b76a25c2-4b67-4070-bdcf-a4c51cb75162)

## Result
Thus the python program to print the indices of the elements greater than or equal to x is executed successfully.

## NumPy Program: Replace the Second Column in a 2D Array

## Aim
To write a *NumPy* program that find the sum of Second column in a given numpy array.

##  Algorithm
1. *Import NumPy*: Start by importing the NumPy library.
2. *Get Input*: Get a 2D NumPy array and a new column (as another array) from the user.
3.Reshape the NumPy array into a 4×3 matrix.
4.Extract the second column of the reshaped matrix.
5.Compute the sum of all elements in that second column.
6.Display the reshaped matrix.
7.Display the sum of the second column.
8.End

##  Program
```
import numpy as np
arr = np.array(eval(input()))
a=arr.reshape(4,3)
column_sums=sum(a[:,1])
print(a)
print(column_sums)
```
## Output
![image](https://github.com/user-attachments/assets/361016ca-df7d-498c-8c7c-81bc2a9fb5a8)

## Result
Thus the python program to  find the sum of Second column in a given numpy array is executed successfully.

## Pandas Program: Create and Display a DataFrame with Custom Index Labels

##  Aim

To create and display a *DataFrame* using the *Pandas* program to join the two given dataframes along columns and assign all data.

##  Algorithm

1. *Import Libraries*: Import the required libraries – pandas and numpy.
2. *Create Dictionary*: Define a dictionary.
3.Create DataFrames:
  -  Use pd.DataFrame() to convert data1 into df1.
  -  Use pd.DataFrame() to convert data2 into df2.
4.Print the original DataFrames:
5.Display df1 and df2 for verification.
6.Concatenate the two DataFrames:
7.Use pd.concat([df1, df2], axis=1) to join the DataFrames side by side (column-wise).
8.Store the result in a variable (e.g., result).
9.Display the result:
10.Print the concatenated DataFrame.
11.End

##  Program
```
import pandas as pd
data1 = {'s_id': ['S1', 'S2', 'S3', 'S4', 'S5'],'name': ['Dan', 'Ryder', 'Bryce', 'Bernal', 'Kwame'], 'marks': [200, 210, 190, 222, 199]}
data2 = { 's_id': ['S4', 'S5', 'S6', 'S7', 'S8'], 'name': ['Scart', 'Willy', 'Dani', 'Kaise', 'Madeeha'], 'marks': [201, 200, 198, 219, 201]}
df1 = pd.DataFrame(data1)
df2 = pd.DataFrame(data2)
print("Original DataFrames:")
print(df1)
print("-------------------------------------")
print(df2)
print()
result = pd.concat([df1, df2], axis=1)
print("Join the said two dataframes along columns:")
print(result)
```
## Output
![image](https://github.com/user-attachments/assets/969e348d-b477-480c-9f9e-d8f9bcede795)

## Result
Thus the *Pandas* program to join the two given dataframes along columns and assign all data is executed successfully.

##  Pandas Program: Join Two DataFrames Along Rows

## AIM
To write a Python program using Pandas to *join two DataFrames along rows* (row-wise concatenation) and assign all data to a new DataFrame.

##  ALGORITHM

1. *Import Libraries*: Import the pandas library.
2. *Create First DataFrame*: Use a dictionary to create student_data1.
3. *Create Second DataFrame*: Use another dictionary to create student_data2.
4. *Concatenate DataFrames*: Use pd.concat()  to concatenate both DataFrames row-wise.
5. *Display Result*: Print the new combined DataFrame.
##  Program
```
import pandas as pd
d=eval(input())
df=pd.DataFrame(d)
print("Original Dataframe",end='\n ')
print(df)
new=eval(input())
df.loc[len(df)]=new
print("combined Dataframe",end='\n ')
print(df)
```
## Output
![image](https://github.com/user-attachments/assets/c4e08917-65a0-4d8d-95f3-e72b1440bd2a)
## Result
Thus the Python program using Pandas to *join two DataFrames along rows* is executed successfully.

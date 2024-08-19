<code>
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
</code>

#Load your data into a Pandas DataFrame:
<code>
df = pd.read_csv('your_data.csv')
</code>
#Examine the structure and summary statistics of the DataFrame:


# Display the first few rows of the DataFrame
<code>
print(df.head())
</code>
Get an overview of the DataFrame's structure and data types
<code>
print(df.info())
</code>code>
# Calculate summary statistics for numerical columns
<code>
<code>
print(df.describe())
</code>

Handle missing values:


# Check for missing values in each column
<code>
print(df.isnull().sum())
</code>

# Handle missing values based on your data and analysis needs

# For example, you can drop rows with missing values using df.dropna() or fill missing values using df.fillna()

Perform exploratory data analysis:

<table>
    <thead>
      <tr>
        <th><code> Histgram </code>code></th>
        <th> <code>Pairplot</code> </th>
        <th><code> Heatmap</code></th>
      </tr>
    </thead>
    <tbody>
        <tr>
          <td><code>
            df.hist()                    
            plt.show()</code>          
          </td>
          <td><code>
            sns.pairplot(df)
            plt.show()</code>              
          </td>
          <td><code>
            corr_matrix = df.corr()    
            sns.heatmap(corr_matrix, annot=True)              
            plt.show()</code>           
          </td>
        </tr>
    </tbody>
  </table>


<table>
    <thead>
      <tr>        
        <th><code># Get the unique values in the column </code></th>
        <th><code># Count the occurrences of each category in the column</code> </th>
        <th><code># Create a bar plot to visualize the distribution of categories</code></th>
        <th><code># Group the DataFrame by the column and perform an aggregation</code></th>
        <th><code># Perform statistical analysis for a numerical column based on categories</code></th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>
              <code>
              unique_values = df['column_name'].unique()
              print(unique_values)
              </code>
            </td>
            <td>
             <code> category_counts = df['column_name'].value_counts()
              print(category_counts)</code>
            </td>                      
          <td><code>
              category_counts.plot(kind='bar')
              plt.xlabel('Categories')
              plt.ylabel('Count')
              plt.title('Category Distribution')
              plt.show()</code>
            </td>                 
          <td>
            <code>  grouped_data = df.groupby('column_name').agg({'numerical_column': 'mean'})
              print(grouped_data</code>
            </td>
            <td>
             <code> for category in unique_values:
              category_data = df[df['column_name'] == category]['numerical_column']
              print(f"Category: {category}")
              print(f"Mean: {category_data.mean()}")
              print(f"Standard Deviation: {category_data.std()}")
              print(f"Minimum: {category_data.min()}")
              print(f"Maximum: {category_data.max()}")
              print() </code>
            </td>
        </tr>
    </tbody>
  </table>


This will provide a visual representation of the frequency of each category.

Group and aggregate data based on categories:

<code>
grouped_data = df.groupby('column_name').agg({'numerical_column': 'mean'})
print(grouped_data)
</code>

This will calculate the mean (or any other desired aggregation) of a numerical column for each category.

Perform statistical analysis by category:

# Perform statistical analysis for a numerical column based on categories
# Write a Python program to calculate the sum of all even numbers from 1 to 10.
<code>
sum_of_evens = 0
for num in range(1, 11):
    if num % 2 == 0:
        sum_of_evens += num
 sum_of_evens = sum_of_evens+num
print("Sum of even numbers from 1 to 10:", sum_of_evens)
</code>


# Write a Python program to load data from an Excel/CSV file and print the dataset. Also, write code to print only the records where the value in the "Status" column is "Completed".
<code>

import pandas as pd
</code>

# Assuming the dataset is in a CSV file named 'data.csv'
<code>
data = pd.read_csv('data.csv')
</code>

# Print the entire dataset
<code>
print("Full dataset:")
print(data)
</code>
# Filter records where the value in the "Status" column is "Completed"
<code>
completed_data = data[data['Status'] == 'Completed']
</code>

# Print the filtered dataset
<code>
print("\nFiltered dataset where status is 'Completed':")
print(completed_data)
</code>

# Use the Matplotlib library in Python to create a bar chart and a scatter chart for a given dataset(any). Provide an explanation of the charts and label the axes appropriately.
<code>
import matplotlib.pyplot as plt
</code>

# Sample dataset
<code>
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
</code>

<table>
    <thead>
      <tr>        
        <th></code>Bar chart</code></th>
        <th></code>Scatter chart</code></th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td> 
              <code>
              plt.figure()              
              plt.bar(x, y)
              plt.xlabel('X-axis')
              plt.ylabel('Y-axis')
              plt.title('Bar Chart')
              plt.show()
              </code>
            </td>
            <td>
              <code>
              plt.figure()
              plt.scatter(x, y)
              plt.xlabel('X-axis')
              plt.ylabel('Y-axis')
              plt.title('Scatter Chart')
              plt.show()
              </code>
            </td>                      
        </tr>
    </tbody>
  </table>




# Write an SQL query to select all the records from the "students" table where the "age" column is greater than 19 and less 25 and "cgpa" is greater than 3.5.
<code>

SELECT *
FROM students
WHERE age > 19 AND age < 25 AND cgpa > 3.5;
</code>


------------------------------------------------------------------------------------------------------------------------------------------------------------------
<code>
import numpy as np
</code>

# Create an array of random numbers for demonstration
<code>
data = np.random.randint(0, 100, 10)
</code>

# Define the code snippet you want to measure
<code>
code_snippet = """
</code>

# Aggregation - Calculate the sum, minimum, and maximum values
<code>
sum_value = np.sum(data)
min_value = np.min(data)
max_value = np.max(data)
</code>

# Standard Deviation (Variance) - Calculate the standard deviation and variance
<code>
std_deviation = np.std(data)
variance = np.var(data)
</code>

# Z-score - Calculate the z-scores for each element in the array
<code>
z_scores = (data - np.mean(data)) / np.std(data)
</code>

# Discretization - Convert the data into discrete bins
<code>

num_bins = 5  # Number of bins
bin_edges = np.linspace(np.min(data), np.max(data), num_bins + 1)  # Compute bin edges
discretized_data = np.digitize(data, bin_edges)
"""
</code>




# Execute and measure the execution time of the code snippet
<code>
execution_time = %timeit -r 10 -n 100 -o -q exec(code_snippet)
</code>

# Print the average execution time
<code>
print("Average Execution Time:", execution_time.best)
</code>



<code>
import pandas as pd
import numpy as np
</code>

# Create a sample DataFrame
<code>
data = {
    'A': np.random.randint(0, 100, 10),
    'B': np.random.randint(0, 100, 10),
    'C': np.random.randint(0, 100, 10)
}
df = pd.DataFrame(data)
print("DataFrame:")
print(df)
</code>code>

# Aggregation - Calculate the sum, minimum, and maximum values of column 'A'
<code>
sum_value = df['A'].sum()
min_value = df['A'].min()
max_value = df['A'].max()
print("Sum of column A:", sum_value)
print("Minimum of column A:", min_value)
print("Maximum of column A:", max_value)
</code>

# Standard Deviation (Variance) - Calculate the standard deviation and variance of column 'B'
<code>
std_deviation = df['B'].std()
variance = df['B'].var()
print("Standard Deviation of column B:", std_deviation)
print("Variance of column B:", variance)
</code>

# Z-score - Calculate the z-scores for each element in column 'C'
<code>
z_scores = (df['C'] - df['C'].mean()) / df['C'].std()
print("Z-scores of column C:")
print(z_scores)
</code>




# Create a sample dataframe
<code>
data = pd.DataFrame({'Age': [22, 35, 45, 18, 50, 60, 32, 28, 40, 55]})
print("Original Data:")
print(data)
</code>

# Perform equal-width binning
<code>
num_bins = 3
bin_labels = ['Low', 'Medium', 'High']
data['Age_Binned'] = pd.cut(data['Age'], num_bins, labels=bin_labels)

print("\nBinned Data:")
print(data)
</code>

Original Data:
   Age
0   22
1   35
2   45
3   18
4   50
5   60
6   32
7   28
8   40
9   55

Binned Data:
   Age Age_Binned
0   22        Low
1   35        Low
2   45     Medium
3   18        Low
4   50     Medium
5   60       High
6   32        Low
7   28        Low
8   40     Medium
9   55       High

######

# Create a sample dataframe
<code>
data = pd.DataFrame({'Scores': [82, 75, 90, 65, 88, 92, 78, 70, 80, 85]})
print("Original Data:")
print(data)
</code>
# Perform histogram analysis and discretize
<code>
hist, bin_edges = np.histogram(data['Scores'], bins=3)
bin_labels = ['Low', 'Medium', 'High']
data['Scores_Binned'] = pd.cut(data['Scores'], bins=bin_edges, labels=bin_labels, include_lowest=True)
print("\nBinned Data:")
print(data)
</code>

Original Data:
   Scores
0      82
1      75
2      90
3      65
4      88
5      92
6      78
7      70
8      80
9      85

Binned Data:
   Scores Scores_Binned
0      82        Medium
1      75           Low
2      90          High
3      65           Low
4      88        Medium
5      92          High
6      78        Medium
7      70           Low
8      80        Medium
9      85        Medium


# Read the CSV file
<code>
data = pd.read_csv('data.csv')
</code>

# Perform equal-width binning
<code>
num_bins = 3
bin_labels = ['Low', 'Medium', 'High']
data['Salary_Binned'] = pd.cut(data['Salary'], num_bins, labels=bin_labels)
</code>

# Perform histogram analysis and discretize
<code>
hist, bin_edges = np.histogram(data['Salary'], bins=3)
data[['Salary_Histogram_Binned',abc] [= pd.cut(data[['Salary',a]], bins=bin_edges, labels=bin_labels, include_lowest=True)
</code>

# Print the updated dataframe
<code>
print(data)
</code>

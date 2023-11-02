# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

## Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.

## CODE

### Developed by:Yuvarani T
### Register number:212222110057
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()
```
#### Which day of the week has the highest total bill amount?
```
sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")
```
### What is the average tip amount given by smokers and non-smokers?
```
sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")
```
### How does the tip percentage vary based on the size of the dining party?
```
sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")
```
### Which gender tends to leave higher tips?
```
sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")
```
### Is there any relationship between the total bill amount and the day of the week?
```
plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()
```
### How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?
```
sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")
```
### Which dining party size group tends to have the highest average total bill amount?
```
sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")
```
### What is the distribution of tip amounts for each day of the week?
```
sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")
```
### How does the tip amount vary based on the type of service (lunch vs. dinner)?
```
sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")
```
### Is there any correlation between the total bill amount and the tip amount?
```
sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
```
### heatmap
```
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```
## OUPUT
### Initial dataset:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/4b63275a-21ea-4841-967f-75aceb63020d)

### tips.head():
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/5c4bfafa-336c-44f9-97b7-de29440f0e7a)

### tips.info():
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/ed395134-9866-4239-b7cd-a8999cc956c5)

### Barplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/c34791d4-1066-44f7-aa59-f0cdf3cd6a3f)

![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/eb52e63b-ebd8-43ca-9d8f-be9f7b2faed4)

### Boxplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/838717d8-38b4-4b1e-8e9b-23528e84cd19)

![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/1cb2ec85-64a0-4126-af86-6fbe8dda2006)

### Plot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/6d882571-d567-46a7-b4b3-805ee7bb5175)

### Violinplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/93899405-26d8-41b3-8c24-c366aeba45d3)

### Barplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/ca47e6f2-a6ff-4626-b11d-1a40faa19901)

### Boxplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/42428efd-702d-4ca7-aad2-5d21d0a0ed8e)

### Violinplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/6ffdddd4-21a0-42b9-9180-09992fdf77d3)

### Scatterplot:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/828ce86e-ad09-48bf-8c7f-0e6519d39762)

### Heatmap:
![image](https://github.com/Yuvaranithulasingam/ODD2023-Datascience-Ex-09/assets/121418522/a2a19266-65ed-48dd-91d3-9236d72b3f83)

## RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file

# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/ecedfb41-e746-4552-9f20-a6e8db024998)

```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/82970340-ed23-49e3-8065-7b6a847298d3)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/5d7e04f0-dafb-4159-af97-aa86aa05c8c3)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```
![image](https://github.com/user-attachments/assets/41ba1dff-8e81-4139-a49e-4f6667d12f04)

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/25337782-2139-448f-a9da-29cac3201331)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/c497ba26-57fe-40bd-a102-65d4fe622941)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image](https://github.com/user-attachments/assets/15fdc38d-55a2-4b77-ac24-ef3f161c449d)

```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/2e3a2f76-d6b7-4cc7-966b-f0c33dbbaf85)

```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (1).csv")
tit
```
![image](https://github.com/user-attachments/assets/30ff237e-be28-45bf-8f6c-dbad1bd85fc8)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/7a2b5ff0-4f2c-44c6-90c0-920e5a0031b5)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/5a7893ed-fb48-4b9e-af46-574144a7196c)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/05e98ca4-a05c-4b26-9d7a-2dd6f443defe)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/e30a01a1-315f-4e1c-8df3-06277973928e)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/d88ab52a-a14e-455a-9b17-0093927506b9)

```
df=pd.read_csv("/content/titanic_dataset (1).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/c6f71ee2-24e9-4e9b-bbb0-3087233831d2)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/1cd8eae0-bcfb-4a3f-9c60-781c756d0aa4)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/fc1b2902-3ce6-4262-9eab-7d198f2c6c3e)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/5e1280c7-5a15-4470-a6f6-139ef3fc71fe)

```
mart=pd.read_csv("/content/titanic_dataset (1).csv")
mart
```
![image](https://github.com/user-attachments/assets/35bee23c-ec1f-4e3c-a096-25ca7780a8cc)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/072ab36c-9668-4a91-967c-7a037eae10d4)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/2a56da8c-c7a1-4c12-9cae-0ddf8a07aafb)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/02a77015-5c19-41e1-9454-fcfdfdf3c100)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/4520f9b3-2a18-45d1-bdc0-b6af79a8a304)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/097c5450-0f35-41fa-889b-866359e4079f)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/a6fe5741-99c4-4880-9ed6-928948c61680)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/335802ef-6e1a-4069-8f61-09983d2d397c)


```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/73d0dbfb-3b52-473f-8a8f-92dcaee4ac2a)



# Result:
 The program has been executed successfully.

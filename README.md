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
```py
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/c7f7b1fb-586a-467e-82ee-2997f961143f)


```py
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/e171cab6-c8b0-4b3d-b74f-8b1b4f055293)


```py
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/331ac47a-ddaf-4948-8362-50103603016e)


```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]

	@@ -51,9 +51,9 @@ plt.title('Multi-:Line Plot')
plt.xlabel('X-Label')
plt.ylabel('Y-Label')
```
![image](https://github.com/user-attachments/assets/4144bfaf-cbe8-4152-90d5-15ea47e94452)


```py
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()

	@@ -65,9 +65,9 @@ plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/72ace6eb-6b62-4219-8cac-b1670af5be84)


```py
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)

	@@ -77,143 +77,143 @@ plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/d21a04ba-2071-44b8-a7ec-d044f6edee55)


```py
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image](https://github.com/user-attachments/assets/c4514658-29ef-46ef-a7c2-0f601042e7bd)


```py
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/784ec14a-6fe6-46e0-bde8-a420f0a85c40)


```py
import pandas as pd
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/eb611838-3e0b-4ce6-b240-5337294650bb)


```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/feda2f05-7914-427d-bfab-75a2c4008af2)


```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/2d452360-3854-4f08-9c5b-b191aac4ffb0)


```py
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/06455b8f-77b4-4c37-9ead-594c18eab422)


```py
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/b827a800-2a9b-484f-8fc1-7263c8e617e0)


```py
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/43fb43a3-1276-450d-babd-eb1985611b52)


```py
df=pd.read_csv("/content/titanic_dataset (1).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/32138d81-5d51-4108-a8eb-e9545c49da6b)


```py
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/6edb40b8-0791-42df-a50f-4c76a9f842b7)

```py
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/e2526595-27f3-4c51-a6ca-cb25ba17fc4a)

```py
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/5562c300-e2c8-42b1-9912-71cc295e49c4)

```py
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/1b449ca8-fbeb-4b73-88a3-129a0d78ac02)

```py
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/57b2553a-6c52-4df6-bdb5-dc025f09a5a4)

```py
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/879f90b4-ad14-4316-b7cb-34ad575d3687)

```py
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/5fc5e4b0-d84e-4d60-8e19-1dd60dc4a48f)

```py
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/de7bf467-cb3f-44ff-afd1-600589b2884f)

```py
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/cb58fcf1-80bb-4092-b155-bfb06692e087)

```py
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/51c290ae-96ff-4dec-b583-71d832043d9f)

```py
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/62d0e63a-854d-4e1f-a894-14a5089b7daf)


```py
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/1ad83bc7-9e66-478a-9b74-563cb067b848)


# Result:
 The program has been executed successfully.

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
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
<img width="338" alt="image" src="https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/1150690c-5d55-4021-9233-262ce6709c27">

```
df = sns.load_dataset("tips")
df
```
<img width="327" alt="image" src="https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/569a2d14-ab51-42b8-a283-e820efcaf30e">
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
<img width="365" alt="image" src="https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/e80baaaf-329c-40c4-b352-8ff17b0fc5c0">

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/4ce78848-1f66-423f-a089-2d21e620e13c)

```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/f5bba551-600a-4637-b83a-5609247b0730)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/9708b7ee-1b80-482e-8732-9ca3549f7c62)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/d50ee79d-d92a-4639-87c4-7557bc49353f)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/8b0f97e6-887a-480d-856a-6a4f4d6587cd)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/053e3d25-a0c1-4050-a9be-bf3f7a8e25a8)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/fd858e56-162f-4cb2-933f-756f8b275b41)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/b7b9e65f-da9b-4478-89be-0b685bb086d0)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/6809b914-41c7-4509-b26d-5b36394467e9)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/0fd6af5d-13f2-44bc-8c51-3fac53c2659a)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/02db6aff-b4e2-4e81-837c-c004f553eb1c)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/7a687d37-9f63-4b80-adb6-8bb44298a29d)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/f1b68368-fc5a-4388-9ab3-6035ca1bc068)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/e9e19e0a-f814-4a18-92d0-c5f863d4917a)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/1a5f08c3-da33-4dc2-be18-34818d3e1639)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/55e69a20-c26f-4d0d-98a1-74a74f677321)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/f2d68a01-a292-465b-a014-b486057df114)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/6a81ae93-2e25-4324-96fc-e82ab3bb9191)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/5810ee99-74bb-42d1-b0a4-1c6cecbdb1f7)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/ac9da33d-c0e9-420e-9aec-bfc4beb4de48)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/adb3024a-19a9-4aa4-a7ca-a9ae8dfe898d)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/8c866a9c-a44d-46dd-a77a-fab3c5439678)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/ca15b067-a509-45c5-98bf-dcdbccc89dea)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/KayyuruTharani/EXNO-6-DS/assets/142209319/324a8ef9-1495-4c1c-baa2-3371f8732e87)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.



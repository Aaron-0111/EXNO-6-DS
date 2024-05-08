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
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/c70a72b8-4bd8-4e50-a73c-de31d13846e0)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/98a1b520-54ae-40ba-8422-86ccec3a52ef)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/02274024-760f-4fa3-8b5a-4be12aa7843e)

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
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/54e00e72-983c-4f69-a292-f308f1f88815)

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

![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/ddca1615-5374-463f-82e7-42cf2657027a)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/ed1b9886-c8c5-423d-bc45-a1e2d721d039)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/278f0e20-642e-40e7-a29c-a69d121f3f54)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/d67422f3-91fb-47b8-924d-0506dc74d744)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/50c3ff76-8e9f-4640-a349-3f31d5ede790)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/d45944f2-73b3-481d-9126-5198108e2c90)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/9f2e7529-d61d-4822-9dba-5221ad1a7986)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/1326fa8a-8d2b-4de5-9e20-258541786fca)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/903f3dc6-04ba-40b7-b61d-f00ecb836980)

```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/9503be1c-d5aa-4c19-9b14-3a594dc9b6d3)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/091116dd-e8a3-4057-9eb9-2f1fdef5fa4f)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/fb15f822-a553-4472-8086-982358c0aa43)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/eac17d85-eb26-4afd-8953-d8dfdcee6737)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/dc98c95f-fe20-47ba-9f49-374ee8e90862)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/ecb14f2c-1746-46bf-84ea-97e6d283f859)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/3e92398d-a20e-4bac-9a58-f834adbe96b9)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/b02fe195-a4b9-46a0-98b3-ad89ee1164b5)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/e7a6d9e8-aee7-4fea-b043-4ff9e07d3a4c)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/91f9fe74-598b-4f91-86e6-9f5f01e934fc)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/29425c11-0100-46d2-b94b-463624cc16a8)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/c9e7c7ce-60e2-4cdf-87ce-e7effec99ccd)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/3cc596f3-cf26-40cb-aa4f-01cccf758106)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/Aaron-0111/EXNO-6-DS/assets/149347631/9fbf0324-3ba6-447b-b034-2400d8f55bfd)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.



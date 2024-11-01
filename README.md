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
![381045756-ed650120-a48b-474f-a6c2-1ce665a10e34](https://github.com/user-attachments/assets/473e9df5-999b-472a-9982-c48a1017c84c)
```
df = sns.load_dataset("tips")
df
```
![381045876-990d80cf-5a93-47e3-aeea-8b5ec6842ad8](https://github.com/user-attachments/assets/4952f890-8ea7-47a5-a9b2-706b1531b902)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex",linestyle='solid', legend="auto")
```
![381046175-16960a93-4c20-4219-9c55-d2b9cbe5ae53](https://github.com/user-attachments/assets/7efdcbd2-6b66-4c77-99c6-7b1eec7a0eec)
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
![381046309-843da908-7e52-423f-aa32-151320f851e1](https://github.com/user-attachments/assets/969781ef-b8bb-4564-9273-573fc912a565)
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
![381046468-dfa456af-1bdc-4e43-8992-fbdf6ce320b9](https://github.com/user-attachments/assets/97a1748a-7fe7-4c80-b7de-8541140283cf)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![381046631-9ab3317b-99a2-4c09-b136-536b33e0c8e9](https://github.com/user-attachments/assets/84ef7a94-7a9d-4b42-a2e0-2180576a5ec6)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![381046707-802f4453-8ae8-49f3-b286-9d59c42d5492](https://github.com/user-attachments/assets/6b3728a4-85a3-47cb-b341-46fcf04b586e)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![381046905-72837406-9a13-4b35-8dfd-801e1c34ecab](https://github.com/user-attachments/assets/15be4d71-d170-4b97-a0ad-d1a3424cd427)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![381047124-3f2bf7ce-7bce-4e3f-b188-f50f34be8cd5](https://github.com/user-attachments/assets/9e707a4e-710e-4a9f-85f4-cb4336e51796)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![381047230-7c710728-76c5-479e-ba3b-ac32cf74e087](https://github.com/user-attachments/assets/fc868a90-c62f-4dc2-8e52-2de222a360e5)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![381047381-7295c198-b25a-487f-8eae-db695fa7f6c0](https://github.com/user-attachments/assets/8aa65a81-6ae2-4c08-8ce8-77495cb0fb74)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![381047522-f862f27e-35a5-43d8-ac16-2797cd9270ad](https://github.com/user-attachments/assets/65c08328-60a2-4428-baab-906921b2c443)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![381047737-e1c716cf-b44a-4163-94ff-2d51d7e0f6fe](https://github.com/user-attachments/assets/2f4cc88b-77f2-44b7-a6cd-19ea9eddeb5a)
```
sns.histplot(data = num_var, kde = True)
```
![381047839-f48073f1-8bf0-464d-be1e-5bdce3d7d103](https://github.com/user-attachments/assets/01894122-3236-4009-b7a8-3f0ada35b019)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![381047969-7f14cdfc-a46d-4ba6-8b0e-f79357a028b7](https://github.com/user-attachments/assets/77cbe190-de17-4b37-826a-25b8aacd5e15)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![381048286-cacf6d7f-ac39-42c3-aba4-ce70599b5c5d](https://github.com/user-attachments/assets/b90d2081-e1b3-4977-bcb4-e269013c0605)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![381048434-aff2d474-32b5-4b27-a303-46ef5d7550c9](https://github.com/user-attachments/assets/8206fb11-0d64-4c6c-b0f2-4ccf28a983a2)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![381048612-f63a259e-4da7-4bc9-ac7a-2b91d1d35d72](https://github.com/user-attachments/assets/33d7e437-1b56-49c0-8153-25b018639983)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![381048755-47c2a171-5787-4849-8b97-f752e1f746cb](https://github.com/user-attachments/assets/c79cb71c-9475-467e-9f41-121a7c266698)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![381048870-7f638def-9200-4085-90f4-a58e75b9d04d](https://github.com/user-attachments/assets/d2a89d34-db30-4434-87de-704edf475bf6)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![381048928-4dc3d976-c133-4455-a22a-110129cb47c6](https://github.com/user-attachments/assets/fc7c4f90-db8c-4baf-bd83-0d43e5d84fc9)
```
sns.kdeplot(data=mart,x='Age')
```
![381049332-95d5b4ac-cea7-41d8-b427-6a3e4f713cf9](https://github.com/user-attachments/assets/9f25ade2-9070-41a7-81a6-8b8ff1d3387d)
```
sns.kdeplot(data=mart)
```
![381049432-73ed2d20-55cd-4dc0-8d0a-35e990d65b77](https://github.com/user-attachments/assets/8dc85919-8f70-45e1-9f9b-edeb111e9b2a)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![381049505-8d3e132c-d001-4361-85e6-8b6b69a6757c](https://github.com/user-attachments/assets/87bfa26e-e371-4840-a6a7-288f85d534dc)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![381049656-504b6523-79b1-4b92-ad70-06963ffcfa3f](https://github.com/user-attachments/assets/42e973e5-f21f-49f0-8408-b1b41f89f51b)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![381049737-3dd909fe-cc73-429b-be4f-fc4222d7d97a](https://github.com/user-attachments/assets/4026981d-8f6e-4b12-a9db-6f67ed544104)
```
hm=sns.heatmap(data=data)
```
![381049831-4a8f04f8-a4e2-425d-a87e-a74cd78d2f9a](https://github.com/user-attachments/assets/c8c4e4b4-ace3-47a5-aeb0-b5e9bb02aa0c)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.

## EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/63e2015e-246c-4d2a-8833-19a65b11b00a)

```
df=sns.load_dataset('tips')
df
```
![image](https://github.com/user-attachments/assets/bf9d6aa9-adfe-4e90-af70-113a818df621)

```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/user-attachments/assets/311d34f7-86ed-42fb-b4b8-9e3f925c7e65)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')

```
![image](https://github.com/user-attachments/assets/9fff3619-db6b-4ffe-8310-d4b522bd4a60)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![image](https://github.com/user-attachments/assets/0f5799e4-9cc7-45f0-a1f4-0ef2afe32160)

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
![image](https://github.com/user-attachments/assets/457cb2c9-070a-43ca-960a-dd9962a54235)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image](https://github.com/user-attachments/assets/dbd53904-5668-4e03-ba55-17f8b62bd1c0)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/abaa6558-a056-4c3e-96a0-25ac6d73d547)

```
file_path = "/content/titanic_dataset (1).csv" 
tit = pd.read_csv(file_path)
tit
```
![image](https://github.com/user-attachments/assets/5ff6c8d6-c1c1-4b39-8f97-554a8696bd63)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/b1003a78-76a9-4a7f-98f5-810cb1ffe874)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![image](https://github.com/user-attachments/assets/3838f87d-499e-42ab-b282-d35a6b11f455)

```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/user-attachments/assets/967e9726-f849-42ca-a53d-10f13684d33c)

```
import seaborn as sns
import numpy as np
import pandas as pd

num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

![image](https://github.com/user-attachments/assets/9f1c6ee9-c9bb-4e47-a2c5-8cf7cfdd4ae9)

```
sns.histplot(data = num_var, kde = True)
```

![image](https://github.com/user-attachments/assets/f5473574-c176-47a5-8763-2dcce694572d)

```
/content/titanic_dataset (1).csv
```
![image](https://github.com/user-attachments/assets/6ad8d2c7-4b54-481a-9e30-5ccba6d0de50)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![image](https://github.com/user-attachments/assets/df705770-bc49-4637-a655-1786a1b843b3)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![image](https://github.com/user-attachments/assets/d68b46e2-36b4-4344-aa0e-b86b75dcba5f)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/311acca3-ae6b-4157-934f-726262c31c4f)

```
mart=pd.read_csv("/content/titanic_dataset (1).csv")
mart
```
![image](https://github.com/user-attachments/assets/c4444a22-4b84-429f-a5e2-3b3fa932d124)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/21f79067-b822-4de8-8411-de7459ce0ff1)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/86f1c5e0-1568-48ed-91cf-04d2bc047ad6)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/30ea3e32-6cb2-4ae9-aff4-3ef0abb73b91)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/0ec2f10a-7c9d-478d-b063-5f2155548d42)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/80d9bc2b-40cb-44ea-a43a-252ce26f3914)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/user-attachments/assets/067b68b0-2948-48c8-84f2-f268586afbe1)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/ba221b43-5c84-44fc-bc14-181a0127d94e)

```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/c7369a38-4444-4095-8264-9e7dde835e0a)





# Result:
Thus, all the data visualization techniques of seaborn has been implemented.

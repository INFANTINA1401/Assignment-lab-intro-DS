# Assignment-lab-intro-DS
# NAME: INFANTINA MARIA L
# REG: 212223100013
# DEPT: CSE [CYBER SECURITY]
# AIM:
To write a python program for inserting columns, rows and changing these etc.
# PROGRAM AND OUTPUT:
```
1.
import pandas as pd
data=[['alex',10],['bob',10]]
df=pd.DataFrame(data,columns=['Name','Age'])
print(df)

OUTPUT:
   Name  Age
0  alex   10
1   bob   10

2.
import pandas as pd
df=pd.DataFrame({"a":[1,2,3],"b":[2,3,4],"c":[4,5,6]},index=[1,2,3])
print(df)

OUTPUT:
   a  b  c
1  1  2  4
2  2  3  5
3  3  4  6

3.
import pandas as pd
df=pd.DataFrame({'car':["bmw","volvo"],'passing':[3,7]},index=[1,2])
print(df)

OUTPUT:
     car  passing
1    bmw        3
2  volvo        7

4.
import pandas as pd
data=[{'a':1,'b':2},{'a':3,'b':10,'c':20}]
df=pd.DataFrame(data)
print(df)

OUTPUT:
   a   b     c
0  1   2   NaN
1  3  10  20.0

5.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
address=['america','london','swizterland']
df["Address"]=address
print(df)

OUTPUT:
     Name  height qualification      Address
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland

6.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
address=['america','london','swizterland']
df["Address"]=address
print(df)
del df["Address"]
print(df)

OUTPUT:
     Name  height qualification      Address
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE

7.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
address=['america','london','swizterland']
df["Address"]=address
print(df)
del df["Address"]
print(df)
df.drop(['height'],axis=1,inplace=True)
print(df)

OUTPUT:
     Name  height qualification      Address
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE
     Name qualification
0    arul            BE
1   maria            BE
2  dharsh            BE

8.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
address=['america','london','swizterland']
df["Address"]=address
print(df)
del df["Address"]
print(df)
df.drop(['height'],axis=1,inplace=True)
print(df)
df.pop("Name")
print(df)

OUTPUT:
     Name  height qualification      Address
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE
     Name qualification
0    arul            BE
1   maria            BE
2  dharsh            BE
  qualification
0            BE
1            BE
2            BE

9.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
address=['america','london','swizterland']
df["Address"]=address
print(df)
df.rename(columns={'Address':'place'},inplace=True)
print(df)

OUTPUT:
     Name  height qualification      Address
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland
     Name  height qualification        place
0    arul     5.7            BE      america
1   maria     5.6            BE       london
2  dharsh     5.5            BE  swizterland

10.
import pandas as pd
df=pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2=pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=pd.concat([df,df2])
print(df)

OUTPUT:
   a  b
0  1  2
1  3  4
0  5  6
1  7  8

11.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
print(df)
df.drop(0,axis=0,inplace=True)
print(df)

OUTPUT:
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE
     Name  height qualification
1   maria     5.6            BE
2  dharsh     5.5            BE

12.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df=df['Name']
print(df)

OUTPUT:
0      arul
1     maria
2    dharsh
Name: Name, dtype: object

13.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
print(df[['Name','qualification']])

OUTPUT:
     Name qualification
0    arul            BE
1   maria            BE
2  dharsh            BE

14.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df.filter(like='eigh') #column with eigh
df.filter(items=['Name','qualification']) #both name and qualification
df.filter(regex='a|e',axis=1) #column with a or e

OUTPUT:
	Name 	height 	qualification
0 	arul 	5.7 	BE
1 	maria 	5.6 	BE
2 	dharsh 	5.5 	BE

15.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df=df.drop_duplicates('height')
print(df)

OUTPUT:
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE

16.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df=df.drop_duplicates()
print(df)

OUTPUT:
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE

17.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=['Name','height'])
print(df)

OUTPUT:
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE

18.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df=df.drop_duplicates(subset=['Name','height'],keep='last') #deletes the first duplicate and keeps the last
print(df)

OUTPUT:
     Name  height qualification
0    arul     5.7            BE
1   maria     5.6            BE
2  dharsh     5.5            BE

19.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df_sample=df.sample(n=2)
print(df_sample)

OUTPUT:
     Name  height qualification
2  dharsh     5.5            BE
1   maria     5.6            BE

20.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df_sample=df.sample(frac=0.5)
print(df_sample)

OUTPUT:
     Name  height qualification
2  dharsh     5.5            BE
0    arul     5.7            BE

21.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'qualification':['BE','BE','BE']}
df=pd.DataFrame(data)
df_sample=df.sample(n=2,axis=1)
print(df_sample)

OUTPUT:
  qualification  height
0            BE     5.7
1            BE     5.6
2            BE     5.5

22.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'salary':[70000,80000,90000]}
df=pd.DataFrame(data)
top_salary=df.nlargest(2,columns='salary')
print(top_salary)

OUTPUT:
     Name  height  salary
2  dharsh     5.5   90000
1   maria     5.6   80000

23.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'salary':[70000,80000,90000]}
df=pd.DataFrame(data)
top_salary=df.nsmallest(2,columns='salary')
print(top_salary)

OUTPUT:
    Name  height  salary
0   arul     5.7   70000
1  maria     5.6   80000

24.
import pandas as pd
data={'Name':['arul','maria','dharsh'],'height':[5.7,5.6,5.5],'salary':[70000,80000,90000]}
df=pd.DataFrame(data)
df=df.query('height>5.6')
print(df)

OUTPUT:
   Name  height  salary
0  arul     5.7   70000

25.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78]}
df=pd.DataFrame(data)
df=df.query('Name.str.contains("a")and height>1.7')#checking condition ,and
print(df)

OUTPUT:
   Name  age  height
2  uday   40    1.78

26.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df=df.query('gender==["f","m"]and height<=1.65')
print(df)

OUTPUT:
   Name  age  height gender
0  arul   23    1.62      f
1  tina   24    1.65      f

27.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df.loc[:,'age']

OUTPUT:
0    23
1    24
2    40
Name: age, dtype: int64

28.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df.iloc[:,1]

OUTPUT:
0    23
1    24
2    40
Name: age, dtype: int64

29.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df.loc[:,['Name','age']]

OUTPUT:
	Name 	age
0 	arul 	23
1 	tina 	24
2 	uday 	40

30.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df_filtered=df[df['age']>30]
print(df_filtered)

OUTPUT:
   Name  age  height gender
2  uday   40    1.78      f

31.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df_filtered=df[df['Name'].str.startswith(('a','u'))]
print(df_filtered)

OUTPUT:
   Name  age  height gender
0  arul   23    1.62      f
2  uday   40    1.78      f

32.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
print(df.tail(2))

OUTPUT:
   Name  age  height gender
1  tina   24    1.65      f
2  uday   40    1.78      f

33.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
print(df.head(2))

OUTPUT:
   Name  age  height gender
0  arul   23    1.62      f
1  tina   24    1.65      f

34.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df.info()

OUTPUT:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3 entries, 0 to 2
Data columns (total 4 columns):
 #   Column  Non-Null Count  Dtype  
---  ------  --------------  -----  
 0   Name    3 non-null      object 
 1   age     3 non-null      int64  
 2   height  3 non-null      float64
 3   gender  3 non-null      object 
dtypes: float64(1), int64(1), object(2)
memory usage: 228.0+ bytes

35.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df.describe()

OUTPUT:
	age 	height
count 	3.000000 	3.000000
mean 	29.000000 	1.683333
std 	9.539392 	0.085049
min 	23.000000 	1.620000
25% 	23.500000 	1.635000
50% 	24.000000 	1.650000
75% 	32.000000 	1.715000
max 	40.000000 	1.780000

36.
import pandas as pd
data={'Name':['arul','tina','uday'],'age':[23,24,40],'height':[1.62,1.65,1.78],'gender':["f","f","f"]}
df=pd.DataFrame(data)
df_sorted=df.sort_values(by='age',ascending=False) #name of rows =index # object is string
print(df_sorted)

OUTPUT:
   Name  age  height gender
2  uday   40    1.78      f
1  tina   24    1.65      f
0  arul   23    1.62      f

37.
import pandas as pd
data={'Name':['arul','tina','uday','ram','rahul'],'age':[23,24,26,27,25],'gender':["f","f","f","m","m"],'salary':[100000,90000,80000,70000,90000]}
df=pd.DataFrame(data)
grouped=df.groupby('gender')['salary'].mean()
print(grouped)

OUTPUT:
gender
f    90000.0
m    80000.0
Name: salary, dtype: float64

```
# RESULT:
Thus we performed our required program.

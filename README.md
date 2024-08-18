# Assignment-lab-intro-DS
# NAME: V MYTHILI
# DEPT: CSE
# AIM:
To write a python program for inserting columns, rows and changing these etc.
# PROGRAM AND OUTPUT:
```
import pandas as pd
df = pd.DataFrame(
    {"a" : [4, 5, 6],
     "b" : [7, 8, 9],
     "c" : [10, 11, 12]},
    index = [1, 2, 3]
)
print(df)
   a  b   c
1  4  7  10
2  5  8  11
3  6  9  12

[ ]
import pandas as pd
df = pd.DataFrame(
    [[4,7,10],[5,8,11],[6,9,12]],index=[1,2,3],columns=["a","b","c"])
print(df)
   a  b   c
1  4  7  10
2  5  8  11
3  6  9  12

[ ]
import pandas as pd
data=[1,2,3,4]
df = pd.DataFrame(data)
print(df)
   0
0  1
1  2
2  3
3  4

[ ]
import pandas as pd
data = [['Alex',10],['Bob',12]]
df = pd.DataFrame(data,columns=['Name','Age'])
print(df)
   Name  Age
0  Alex   10
1   Bob   12

[ ]
import pandas as pd
data = {'Name':['Tom','Jack','Steve','Ricky'],'Age':[28,34,29,42]}
df = pd.DataFrame(data)
print(df)
    Name  Age
0    Tom   28
1   Jack   34
2  Steve   29
3  Ricky   42

[ ]
import pandas as pd
mydataset={
    'cars':["BMW","Volvo","Ford"],
    'passings':[3,7,2]
}
myvar=pd.DataFrame(mydataset)
print(myvar)
    cars  passings
0    BMW         3
1  Volvo         7
2   Ford         2

[ ]
import pandas as pd
data=[{'a':1,'b':2},{'a':5,'b ':10,'c':20}]
df=pd.DataFrame(data)
df


[ ]
import pandas as pd
df = pd.DataFrame(data,index=['first','second'])
df


[ ]
import pandas as pd
df1 = pd.DataFrame(data,index=['first','second'],columns=['a','b'])
df1


[ ]
import pandas as pd
data={'Name':['jai','princi','Gaurav','Anuj'],'Height':[5.1,6.2,5.1,5.2],'Qualification':['Msc','MA','Msc','Msc']}
df = pd.DataFrame(data)
address=['Delhi','Bangalore','Chennai','Patna']
df['Address']=address
df


[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],'Address':['Delhi','Kanpur','Allahabad','Kannauj'],
        'Qualification':['Msc','MA','MCA','Phd'],'address':['Delhi','Bangalore','Chennai','Patna']}
df = pd.DataFrame(data)
del df['Address']
df




[ ]
df.drop(['Address'],axis=1,inplace=True)
df


[ ]
df.pop('Age')
df


[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],'Address':['Delhi','Kanpur','Allahabad','Kannauj'],
        'Qualification':['Msc','MA','MCA','Phd']}
df = pd.DataFrame(data)
print(df)
df.rename(columns={'Address':'place'},inplace=True)
df



[ ]
import pandas as pd
df = pd.DataFrame([[1,2],[3,4]],columns=['a','b'])
df2= pd.DataFrame([[5,6],[7,8]],columns=['a','b'])
df=pd.concat([df,df2])
df


[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],'Address':['Delhi','Kanpur','Allahabad','Kannauj'],
        'Qualification':['Msc','MA','MCA','Phd']}
df = pd.DataFrame(data)
df
df.drop(1,axis=0,inplace=True)
df




[ ]
import pandas as pd
data = {'name':['Alice','Bob'],'age':[25,32],'gender':['F','M'],'height':[1.2,5.6]}
df = pd.DataFrame(data)
df = df['name']
print(df)
0    Alice
1      Bob
Name: name, dtype: object

[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],'Address':['Delhi','Kanpur','Allahabad','Kannauj'],
        'Qualification':['Msc','MA','MCA','Phd']}
df = pd.DataFrame(data)
print(df[['Name','Qualification']])
     Name Qualification
0     Jai           Msc
1  Princi            MA
2  Gaurav           MCA
3    Anuj           Phd

[ ]
import pandas as pd
data = {'name':['tara','Bob'],'age':[25,32],'gender':['F','M'],'height':[1.2,5.6]}
df = pd.DataFrame(data)
#df.filter(items=['name','age'])
df.filter(like='eigh')
#df.filter(regex='e|a',axis=1)
print(df)
   name  age gender  height
0  tara   25      F     1.2
1   Bob   32      M     5.6

[ ]
import pandas as pd
data = {'name':['Alice','Bob'],'age':[25,32],'gender':['F','M'],'height':[1.2,5.6]}
#df = pd.DataFrame(data)
df.filter(like='eigh')
#df.filter(regex='e|a',axis=1)
print(df)
    name  age gender  height
0  Alice   25      F     1.2
1    Bob   32      M     5.6

[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],'Address':['Delhi','Kanpur','Allahabad','Kannauj'],
        'Qualification':['Msc','MA','MCA','Phd']}
df.filter(regex='e|a',axis=1)
print(df)
     Name  Age    Address Qualification
0     Jai   27      Delhi           Msc
1  Princi   24     Kanpur            MA
2  Gaurav   22  Allahabad           MCA
3    Anuj   32    Kannauj           Phd

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','Alice'],'age':[25,32,18,25],'gender':['F','M','M','F'],'height':[1.2,5.6,2.3,1.2]}
df = pd.DataFrame(data)
df = df.drop_duplicates()
df


[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','Alice'],'age':[25,32,18,26],'gender':['F','M','M','F'],'height':[1.2,5.6,2.3,1.2]}
df = pd.DataFrame(data)
df = df.drop_duplicates(['name','age'])
df


[ ]
import pandas as pd
data = {'name':['Alice','Bob','Bob','Alice'],'age':[25,18,18,26],'gender':['F','M','M','F'],'height':[1.2,5.6,2.3,1.2]}
df = pd.DataFrame(data)
df = df.drop_duplicates(subset=['name','age'])
df



[ ]
import pandas as pd
data = {'name':['Alice','Bob','Bob','Alice'],'age':[25,18,18,26],'gender':['F','M','F','F'],'height':[1.2,5.6,2.3,1.2]}
df = pd.DataFrame(data)
df = df.drop_duplicates(subset=['name','age'],keep='last')
df


[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],
        'Qualification':['Msc','MA','MCA','Phd']}
df = pd.DataFrame(data)
df_sample = df.sample(n=2)
print(df_sample)
     Name  Age Qualification
1  Princi   24            MA
3    Anuj   32           Phd

[ ]
import pandas as pd
data = {'Name':['Jai','Princi','Gaurav','Anuj'],'Age':[27,24,22,32],
        'Qualification':['Msc','MA','MCA','Phd']}
df = pd.DataFrame(data)
df_sample = df.sample(frac=0.5)
print(df_sample)
     Name  Age Qualification
2  Gaurav   22           MCA
1  Princi   24            MA

[ ]
 import pandas as pd
 data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000]}
 df = pd.DataFrame(data)
 top_salary = df.nlargest(2,columns='salary')
 print(top_salary)

    name  age  salary
4  Emily   45   90000
3  David   40   80000

[ ]
 import pandas as pd
 data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000]}
 df = pd.DataFrame(data)
 top_salary = df.nsmallest(2,columns='salary')
 print(top_salary)
    name  age  salary
0  Alice   25   50000
1    Bob   30   60000

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df=df.query('name.str.contains("a") and height >1.7')
print(df)
    name  age gender  height
3  David   40      M    1.83

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df = df.query('age >= 30')
print(df)
      name  age gender  height
1      Bob   30      M    1.78
2  Charlie   35      M    1.63
3    David   40      M    1.83
4    Emily   45      F    1.72

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df = df.query('gender == ["F","M"] and height <= 1.65')
print(df)

      name  age gender  height
0    Alice   25      F    1.62
2  Charlie   35      M    1.63

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df.loc[:,'age']


[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df.loc[:,['name','age']]


[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df.iloc[:,0]


[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df_filtered = df[df['age'] > 30]
print(df_filtered)
      name  age gender  height
2  Charlie   35      M    1.63
3    David   40      M    1.83
4    Emily   45      F    1.72

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df_filtered = df[(df['gender'] == 'M') & (df['height'] > 1.5)]
print(df_filtered)
      name  age gender  height
1      Bob   30      M    1.78
2  Charlie   35      M    1.63
3    David   40      M    1.83

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],
         'age':[25,30,35,40,45],
         'gender':['F','M','M','M','F'],
         'height':[1.62,1.78,1.63,1.83,1.72]}
df = pd.DataFrame(data)
df_filtered = df[df['name'].str.startswith(('A','C'))]
print(df_filtered)
      name  age gender  height
0    Alice   25      F    1.62
2  Charlie   35      M    1.63

[ ]
 import pandas as pd
 data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000],'gender':['F','M','M','M','F']}
 df = pd.DataFrame(data)
 print(df.tail(3))
      name  age  salary gender
2  Charlie   35   70000      M
3    David   40   80000      M
4    Emily   45   90000      F

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000],'gender':['F','M','M','M','F']}
df = pd.DataFrame(data)
print(df.head(2))
    name  age  salary gender
0  Alice   25   50000      F
1    Bob   30   60000      M

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000],'gender':['F','M','M','M','F']}
df = pd.DataFrame(data)
df.info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 5 entries, 0 to 4
Data columns (total 4 columns):
 #   Column  Non-Null Count  Dtype 
---  ------  --------------  ----- 
 0   name    5 non-null      object
 1   age     5 non-null      int64 
 2   salary  5 non-null      int64 
 3   gender  5 non-null      object
dtypes: int64(2), object(2)
memory usage: 288.0+ bytes

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000],'gender':['F','M','M','M','F']}
df = pd.DataFrame(data)
print(df.describe())
             age        salary
count   5.000000      5.000000
mean   35.000000  70000.000000
std     7.905694  15811.388301
min    25.000000  50000.000000
25%    30.000000  60000.000000
50%    35.000000  70000.000000
75%    40.000000  80000.000000
max    45.000000  90000.000000

[ ]
import pandas as pd
data = {'name':['Alice','Bob','Charlie','David','Emily'],'age':[25,30,35,40,45],'salary':[50000,60000,70000,80000,90000],'gender':['F','M','M','M','F']}
df = pd.DataFrame(data)
df_sorted = df.sort_values(by='age',ascending=False)
print(df_sorted)
      name  age  salary gender
4    Emily   45   90000      F
3    David   40   80000      M
2  Charlie   35   70000      M
1      Bob   30   60000      M
0    Alice   25   50000      F
```
# RESULT:
Thus we performed our required program.

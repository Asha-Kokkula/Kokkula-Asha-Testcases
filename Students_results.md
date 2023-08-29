```python
import pandas as pd
df2=pd.DataFrame({"names":['vineet','hisham','raj','ajeet','sujit','ramesh','priya','priyanka','suresh','ritesh','hitesh','jatin','chitesh','suman','raman','aman','ravi','shravi','chavvi','himanshu'],"rno":['1','2','3','4','5','6','7','8','9','10','11','12','13','14','15','16','17','18','19','20']})
df3=pd.DataFrame({"results":['fail','fail','pass','pass','fail','pass','fail','pass','pass','pass','pass','fail','fail','fail','pass','fail','pass','fail','pass','pass'],"rno":['1','2','3','4','5','6','7','8','9','10','11','12','13','14','15','16','17','18','19','20']})

```


```python
df2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>names</th>
      <th>rno</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vineet</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>hisham</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>raj</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ajeet</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>sujit</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ramesh</td>
      <td>6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>priya</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>priyanka</td>
      <td>8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>suresh</td>
      <td>9</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ritesh</td>
      <td>10</td>
    </tr>
    <tr>
      <th>10</th>
      <td>hitesh</td>
      <td>11</td>
    </tr>
    <tr>
      <th>11</th>
      <td>jatin</td>
      <td>12</td>
    </tr>
    <tr>
      <th>12</th>
      <td>chitesh</td>
      <td>13</td>
    </tr>
    <tr>
      <th>13</th>
      <td>suman</td>
      <td>14</td>
    </tr>
    <tr>
      <th>14</th>
      <td>raman</td>
      <td>15</td>
    </tr>
    <tr>
      <th>15</th>
      <td>aman</td>
      <td>16</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ravi</td>
      <td>17</td>
    </tr>
    <tr>
      <th>17</th>
      <td>shravi</td>
      <td>18</td>
    </tr>
    <tr>
      <th>18</th>
      <td>chavvi</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>himanshu</td>
      <td>20</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>results</th>
      <th>rno</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>fail</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>fail</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>pass</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>pass</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>fail</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>pass</td>
      <td>6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>fail</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>pass</td>
      <td>8</td>
    </tr>
    <tr>
      <th>8</th>
      <td>pass</td>
      <td>9</td>
    </tr>
    <tr>
      <th>9</th>
      <td>pass</td>
      <td>10</td>
    </tr>
    <tr>
      <th>10</th>
      <td>pass</td>
      <td>11</td>
    </tr>
    <tr>
      <th>11</th>
      <td>fail</td>
      <td>12</td>
    </tr>
    <tr>
      <th>12</th>
      <td>fail</td>
      <td>13</td>
    </tr>
    <tr>
      <th>13</th>
      <td>fail</td>
      <td>14</td>
    </tr>
    <tr>
      <th>14</th>
      <td>pass</td>
      <td>15</td>
    </tr>
    <tr>
      <th>15</th>
      <td>fail</td>
      <td>16</td>
    </tr>
    <tr>
      <th>16</th>
      <td>pass</td>
      <td>17</td>
    </tr>
    <tr>
      <th>17</th>
      <td>fail</td>
      <td>18</td>
    </tr>
    <tr>
      <th>18</th>
      <td>pass</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>pass</td>
      <td>20</td>
    </tr>
  </tbody>
</table>
</div>




```python
#
combined_df=pd.merge(df2,df3, on='rno')
combined_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>names</th>
      <th>rno</th>
      <th>results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vineet</td>
      <td>1</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>1</th>
      <td>hisham</td>
      <td>2</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>2</th>
      <td>raj</td>
      <td>3</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ajeet</td>
      <td>4</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>4</th>
      <td>sujit</td>
      <td>5</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ramesh</td>
      <td>6</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>6</th>
      <td>priya</td>
      <td>7</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>7</th>
      <td>priyanka</td>
      <td>8</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>8</th>
      <td>suresh</td>
      <td>9</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ritesh</td>
      <td>10</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>10</th>
      <td>hitesh</td>
      <td>11</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>11</th>
      <td>jatin</td>
      <td>12</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>12</th>
      <td>chitesh</td>
      <td>13</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>13</th>
      <td>suman</td>
      <td>14</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>14</th>
      <td>raman</td>
      <td>15</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>15</th>
      <td>aman</td>
      <td>16</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ravi</td>
      <td>17</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>17</th>
      <td>shravi</td>
      <td>18</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>18</th>
      <td>chavvi</td>
      <td>19</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>19</th>
      <td>himanshu</td>
      <td>20</td>
      <td>pass</td>
    </tr>
  </tbody>
</table>
</div>




```python
#1. Problem statement 
#Analyse the given datasets and print the student names who have successfully cleared the exam. 

passed_students_names=combined_df[combined_df['results']== 'pass']['names']
print("passed students names :","\n",passed_students_names)
```

    passed students names : 
     2          raj
    3        ajeet
    5       ramesh
    7     priyanka
    8       suresh
    9       ritesh
    10      hitesh
    14       raman
    16        ravi
    18      chavvi
    19    himanshu
    Name: names, dtype: object
    


```python
#2.Problem
#Count Number Of Students(Pass/Fail)

z=combined_df["names"].count()
print("Count of students :","\n",z)
```

    Count of students : 
     20
    


```python
#3.Problem
#Arrange Student Names Apla Based
names_alphabetic=combined_df["names"].sort_values()
print("students names in alphabetic order :","\n",names_alphabetic)
```

    students names in alphabetic order : 
     3        ajeet
    15        aman
    18      chavvi
    12     chitesh
    19    himanshu
    1       hisham
    10      hitesh
    11       jatin
    6        priya
    7     priyanka
    2          raj
    14       raman
    5       ramesh
    16        ravi
    9       ritesh
    17      shravi
    4        sujit
    13       suman
    8       suresh
    0       vineet
    Name: names, dtype: object
    


```python

```

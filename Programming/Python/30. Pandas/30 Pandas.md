


  
For better handling of CSV files and performing operations on them “Pandas” library is used. It's a powerful tool for data analysis.  
  

```python
import pandas  
  
data = pandas.read\_csv('text.csv')  
------------------------------  
  
         day  temp condition  
0     Monday    12     Sunny  
1    Tuesday    14      Rain  
2  Wednesday    15      Rain  
3   Thursday    14    Cloudy  
4     Friday    21     Sunny  
5   Saturday    22     Sunny  
6     Sunday    24     Sunny
```
   
  
Because Pandas prepares data in certain way, we can call any column just by it's name, like:  
  

```python
data['temp']  
------------------------------  
  
0    12  
1    14  
2    15  
3    14  
4    21  
5    22  
6    24  
Name: temp, dtype: int64
```

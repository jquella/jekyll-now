
# Project 1

## Step 1: Load the data and perform basic operations.

##### 1. Load the data in using pandas.


```python
import numpy as np
import pandas as pd
```


```python
sat = pd.read_csv('../data/sat.csv', index_col=0)
```


```python
sat.head()
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
      <th>State</th>
      <th>Participation</th>
      <th>Evidence-Based Reading and Writing</th>
      <th>Math</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alabama</td>
      <td>5%</td>
      <td>593</td>
      <td>572</td>
      <td>1165</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alaska</td>
      <td>38%</td>
      <td>547</td>
      <td>533</td>
      <td>1080</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Arizona</td>
      <td>30%</td>
      <td>563</td>
      <td>553</td>
      <td>1116</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arkansas</td>
      <td>3%</td>
      <td>614</td>
      <td>594</td>
      <td>1208</td>
    </tr>
    <tr>
      <th>4</th>
      <td>California</td>
      <td>53%</td>
      <td>531</td>
      <td>524</td>
      <td>1055</td>
    </tr>
  </tbody>
</table>
</div>




```python
act = pd.read_csv('../data/act.csv', index_col=0)
```


```python
act.head()
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
      <th>State</th>
      <th>Participation</th>
      <th>English</th>
      <th>Math</th>
      <th>Reading</th>
      <th>Science</th>
      <th>Composite</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>60%</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>100%</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>65%</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>62%</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>100%</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
    </tr>
  </tbody>
</table>
</div>



##### 2. Print the first ten rows of each dataframe.


```python
sat.head(10)
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
      <th>State</th>
      <th>Participation</th>
      <th>Evidence-Based Reading and Writing</th>
      <th>Math</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alabama</td>
      <td>5%</td>
      <td>593</td>
      <td>572</td>
      <td>1165</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alaska</td>
      <td>38%</td>
      <td>547</td>
      <td>533</td>
      <td>1080</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Arizona</td>
      <td>30%</td>
      <td>563</td>
      <td>553</td>
      <td>1116</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arkansas</td>
      <td>3%</td>
      <td>614</td>
      <td>594</td>
      <td>1208</td>
    </tr>
    <tr>
      <th>4</th>
      <td>California</td>
      <td>53%</td>
      <td>531</td>
      <td>524</td>
      <td>1055</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Colorado</td>
      <td>11%</td>
      <td>606</td>
      <td>595</td>
      <td>1201</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Connecticut</td>
      <td>100%</td>
      <td>530</td>
      <td>512</td>
      <td>1041</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Delaware</td>
      <td>100%</td>
      <td>503</td>
      <td>492</td>
      <td>996</td>
    </tr>
    <tr>
      <th>8</th>
      <td>District of Columbia</td>
      <td>100%</td>
      <td>482</td>
      <td>468</td>
      <td>950</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Florida</td>
      <td>83%</td>
      <td>520</td>
      <td>497</td>
      <td>1017</td>
    </tr>
  </tbody>
</table>
</div>




```python
act.head(10)
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
      <th>State</th>
      <th>Participation</th>
      <th>English</th>
      <th>Math</th>
      <th>Reading</th>
      <th>Science</th>
      <th>Composite</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>60%</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>100%</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>65%</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>62%</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>100%</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>California</td>
      <td>31%</td>
      <td>22.5</td>
      <td>22.7</td>
      <td>23.1</td>
      <td>22.2</td>
      <td>22.8</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Colorado</td>
      <td>100%</td>
      <td>20.1</td>
      <td>20.3</td>
      <td>21.2</td>
      <td>20.9</td>
      <td>20.8</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Connecticut</td>
      <td>31%</td>
      <td>25.5</td>
      <td>24.6</td>
      <td>25.6</td>
      <td>24.6</td>
      <td>25.2</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Delaware</td>
      <td>18%</td>
      <td>24.1</td>
      <td>23.4</td>
      <td>24.8</td>
      <td>23.6</td>
      <td>24.1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>District of Columbia</td>
      <td>32%</td>
      <td>24.4</td>
      <td>23.5</td>
      <td>24.9</td>
      <td>23.5</td>
      <td>24.2</td>
    </tr>
  </tbody>
</table>
</div>



##### 3. Describe in words what each variable (column) is.

### SAT
1. No column header. Looks to be the index.
2. **State**: What state the row of data is for.
3. **Participation:** Percent of HS seniors in that state took the test.
4. **Evidenced-Based Reading and Writing:** Avg. (mean) score for that section of the test.
5. **Math:** Avg. (mean) score for that section of the test.
6. **Total:** Sum of two section scores

### ACT
1. No column header. Looks to be the index.
2. **State**: What state the row of data is for.
3. **Participation:** Percent of HS seniors in that state took the test.
4. **English:** Avg. (mean) score for that section of the test.
5. **Math:** Avg. (mean) score for that section of the test.
6. **Reading:** Avg. (mean) score for that section of the test.
7. **Science:** Avg. (mean) score for that section of the test.
8. **Composite:** Avg. (mean) score for all sections.

##### 4. Does the data look complete? Are there any obvious issues with the observations?

##### 5. Print the types of each column.


```python
sat.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 51 entries, 0 to 50
    Data columns (total 5 columns):
    State                                 51 non-null object
    Participation                         51 non-null object
    Evidence-Based Reading and Writing    51 non-null int64
    Math                                  51 non-null int64
    Total                                 51 non-null int64
    dtypes: int64(3), object(2)
    memory usage: 2.4+ KB
    


```python
act.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 52 entries, 0 to 51
    Data columns (total 7 columns):
    State            52 non-null object
    Participation    52 non-null object
    English          52 non-null float64
    Math             52 non-null float64
    Reading          52 non-null float64
    Science          52 non-null float64
    Composite        52 non-null float64
    dtypes: float64(5), object(2)
    memory usage: 3.2+ KB
    

##### 6. Do any types need to be reassigned? If so, go ahead and do it.

- Participation data type for both sets is 'object' - will go ahead and change them to float.


```python
# checking how to change object % to proper float value
a = sat['Participation'][0]
float(a.strip('%'))/100
```




    0.05




```python
sat['Participation'] = [float(i.strip('%'))/100 for i in sat['Participation']]
```


```python
sat.head()
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
      <th>State</th>
      <th>Participation</th>
      <th>Evidence-Based Reading and Writing</th>
      <th>Math</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alabama</td>
      <td>0.05</td>
      <td>593</td>
      <td>572</td>
      <td>1165</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alaska</td>
      <td>0.38</td>
      <td>547</td>
      <td>533</td>
      <td>1080</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Arizona</td>
      <td>0.30</td>
      <td>563</td>
      <td>553</td>
      <td>1116</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arkansas</td>
      <td>0.03</td>
      <td>614</td>
      <td>594</td>
      <td>1208</td>
    </tr>
    <tr>
      <th>4</th>
      <td>California</td>
      <td>0.53</td>
      <td>531</td>
      <td>524</td>
      <td>1055</td>
    </tr>
  </tbody>
</table>
</div>




```python
act['Participation'] = [float(i.strip('%'))/100 for i in act['Participation']]
```


```python
act.head()
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
      <th>State</th>
      <th>Participation</th>
      <th>English</th>
      <th>Math</th>
      <th>Reading</th>
      <th>Science</th>
      <th>Composite</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>0.60</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
    </tr>
  </tbody>
</table>
</div>



##### 7. Create a dictionary for each column mapping the State to its respective value for that column. (For example, you should have three SAT dictionaries.)


```python
# # [i for i in sat.columns[2:]]

# # messing around and trying to automate everything. unfortunately can't do that with new dict names
# for i in sat.columns[2:]:
#     for j in range(len(sat)):
#         pass
```


```python
# #longer way
# sat_math = {}
# for i in range(len(sat)):
#     d.update({sat['State'][i]:act['Composite'][i]})
```


```python
# Creating ACT dictionaries, the better comprehension way

act_dict_english = {act['State'][i]:act['English'][i] for i in range(len(act))}
act_dict_math = {act['State'][i]:act['Math'][i] for i in range(len(act))}
act_dict_reading = {act['State'][i]:act['Reading'][i] for i in range(len(act))}
act_dict_science = {act['State'][i]:act['Science'][i] for i in range(len(act))}
act_dict_composite = {act['State'][i]:act['Composite'][i] for i in range(len(act))}
```


```python
# Creating SAT dictionaries, the better comprehension way

sat_dict_ev_read_write = {sat['State'][i]:sat['Evidence-Based Reading and Writing'][i] for i in range(len(sat))}
sat_dict_math = {sat['State'][i]:sat['Math'][i] for i in range(len(sat))}
sat_dict_total = {sat['State'][i]:sat['Total'][i] for i in range(len(sat))}
```

##### 8. Create one dictionary where each key is the column name, and each value is an iterable (a list or a Pandas Series) of all the values in that column.


```python
col_dict = {i:sat[i].values for i in sat.columns}
```


```python
col_dict
```




    {'State': array(['Alabama', 'Alaska', 'Arizona', 'Arkansas', 'California',
            'Colorado', 'Connecticut', 'Delaware', 'District of Columbia',
            'Florida', 'Georgia', 'Hawaii', 'Idaho', 'Illinois', 'Indiana',
            'Iowa', 'Kansas', 'Kentucky', 'Louisiana', 'Maine', 'Maryland',
            'Massachusetts', 'Michigan', 'Minnesota', 'Mississippi',
            'Missouri', 'Montana', 'Nebraska', 'Nevada', 'New Hampshire',
            'New Jersey', 'New Mexico', 'New York', 'North Carolina',
            'North Dakota', 'Ohio', 'Oklahoma', 'Oregon', 'Pennsylvania',
            'Rhode Island', 'South Carolina', 'South Dakota', 'Tennessee',
            'Texas', 'Utah', 'Vermont', 'Virginia', 'Washington',
            'West Virginia', 'Wisconsin', 'Wyoming'], dtype=object),
     'Participation': array([0.05, 0.38, 0.3 , 0.03, 0.53, 0.11, 1.  , 1.  , 1.  , 0.83, 0.61,
            0.55, 0.93, 0.09, 0.63, 0.02, 0.04, 0.04, 0.04, 0.95, 0.69, 0.76,
            1.  , 0.03, 0.02, 0.03, 0.1 , 0.03, 0.26, 0.96, 0.7 , 0.11, 0.67,
            0.49, 0.02, 0.12, 0.07, 0.43, 0.65, 0.71, 0.5 , 0.03, 0.05, 0.62,
            0.03, 0.6 , 0.65, 0.64, 0.14, 0.03, 0.03]),
     'Evidence-Based Reading and Writing': array([593, 547, 563, 614, 531, 606, 530, 503, 482, 520, 535, 544, 513,
            559, 542, 641, 632, 631, 611, 513, 536, 555, 509, 644, 634, 640,
            605, 629, 563, 532, 530, 577, 528, 546, 635, 578, 530, 560, 540,
            539, 543, 612, 623, 513, 624, 562, 561, 541, 558, 642, 626],
           dtype=int64),
     'Math': array([572, 533, 553, 594, 524, 595, 512, 492, 468, 497, 515, 541, 493,
            556, 532, 635, 628, 616, 586, 499,  52, 551, 495, 651, 607, 631,
            591, 625, 553, 520, 526, 561, 523, 535, 621, 570, 517, 548, 531,
            524, 521, 603, 604, 507, 614, 551, 541, 534, 528, 649, 604],
           dtype=int64),
     'Total': array([1165, 1080, 1116, 1208, 1055, 1201, 1041,  996,  950, 1017, 1050,
            1085, 1005, 1115, 1074, 1275, 1260, 1247, 1198, 1012, 1060, 1107,
            1005, 1295, 1242, 1271, 1196, 1253, 1116, 1052, 1056, 1138, 1052,
            1081, 1256, 1149, 1047, 1108, 1071, 1062, 1064, 1216, 1228, 1020,
            1238, 1114, 1102, 1075, 1086, 1291, 1230], dtype=int64)}



##### 9. Merge the dataframes on the state column.


```python
# both = pd.merge(sat, act, how='left',suffixes=('_sat','_act')) -- this did NOT work
# both = pd.concat([sat, act], axis=1, join_axes=[act.index], suffixes=('_sat','_act'))
```


```python
both = pd.merge(act, sat, how='left', on='State', suffixes=('_act','_sat')) 
```


```python
both['State'].unique()
```




    array(['National', 'Alabama', 'Alaska', 'Arizona', 'Arkansas',
           'California', 'Colorado', 'Connecticut', 'Delaware',
           'District of Columbia', 'Florida', 'Georgia', 'Hawaii', 'Idaho',
           'Illinois', 'Indiana', 'Iowa', 'Kansas', 'Kentucky', 'Louisiana',
           'Maine', 'Maryland', 'Massachusetts', 'Michigan', 'Minnesota',
           'Mississippi', 'Missouri', 'Montana', 'Nebraska', 'Nevada',
           'New Hampshire', 'New Jersey', 'New Mexico', 'New York',
           'North Carolina', 'North Dakota', 'Ohio', 'Oklahoma', 'Oregon',
           'Pennsylvania', 'Rhode Island', 'South Carolina', 'South Dakota',
           'Tennessee', 'Texas', 'Utah', 'Vermont', 'Virginia', 'Washington',
           'West Virginia', 'Wisconsin', 'Wyoming'], dtype=object)




```python
both.head()
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
      <th>State</th>
      <th>Participation_act</th>
      <th>English</th>
      <th>Math_act</th>
      <th>Reading</th>
      <th>Science</th>
      <th>Composite</th>
      <th>Participation_sat</th>
      <th>Evidence-Based Reading and Writing</th>
      <th>Math_sat</th>
      <th>Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>0.60</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>0.30</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>0.03</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
  </tbody>
</table>
</div>



##### 10. Change the names of the columns so you can distinguish between the SAT columns and the ACT columns.


```python
#first, gonna make everything lower case
lower_names = []
for i in both.columns:
    lower_names.append(i.lower())
```


```python
both.columns = lower_names
```


```python
###### SCRAP THIS VERSION ######

# #then, gonna change the ones we didn't already add a suffix to
# act_cols = ['english', 'reading', 'science', 'composite']
# sat_cols = ['evidence-based reading and writing', 'total']

# act_new_cols = [i+'_act' for i in act_cols]
# sat_new_cols = [i+'_sat' for i in sat_cols]
```


```python
new_cols = ['state', 'participation_act', 'english_act', 'math_act','reading_act', 'science_act','composite_act',
            'participation_sat','evidence-based reading and writing_sat', 'math_sat','total_sat']
```


```python
both.columns = new_cols
```


```python
both.head()
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>0.60</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>0.30</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>0.03</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
both['english_act'].max()
```




    25.5



##### 11. Print the minimum and maximum of each numeric column in the data frame.


```python
# ###### OLD, SLOW WAY #####
# numeric_cols = ['english_act', 'math_sat', 'reading_act', 'science_act', 'composite_act', 
#                 'evidence-based reading and writing_sat', 'math_act', 'total_sat']

# for i in both.columns:
#     if i in numeric_cols:
#         print('Min and Max of {}: ({}, {})'.format(i, both[i].min(),both[i].max()))
```


```python
# #### OLD WAY, WITHOUT PARTICIPATION ####
# numeric_cols = ['english_act', 'math_act', 'reading_act', 'science_act', 'composite_act', 
#                 'evidence-based reading and writing_sat', 'math_sat', 'total_sat']
```


```python
# #### NEW WAY, incl. PARTICIPATION ####
numeric_cols = list(both.columns)[1:]
```


```python
minmax = [(both[i].min(), both[i].max()) for i in both.columns if i in numeric_cols]

for i in range(len(numeric_cols)):
    print('Min and Max of {}: {}'.format(numeric_cols[i], minmax[i]))
```

    Min and Max of participation_act: (0.08, 1.0)
    Min and Max of english_act: (16.3, 25.5)
    Min and Max of math_act: (18.0, 25.3)
    Min and Max of reading_act: (18.1, 26.0)
    Min and Max of science_act: (2.3, 24.9)
    Min and Max of composite_act: (17.8, 25.5)
    Min and Max of participation_sat: (0.02, 1.0)
    Min and Max of evidence-based reading and writing_sat: (482.0, 644.0)
    Min and Max of math_sat: (52.0, 651.0)
    Min and Max of total_sat: (950.0, 1295.0)
    

##### 12. Write a function using only list comprehensions, no loops, to compute standard deviation. Using this function, calculate the standard deviation of each numeric column in both data sets. Add these to a list called `sd`.

$$\sigma = \sqrt{\frac{1}{n}\sum_{i=1}^n(x_i - \mu)^2}$$


```python
def std_dev(sample):
    """Computes standard deviation using list comprehensions."""
    
    std = np.sqrt(np.sum([((i - np.nanmean(sample))**2) for i in sample]) / len(sample))
    
    return std
```


```python
# check that it works!

print(std_dev(both[numeric_cols[0]]))
print(np.std(both[numeric_cols[0]]))
```

    0.3152495020150073
    0.3152495020150073
    


```python
numeric_cols
```




    ['participation_act',
     'english_act',
     'math_act',
     'reading_act',
     'science_act',
     'composite_act',
     'participation_sat',
     'evidence-based reading and writing_sat',
     'math_sat',
     'total_sat']




```python
std_dev(both['evidence-based reading and writing_sat'])
```




    nan




```python
np.nanmean(both['math_sat'])
```




    547.6274509803922




```python
both.head()
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>National</td>
      <td>0.60</td>
      <td>20.3</td>
      <td>20.7</td>
      <td>21.4</td>
      <td>21.0</td>
      <td>21.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>0.30</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>0.03</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
both.loc[:,['evidence-based reading and writing_sat', 'math_sat', 'total_sat']].head()
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
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# dropping NaN national row 
both.dropna(inplace=True)
both.head()
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>0.30</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>0.03</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>California</td>
      <td>0.31</td>
      <td>22.5</td>
      <td>22.7</td>
      <td>23.1</td>
      <td>22.2</td>
      <td>22.8</td>
      <td>0.53</td>
      <td>531.0</td>
      <td>524.0</td>
      <td>1055.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
sd = [std_dev(both[i]) for i in numeric_cols]
```


```python
print(sd,'\n', 'len is',len(sd))
```

    [0.31824175751231804, 2.3304876369363368, 1.9624620273436781, 2.046902931484265, 3.151107895464408, 2.0007860815819893, 0.3492907076664507, 45.21697020437866, 84.07255521608297, 91.58351056778743] 
     len is 10
    

## Step 2: Manipulate the dataframe

##### 13. Turn the list `sd` into a new observation in your dataset.


```python
# add a row label that would match up with 'state' to make the sd list the same length as the # of cols in dataframe
sd.insert(0, 'std_dev')
sd
```




    ['std_dev',
     0.31824175751231804,
     2.3304876369363368,
     1.9624620273436781,
     2.046902931484265,
     3.151107895464408,
     2.0007860815819893,
     0.3492907076664507,
     45.21697020437866,
     84.07255521608297,
     91.58351056778743]




```python
both.index[-1]
```




    51




```python
# put it on the end row
both.loc[52] = sd
```


```python
both.tail()
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>48</th>
      <td>Washington</td>
      <td>0.290000</td>
      <td>20.900000</td>
      <td>21.900000</td>
      <td>22.100000</td>
      <td>22.000000</td>
      <td>21.900000</td>
      <td>0.640000</td>
      <td>541.00000</td>
      <td>534.000000</td>
      <td>1075.000000</td>
    </tr>
    <tr>
      <th>49</th>
      <td>West Virginia</td>
      <td>0.690000</td>
      <td>20.000000</td>
      <td>19.400000</td>
      <td>21.200000</td>
      <td>20.500000</td>
      <td>20.400000</td>
      <td>0.140000</td>
      <td>558.00000</td>
      <td>528.000000</td>
      <td>1086.000000</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Wisconsin</td>
      <td>1.000000</td>
      <td>19.700000</td>
      <td>20.400000</td>
      <td>20.600000</td>
      <td>20.900000</td>
      <td>20.500000</td>
      <td>0.030000</td>
      <td>642.00000</td>
      <td>649.000000</td>
      <td>1291.000000</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Wyoming</td>
      <td>1.000000</td>
      <td>19.400000</td>
      <td>19.800000</td>
      <td>20.800000</td>
      <td>20.600000</td>
      <td>20.200000</td>
      <td>0.030000</td>
      <td>626.00000</td>
      <td>604.000000</td>
      <td>1230.000000</td>
    </tr>
    <tr>
      <th>52</th>
      <td>std_dev</td>
      <td>0.318242</td>
      <td>2.330488</td>
      <td>1.962462</td>
      <td>2.046903</td>
      <td>3.151108</td>
      <td>2.000786</td>
      <td>0.349291</td>
      <td>45.21697</td>
      <td>84.072555</td>
      <td>91.583511</td>
    </tr>
  </tbody>
</table>
</div>



##### 14. Sort the dataframe by the values in a numeric column (e.g. observations descending by SAT participation rate)


```python
both.sort_values(by='total_sat', ascending=False)
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>24</th>
      <td>Minnesota</td>
      <td>1.000000</td>
      <td>20.400000</td>
      <td>21.500000</td>
      <td>21.800000</td>
      <td>21.600000</td>
      <td>21.500000</td>
      <td>0.030000</td>
      <td>644.00000</td>
      <td>651.000000</td>
      <td>1295.000000</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Wisconsin</td>
      <td>1.000000</td>
      <td>19.700000</td>
      <td>20.400000</td>
      <td>20.600000</td>
      <td>20.900000</td>
      <td>20.500000</td>
      <td>0.030000</td>
      <td>642.00000</td>
      <td>649.000000</td>
      <td>1291.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Iowa</td>
      <td>0.670000</td>
      <td>21.200000</td>
      <td>21.300000</td>
      <td>22.600000</td>
      <td>22.100000</td>
      <td>21.900000</td>
      <td>0.020000</td>
      <td>641.00000</td>
      <td>635.000000</td>
      <td>1275.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Missouri</td>
      <td>1.000000</td>
      <td>19.800000</td>
      <td>19.900000</td>
      <td>20.800000</td>
      <td>20.500000</td>
      <td>20.400000</td>
      <td>0.030000</td>
      <td>640.00000</td>
      <td>631.000000</td>
      <td>1271.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Kansas</td>
      <td>0.730000</td>
      <td>21.100000</td>
      <td>21.300000</td>
      <td>22.300000</td>
      <td>21.700000</td>
      <td>21.700000</td>
      <td>0.040000</td>
      <td>632.00000</td>
      <td>628.000000</td>
      <td>1260.000000</td>
    </tr>
    <tr>
      <th>35</th>
      <td>North Dakota</td>
      <td>0.980000</td>
      <td>19.000000</td>
      <td>20.400000</td>
      <td>20.500000</td>
      <td>20.600000</td>
      <td>20.300000</td>
      <td>0.020000</td>
      <td>635.00000</td>
      <td>621.000000</td>
      <td>1256.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Nebraska</td>
      <td>0.840000</td>
      <td>20.900000</td>
      <td>20.900000</td>
      <td>21.900000</td>
      <td>21.500000</td>
      <td>21.400000</td>
      <td>0.030000</td>
      <td>629.00000</td>
      <td>625.000000</td>
      <td>1253.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Kentucky</td>
      <td>1.000000</td>
      <td>19.600000</td>
      <td>19.400000</td>
      <td>20.500000</td>
      <td>20.100000</td>
      <td>20.000000</td>
      <td>0.040000</td>
      <td>631.00000</td>
      <td>616.000000</td>
      <td>1247.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Mississippi</td>
      <td>1.000000</td>
      <td>18.200000</td>
      <td>18.100000</td>
      <td>18.800000</td>
      <td>18.800000</td>
      <td>18.600000</td>
      <td>0.020000</td>
      <td>634.00000</td>
      <td>607.000000</td>
      <td>1242.000000</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Utah</td>
      <td>1.000000</td>
      <td>19.500000</td>
      <td>19.900000</td>
      <td>20.800000</td>
      <td>20.600000</td>
      <td>20.300000</td>
      <td>0.030000</td>
      <td>624.00000</td>
      <td>614.000000</td>
      <td>1238.000000</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Wyoming</td>
      <td>1.000000</td>
      <td>19.400000</td>
      <td>19.800000</td>
      <td>20.800000</td>
      <td>20.600000</td>
      <td>20.200000</td>
      <td>0.030000</td>
      <td>626.00000</td>
      <td>604.000000</td>
      <td>1230.000000</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Tennessee</td>
      <td>1.000000</td>
      <td>19.500000</td>
      <td>19.200000</td>
      <td>20.100000</td>
      <td>19.900000</td>
      <td>19.800000</td>
      <td>0.050000</td>
      <td>623.00000</td>
      <td>604.000000</td>
      <td>1228.000000</td>
    </tr>
    <tr>
      <th>42</th>
      <td>South Dakota</td>
      <td>0.800000</td>
      <td>20.700000</td>
      <td>21.500000</td>
      <td>22.300000</td>
      <td>22.000000</td>
      <td>21.800000</td>
      <td>0.030000</td>
      <td>612.00000</td>
      <td>603.000000</td>
      <td>1216.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.000000</td>
      <td>18.900000</td>
      <td>19.000000</td>
      <td>19.700000</td>
      <td>19.500000</td>
      <td>19.400000</td>
      <td>0.030000</td>
      <td>614.00000</td>
      <td>594.000000</td>
      <td>1208.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Colorado</td>
      <td>1.000000</td>
      <td>20.100000</td>
      <td>20.300000</td>
      <td>21.200000</td>
      <td>20.900000</td>
      <td>20.800000</td>
      <td>0.110000</td>
      <td>606.00000</td>
      <td>595.000000</td>
      <td>1201.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Louisiana</td>
      <td>1.000000</td>
      <td>19.400000</td>
      <td>18.800000</td>
      <td>19.800000</td>
      <td>19.600000</td>
      <td>19.500000</td>
      <td>0.040000</td>
      <td>611.00000</td>
      <td>586.000000</td>
      <td>1198.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Montana</td>
      <td>1.000000</td>
      <td>19.000000</td>
      <td>20.200000</td>
      <td>21.000000</td>
      <td>20.500000</td>
      <td>20.300000</td>
      <td>0.100000</td>
      <td>605.00000</td>
      <td>591.000000</td>
      <td>1196.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.000000</td>
      <td>18.900000</td>
      <td>18.400000</td>
      <td>19.700000</td>
      <td>19.400000</td>
      <td>19.200000</td>
      <td>0.050000</td>
      <td>593.00000</td>
      <td>572.000000</td>
      <td>1165.000000</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Ohio</td>
      <td>0.750000</td>
      <td>21.200000</td>
      <td>21.600000</td>
      <td>22.500000</td>
      <td>22.000000</td>
      <td>22.000000</td>
      <td>0.120000</td>
      <td>578.00000</td>
      <td>570.000000</td>
      <td>1149.000000</td>
    </tr>
    <tr>
      <th>32</th>
      <td>New Mexico</td>
      <td>0.660000</td>
      <td>18.600000</td>
      <td>19.400000</td>
      <td>20.400000</td>
      <td>20.000000</td>
      <td>19.700000</td>
      <td>0.110000</td>
      <td>577.00000</td>
      <td>561.000000</td>
      <td>1138.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.620000</td>
      <td>18.600000</td>
      <td>19.800000</td>
      <td>20.100000</td>
      <td>19.800000</td>
      <td>19.700000</td>
      <td>0.300000</td>
      <td>563.00000</td>
      <td>553.000000</td>
      <td>1116.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Nevada</td>
      <td>1.000000</td>
      <td>16.300000</td>
      <td>18.000000</td>
      <td>18.100000</td>
      <td>18.200000</td>
      <td>17.800000</td>
      <td>0.260000</td>
      <td>563.00000</td>
      <td>553.000000</td>
      <td>1116.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Illinois</td>
      <td>0.930000</td>
      <td>21.000000</td>
      <td>21.200000</td>
      <td>21.600000</td>
      <td>21.300000</td>
      <td>21.400000</td>
      <td>0.090000</td>
      <td>559.00000</td>
      <td>556.000000</td>
      <td>1115.000000</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Vermont</td>
      <td>0.290000</td>
      <td>23.300000</td>
      <td>23.100000</td>
      <td>24.400000</td>
      <td>23.200000</td>
      <td>23.600000</td>
      <td>0.600000</td>
      <td>562.00000</td>
      <td>551.000000</td>
      <td>1114.000000</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Oregon</td>
      <td>0.400000</td>
      <td>21.200000</td>
      <td>21.500000</td>
      <td>22.400000</td>
      <td>21.700000</td>
      <td>21.800000</td>
      <td>0.430000</td>
      <td>560.00000</td>
      <td>548.000000</td>
      <td>1108.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Massachusetts</td>
      <td>0.290000</td>
      <td>25.400000</td>
      <td>25.300000</td>
      <td>25.900000</td>
      <td>24.700000</td>
      <td>25.400000</td>
      <td>0.760000</td>
      <td>555.00000</td>
      <td>551.000000</td>
      <td>1107.000000</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Virginia</td>
      <td>0.290000</td>
      <td>23.500000</td>
      <td>23.300000</td>
      <td>24.600000</td>
      <td>23.500000</td>
      <td>23.800000</td>
      <td>0.650000</td>
      <td>561.00000</td>
      <td>541.000000</td>
      <td>1102.000000</td>
    </tr>
    <tr>
      <th>49</th>
      <td>West Virginia</td>
      <td>0.690000</td>
      <td>20.000000</td>
      <td>19.400000</td>
      <td>21.200000</td>
      <td>20.500000</td>
      <td>20.400000</td>
      <td>0.140000</td>
      <td>558.00000</td>
      <td>528.000000</td>
      <td>1086.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Hawaii</td>
      <td>0.900000</td>
      <td>17.800000</td>
      <td>19.200000</td>
      <td>19.200000</td>
      <td>19.300000</td>
      <td>19.000000</td>
      <td>0.550000</td>
      <td>544.00000</td>
      <td>541.000000</td>
      <td>1085.000000</td>
    </tr>
    <tr>
      <th>34</th>
      <td>North Carolina</td>
      <td>1.000000</td>
      <td>17.800000</td>
      <td>19.300000</td>
      <td>19.600000</td>
      <td>19.300000</td>
      <td>19.100000</td>
      <td>0.490000</td>
      <td>546.00000</td>
      <td>535.000000</td>
      <td>1081.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.650000</td>
      <td>18.700000</td>
      <td>19.800000</td>
      <td>20.400000</td>
      <td>19.900000</td>
      <td>19.800000</td>
      <td>0.380000</td>
      <td>547.00000</td>
      <td>533.000000</td>
      <td>1080.000000</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Washington</td>
      <td>0.290000</td>
      <td>20.900000</td>
      <td>21.900000</td>
      <td>22.100000</td>
      <td>22.000000</td>
      <td>21.900000</td>
      <td>0.640000</td>
      <td>541.00000</td>
      <td>534.000000</td>
      <td>1075.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Indiana</td>
      <td>0.350000</td>
      <td>22.000000</td>
      <td>22.400000</td>
      <td>23.200000</td>
      <td>22.300000</td>
      <td>22.600000</td>
      <td>0.630000</td>
      <td>542.00000</td>
      <td>532.000000</td>
      <td>1074.000000</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Pennsylvania</td>
      <td>0.230000</td>
      <td>23.400000</td>
      <td>23.400000</td>
      <td>24.200000</td>
      <td>23.300000</td>
      <td>23.700000</td>
      <td>0.650000</td>
      <td>540.00000</td>
      <td>531.000000</td>
      <td>1071.000000</td>
    </tr>
    <tr>
      <th>41</th>
      <td>South Carolina</td>
      <td>1.000000</td>
      <td>17.500000</td>
      <td>18.600000</td>
      <td>19.100000</td>
      <td>18.900000</td>
      <td>18.700000</td>
      <td>0.500000</td>
      <td>543.00000</td>
      <td>521.000000</td>
      <td>1064.000000</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Rhode Island</td>
      <td>0.210000</td>
      <td>24.000000</td>
      <td>23.300000</td>
      <td>24.700000</td>
      <td>23.400000</td>
      <td>24.000000</td>
      <td>0.710000</td>
      <td>539.00000</td>
      <td>524.000000</td>
      <td>1062.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Maryland</td>
      <td>0.280000</td>
      <td>23.300000</td>
      <td>23.100000</td>
      <td>24.200000</td>
      <td>2.300000</td>
      <td>23.600000</td>
      <td>0.690000</td>
      <td>536.00000</td>
      <td>52.000000</td>
      <td>1060.000000</td>
    </tr>
    <tr>
      <th>31</th>
      <td>New Jersey</td>
      <td>0.340000</td>
      <td>23.800000</td>
      <td>23.800000</td>
      <td>24.100000</td>
      <td>23.200000</td>
      <td>23.900000</td>
      <td>0.700000</td>
      <td>530.00000</td>
      <td>526.000000</td>
      <td>1056.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>California</td>
      <td>0.310000</td>
      <td>22.500000</td>
      <td>22.700000</td>
      <td>23.100000</td>
      <td>22.200000</td>
      <td>22.800000</td>
      <td>0.530000</td>
      <td>531.00000</td>
      <td>524.000000</td>
      <td>1055.000000</td>
    </tr>
    <tr>
      <th>33</th>
      <td>New York</td>
      <td>0.310000</td>
      <td>23.800000</td>
      <td>24.000000</td>
      <td>24.600000</td>
      <td>23.900000</td>
      <td>24.200000</td>
      <td>0.670000</td>
      <td>528.00000</td>
      <td>523.000000</td>
      <td>1052.000000</td>
    </tr>
    <tr>
      <th>30</th>
      <td>New Hampshire</td>
      <td>0.180000</td>
      <td>25.400000</td>
      <td>25.100000</td>
      <td>26.000000</td>
      <td>24.900000</td>
      <td>25.500000</td>
      <td>0.960000</td>
      <td>532.00000</td>
      <td>520.000000</td>
      <td>1052.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Georgia</td>
      <td>0.550000</td>
      <td>21.000000</td>
      <td>20.900000</td>
      <td>22.000000</td>
      <td>21.300000</td>
      <td>21.400000</td>
      <td>0.610000</td>
      <td>535.00000</td>
      <td>515.000000</td>
      <td>1050.000000</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Oklahoma</td>
      <td>1.000000</td>
      <td>18.500000</td>
      <td>18.800000</td>
      <td>20.100000</td>
      <td>19.600000</td>
      <td>19.400000</td>
      <td>0.070000</td>
      <td>530.00000</td>
      <td>517.000000</td>
      <td>1047.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Connecticut</td>
      <td>0.310000</td>
      <td>25.500000</td>
      <td>24.600000</td>
      <td>25.600000</td>
      <td>24.600000</td>
      <td>25.200000</td>
      <td>1.000000</td>
      <td>530.00000</td>
      <td>512.000000</td>
      <td>1041.000000</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Texas</td>
      <td>0.450000</td>
      <td>19.500000</td>
      <td>20.700000</td>
      <td>21.100000</td>
      <td>20.900000</td>
      <td>20.700000</td>
      <td>0.620000</td>
      <td>513.00000</td>
      <td>507.000000</td>
      <td>1020.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Florida</td>
      <td>0.730000</td>
      <td>19.000000</td>
      <td>19.400000</td>
      <td>21.000000</td>
      <td>19.400000</td>
      <td>19.800000</td>
      <td>0.830000</td>
      <td>520.00000</td>
      <td>497.000000</td>
      <td>1017.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Maine</td>
      <td>0.080000</td>
      <td>24.200000</td>
      <td>24.000000</td>
      <td>24.800000</td>
      <td>23.700000</td>
      <td>24.300000</td>
      <td>0.950000</td>
      <td>513.00000</td>
      <td>499.000000</td>
      <td>1012.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Idaho</td>
      <td>0.380000</td>
      <td>21.900000</td>
      <td>21.800000</td>
      <td>23.000000</td>
      <td>22.100000</td>
      <td>22.300000</td>
      <td>0.930000</td>
      <td>513.00000</td>
      <td>493.000000</td>
      <td>1005.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Michigan</td>
      <td>0.290000</td>
      <td>24.100000</td>
      <td>23.700000</td>
      <td>24.500000</td>
      <td>23.800000</td>
      <td>24.100000</td>
      <td>1.000000</td>
      <td>509.00000</td>
      <td>495.000000</td>
      <td>1005.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Delaware</td>
      <td>0.180000</td>
      <td>24.100000</td>
      <td>23.400000</td>
      <td>24.800000</td>
      <td>23.600000</td>
      <td>24.100000</td>
      <td>1.000000</td>
      <td>503.00000</td>
      <td>492.000000</td>
      <td>996.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>District of Columbia</td>
      <td>0.320000</td>
      <td>24.400000</td>
      <td>23.500000</td>
      <td>24.900000</td>
      <td>23.500000</td>
      <td>24.200000</td>
      <td>1.000000</td>
      <td>482.00000</td>
      <td>468.000000</td>
      <td>950.000000</td>
    </tr>
    <tr>
      <th>52</th>
      <td>std_dev</td>
      <td>0.318242</td>
      <td>2.330488</td>
      <td>1.962462</td>
      <td>2.046903</td>
      <td>3.151108</td>
      <td>2.000786</td>
      <td>0.349291</td>
      <td>45.21697</td>
      <td>84.072555</td>
      <td>91.583511</td>
    </tr>
  </tbody>
</table>
</div>



##### 15. Use a boolean filter to display only observations with a score above a certain threshold (e.g. only states with a participation rate above 50%)


```python
both[both['math_sat'] >= 600]
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>16</th>
      <td>Iowa</td>
      <td>0.67</td>
      <td>21.2</td>
      <td>21.3</td>
      <td>22.6</td>
      <td>22.1</td>
      <td>21.9</td>
      <td>0.02</td>
      <td>641.0</td>
      <td>635.0</td>
      <td>1275.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Kansas</td>
      <td>0.73</td>
      <td>21.1</td>
      <td>21.3</td>
      <td>22.3</td>
      <td>21.7</td>
      <td>21.7</td>
      <td>0.04</td>
      <td>632.0</td>
      <td>628.0</td>
      <td>1260.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Kentucky</td>
      <td>1.00</td>
      <td>19.6</td>
      <td>19.4</td>
      <td>20.5</td>
      <td>20.1</td>
      <td>20.0</td>
      <td>0.04</td>
      <td>631.0</td>
      <td>616.0</td>
      <td>1247.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Minnesota</td>
      <td>1.00</td>
      <td>20.4</td>
      <td>21.5</td>
      <td>21.8</td>
      <td>21.6</td>
      <td>21.5</td>
      <td>0.03</td>
      <td>644.0</td>
      <td>651.0</td>
      <td>1295.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Mississippi</td>
      <td>1.00</td>
      <td>18.2</td>
      <td>18.1</td>
      <td>18.8</td>
      <td>18.8</td>
      <td>18.6</td>
      <td>0.02</td>
      <td>634.0</td>
      <td>607.0</td>
      <td>1242.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Missouri</td>
      <td>1.00</td>
      <td>19.8</td>
      <td>19.9</td>
      <td>20.8</td>
      <td>20.5</td>
      <td>20.4</td>
      <td>0.03</td>
      <td>640.0</td>
      <td>631.0</td>
      <td>1271.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Nebraska</td>
      <td>0.84</td>
      <td>20.9</td>
      <td>20.9</td>
      <td>21.9</td>
      <td>21.5</td>
      <td>21.4</td>
      <td>0.03</td>
      <td>629.0</td>
      <td>625.0</td>
      <td>1253.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>North Dakota</td>
      <td>0.98</td>
      <td>19.0</td>
      <td>20.4</td>
      <td>20.5</td>
      <td>20.6</td>
      <td>20.3</td>
      <td>0.02</td>
      <td>635.0</td>
      <td>621.0</td>
      <td>1256.0</td>
    </tr>
    <tr>
      <th>42</th>
      <td>South Dakota</td>
      <td>0.80</td>
      <td>20.7</td>
      <td>21.5</td>
      <td>22.3</td>
      <td>22.0</td>
      <td>21.8</td>
      <td>0.03</td>
      <td>612.0</td>
      <td>603.0</td>
      <td>1216.0</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Tennessee</td>
      <td>1.00</td>
      <td>19.5</td>
      <td>19.2</td>
      <td>20.1</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.05</td>
      <td>623.0</td>
      <td>604.0</td>
      <td>1228.0</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Utah</td>
      <td>1.00</td>
      <td>19.5</td>
      <td>19.9</td>
      <td>20.8</td>
      <td>20.6</td>
      <td>20.3</td>
      <td>0.03</td>
      <td>624.0</td>
      <td>614.0</td>
      <td>1238.0</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Wisconsin</td>
      <td>1.00</td>
      <td>19.7</td>
      <td>20.4</td>
      <td>20.6</td>
      <td>20.9</td>
      <td>20.5</td>
      <td>0.03</td>
      <td>642.0</td>
      <td>649.0</td>
      <td>1291.0</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Wyoming</td>
      <td>1.00</td>
      <td>19.4</td>
      <td>19.8</td>
      <td>20.8</td>
      <td>20.6</td>
      <td>20.2</td>
      <td>0.03</td>
      <td>626.0</td>
      <td>604.0</td>
      <td>1230.0</td>
    </tr>
  </tbody>
</table>
</div>



## Step 3: Visualize the data

##### 16. Using MatPlotLib and PyPlot, plot the distribution of the Rate columns for both SAT and ACT using histograms. (You should have two histograms. You might find [this link](https://matplotlib.org/users/pyplot_tutorial.html#working-with-multiple-figures-and-axes) helpful in organizing one plot above the other.) 


```python
import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline
```


```python
fig, ax = plt.subplots(1,2, figsize=(15,8))

fig.suptitle('Participation Rates for ACT and SAT', fontsize=16)

ax[0].hist(both[both['state'] != 'std_dev'].loc[:,'participation_act']);
ax[0].set(title='ACT Participation');

ax[1].hist(both[both['state'] != 'std_dev'].loc[:,'participation_sat']);
ax[1].set(title='SAT Participation');
```


![png](../images/starter-code_files/starter-code_75_0.png)



```python
# sat
```

##### 17. Plot the Math(s) distributions from both data sets.


```python
fig, ax = plt.subplots(1,2, figsize=(15,8))

fig.suptitle('Math Scores for ACT and SAT', fontsize=16)

ax[0].hist(both[both['state'] != 'std_dev'].loc[:,'math_act']);
ax[0].set(title='ACT Math');

ax[1].hist(both[both['state'] != 'std_dev'].loc[:,'math_sat']);
ax[1].set(title='SAT Math');
```


![png](../images/starter-code_files/starter-code_78_0.png)



```python
tests = both.copy()
```


```python
tests.loc[21, 'math_sat'] = float(tests.loc[21, 'total_sat'] - tests.loc[21, 'evidence-based reading and writing_sat'])
```


```python
tests.loc[18:24]
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>18</th>
      <td>Kentucky</td>
      <td>1.00</td>
      <td>19.6</td>
      <td>19.4</td>
      <td>20.5</td>
      <td>20.1</td>
      <td>20.0</td>
      <td>0.04</td>
      <td>631.0</td>
      <td>616.0</td>
      <td>1247.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Louisiana</td>
      <td>1.00</td>
      <td>19.4</td>
      <td>18.8</td>
      <td>19.8</td>
      <td>19.6</td>
      <td>19.5</td>
      <td>0.04</td>
      <td>611.0</td>
      <td>586.0</td>
      <td>1198.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Maine</td>
      <td>0.08</td>
      <td>24.2</td>
      <td>24.0</td>
      <td>24.8</td>
      <td>23.7</td>
      <td>24.3</td>
      <td>0.95</td>
      <td>513.0</td>
      <td>499.0</td>
      <td>1012.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Maryland</td>
      <td>0.28</td>
      <td>23.3</td>
      <td>23.1</td>
      <td>24.2</td>
      <td>2.3</td>
      <td>23.6</td>
      <td>0.69</td>
      <td>536.0</td>
      <td>524.0</td>
      <td>1060.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Massachusetts</td>
      <td>0.29</td>
      <td>25.4</td>
      <td>25.3</td>
      <td>25.9</td>
      <td>24.7</td>
      <td>25.4</td>
      <td>0.76</td>
      <td>555.0</td>
      <td>551.0</td>
      <td>1107.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Michigan</td>
      <td>0.29</td>
      <td>24.1</td>
      <td>23.7</td>
      <td>24.5</td>
      <td>23.8</td>
      <td>24.1</td>
      <td>1.00</td>
      <td>509.0</td>
      <td>495.0</td>
      <td>1005.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Minnesota</td>
      <td>1.00</td>
      <td>20.4</td>
      <td>21.5</td>
      <td>21.8</td>
      <td>21.6</td>
      <td>21.5</td>
      <td>0.03</td>
      <td>644.0</td>
      <td>651.0</td>
      <td>1295.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
fig, ax = plt.subplots(1,2, figsize=(15,8))

fig.suptitle('Math Scores for ACT and SAT', fontsize=16)

ax[0].hist(tests[tests['state'] != 'std_dev'].loc[:,'math_act']);
ax[0].set(title='ACT Math');

ax[1].hist(tests[tests['state'] != 'std_dev'].loc[:,'math_sat']);
ax[1].set(title='SAT Math');
```


![png](../images/starter-code_files/starter-code_82_0.png)


##### 18. Plot the Verbal distributions from both data sets.


```python
tests.head(2)
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
fig, ax = plt.subplots(1,3, figsize=(15,8))

fig.suptitle('Verbal Scores for ACT and SAT', fontsize=16)

ax[0].hist(tests[tests['state'] != 'std_dev'].loc[:,'english_act']);
ax[0].set(title='ACT English');

ax[1].hist(tests[tests['state'] != 'std_dev'].loc[:,'reading_act']);
ax[1].set(title='ACT Reading');

ax[2].hist(tests[tests['state'] != 'std_dev'].loc[:,'evidence-based reading and writing_sat']);
ax[2].set(title='SAT Verbal');
```


![png](../images/starter-code_files/starter-code_85_0.png)


### Adding in z-score columns
**Here's what I'm trying to do:**
- Iteratively make new columns with '_zscore' append to each numeric column (probably a for loop)
- For each of those columns, iterate over each state row and calculate z-score, then put it in (probably .apply(lambda x: x- [whichever is appr. mean])
- Then I can use those values as color scales for visualization (in Tableau, or learn with Seaborn or Pyplot)


```python
# tests['math_sat']
dftestlist = [float(tests[tests['state'] == 'std_dev'][i].values) for i in list(tests.columns)[1:]]
```


```python
zscorenames = [i+'_zscore' for i in list(tests.columns)[1:]]
```


```python
zscorenames
```




    ['participation_act_zscore',
     'english_act_zscore',
     'math_act_zscore',
     'reading_act_zscore',
     'science_act_zscore',
     'composite_act_zscore',
     'participation_sat_zscore',
     'evidence-based reading and writing_sat_zscore',
     'math_sat_zscore',
     'total_sat_zscore']




```python
## use .map() or .apply()
```


```python
df = pd.DataFrame(np.random.randint(low=0, high=10, size=(5, 5)),columns=['a', 'b', 'c', 'd', 'e'])
```


```python
for i in tests.columns[1:]:
    for j in zscorenames:
        df[j] = tests[i].mean()
```


```python
tests['math_act'].mean()
```




    20.812739654371992




```python
df[[i+'_zscore' for i in list(tests.columns)[1:]][0]] = np.random.randint(1,10)
```


```python
df['participation_act_zscore'] = df['participation_act_zscore'].apply(lambda x: x - dftestlist[df.columns.get_loc('participation_act_zscore')])
```


```python
df.head()
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
      <th>a</th>
      <th>b</th>
      <th>c</th>
      <th>d</th>
      <th>e</th>
      <th>participation_act_zscore</th>
      <th>english_act_zscore</th>
      <th>math_act_zscore</th>
      <th>reading_act_zscore</th>
      <th>science_act_zscore</th>
      <th>composite_act_zscore</th>
      <th>participation_sat_zscore</th>
      <th>evidence-based reading and writing_sat_zscore</th>
      <th>math_sat_zscore</th>
      <th>total_sat_zscore</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6</td>
      <td>6</td>
      <td>5</td>
      <td>2</td>
      <td>2</td>
      <td>0.999214</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>5</td>
      <td>4</td>
      <td>8</td>
      <td>3</td>
      <td>0.999214</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>8</td>
      <td>0</td>
      <td>6</td>
      <td>7</td>
      <td>0.999214</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>3</td>
      <td>9</td>
      <td>9</td>
      <td>4</td>
      <td>0.999214</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
    </tr>
    <tr>
      <th>4</th>
      <td>7</td>
      <td>0</td>
      <td>5</td>
      <td>6</td>
      <td>0</td>
      <td>0.999214</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
      <td>1106.203529</td>
    </tr>
  </tbody>
</table>
</div>



##### 19. When we make assumptions about how data are distributed, what is the most common assumption?

**A:** Generally we tend to assume it's normally distributed, if anything

##### 20. Does this assumption hold true for any of our columns? Which?


```python
for i in range(len(tests.columns[1:])):
    print(tests.columns[i+1])
```

    participation_act
    english_act
    math_act
    reading_act
    science_act
    composite_act
    participation_sat
    evidence-based reading and writing_sat
    math_sat
    total_sat
    


```python
tests['science_act'][21] = 23.0
```

    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\ipykernel\__main__.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame
    
    See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
      if __name__ == '__main__':
    


```python
fig, ax = plt.subplots(nrows=len(tests.columns[1:]), ncols=1, figsize=(10, 40));

for i in range(len(tests.columns[1:])):
    sns.distplot(
        tests[tests['state'] != 'std_dev'].loc[:,tests.columns[i+1]],
        ax=ax[i],
        kde=True);
    
#     ax[i].set_ylabel(tests.columns[i+1]);
```

    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
      warnings.warn("The 'normed' kwarg is deprecated, and has been "
    


![png](../images/starter-code_files/starter-code_102_1.png)


**A:** If anything, Science ACT scores are closes, but most look multi-modal or very skewed

##### 21. Plot some scatterplots examining relationships between all variables.


```python
# making some things easy on myself by dropping 'std_dev' row
new = tests.drop(52, axis=0)
```


```python
new.tail(3)
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
      <th>state</th>
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>49</th>
      <td>West Virginia</td>
      <td>0.69</td>
      <td>20.0</td>
      <td>19.4</td>
      <td>21.2</td>
      <td>20.5</td>
      <td>20.4</td>
      <td>0.14</td>
      <td>558.0</td>
      <td>528.0</td>
      <td>1086.0</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Wisconsin</td>
      <td>1.00</td>
      <td>19.7</td>
      <td>20.4</td>
      <td>20.6</td>
      <td>20.9</td>
      <td>20.5</td>
      <td>0.03</td>
      <td>642.0</td>
      <td>649.0</td>
      <td>1291.0</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Wyoming</td>
      <td>1.00</td>
      <td>19.4</td>
      <td>19.8</td>
      <td>20.8</td>
      <td>20.6</td>
      <td>20.2</td>
      <td>0.03</td>
      <td>626.0</td>
      <td>604.0</td>
      <td>1230.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
sns.heatmap(new.corr());
```


![png](../images/starter-code_files/starter-code_107_0.png)



```python
sns.heatmap(abs(new.corr()));
```


![png](../images/starter-code_files/starter-code_108_0.png)



```python
sns.pairplot(new);
```


![png](../images/starter-code_files/starter-code_109_0.png)


##### 22. Are there any interesting relationships to note?

**A:** ACT participation and SAT scores are negatively correlated (as well as the converse). This is likely because test-taksrs for those in states where one test has much higher participation than the other means that only ambitious, prepared students are taking the non-default test in their state.

##### 23. Create box plots for each variable. 


```python
fig, ax = plt.subplots(nrows=len(new.columns[1:]), ncols=1, figsize=(10,40));

for i in range(len(new.columns[1:])):
    sns.boxplot(new[new.columns[i+1]],
                notch=False,
                ax=ax[i]);
```

    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\seaborn\categorical.py:454: FutureWarning: remove_na is deprecated and is a private function. Do not use.
      box_data = remove_na(group_data)
    


![png](../images/starter-code_files/starter-code_113_1.png)


##### BONUS: Using Tableau, create a heat map for each variable using a map of the US. 


```python
new.to_csv('../data/merged_test_data.csv')
```

**Tableau dashboard here!**: https://public.tableau.com/profile/jamiequella#!/vizhome/SAT_ACT/Dashboard1

## Step 4: Descriptive and Inferential Statistics

##### 24. Summarize each distribution. As data scientists, be sure to back up these summaries with statistics. (Hint: What are the three things we care about when describing distributions?)


```python
#center, shape, spread. Center and Spread are below for each distribution
new.describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>participation_act</th>
      <td>51.0</td>
      <td>0.652549</td>
      <td>0.321408</td>
      <td>0.08</td>
      <td>0.31</td>
      <td>0.69</td>
      <td>1.00</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>english_act</th>
      <td>51.0</td>
      <td>20.931373</td>
      <td>2.353677</td>
      <td>16.30</td>
      <td>19.00</td>
      <td>20.70</td>
      <td>23.30</td>
      <td>25.5</td>
    </tr>
    <tr>
      <th>math_act</th>
      <td>51.0</td>
      <td>21.182353</td>
      <td>1.981989</td>
      <td>18.00</td>
      <td>19.40</td>
      <td>20.90</td>
      <td>23.10</td>
      <td>25.3</td>
    </tr>
    <tr>
      <th>reading_act</th>
      <td>51.0</td>
      <td>22.013725</td>
      <td>2.067271</td>
      <td>18.10</td>
      <td>20.45</td>
      <td>21.80</td>
      <td>24.15</td>
      <td>26.0</td>
    </tr>
    <tr>
      <th>science_act</th>
      <td>51.0</td>
      <td>21.447059</td>
      <td>1.735552</td>
      <td>18.20</td>
      <td>19.95</td>
      <td>21.30</td>
      <td>23.10</td>
      <td>24.9</td>
    </tr>
    <tr>
      <th>composite_act</th>
      <td>51.0</td>
      <td>21.519608</td>
      <td>2.020695</td>
      <td>17.80</td>
      <td>19.80</td>
      <td>21.40</td>
      <td>23.60</td>
      <td>25.5</td>
    </tr>
    <tr>
      <th>participation_sat</th>
      <td>51.0</td>
      <td>0.398039</td>
      <td>0.352766</td>
      <td>0.02</td>
      <td>0.04</td>
      <td>0.38</td>
      <td>0.66</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>evidence-based reading and writing_sat</th>
      <td>51.0</td>
      <td>569.117647</td>
      <td>45.666901</td>
      <td>482.00</td>
      <td>533.50</td>
      <td>559.00</td>
      <td>613.00</td>
      <td>644.0</td>
    </tr>
    <tr>
      <th>math_sat</th>
      <td>51.0</td>
      <td>556.882353</td>
      <td>47.121395</td>
      <td>468.00</td>
      <td>523.50</td>
      <td>548.00</td>
      <td>599.00</td>
      <td>651.0</td>
    </tr>
    <tr>
      <th>total_sat</th>
      <td>51.0</td>
      <td>1126.098039</td>
      <td>92.494812</td>
      <td>950.00</td>
      <td>1055.50</td>
      <td>1107.00</td>
      <td>1212.00</td>
      <td>1295.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Shapes are below:
fig, ax = plt.subplots(nrows=len(tests.columns[1:]), ncols=1, figsize=(10, 40));

for i in range(len(tests.columns[1:])):
    sns.distplot(
        tests[tests['state'] != 'std_dev'].loc[:,tests.columns[i+1]],
        ax=ax[i],
        kde=True);
```

    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\matplotlib\axes\_axes.py:6462: UserWarning: The 'normed' kwarg is deprecated, and has been replaced by the 'density' kwarg.
      warnings.warn("The 'normed' kwarg is deprecated, and has been "
    


![png](../images/starter-code_files/starter-code_120_1.png)


##### 25. Summarize each relationship. Be sure to back up these summaries with statistics.

**A:** See #21. Summary stats below. 


```python
new.corr()
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
      <th>participation_act</th>
      <th>english_act</th>
      <th>math_act</th>
      <th>reading_act</th>
      <th>science_act</th>
      <th>composite_act</th>
      <th>participation_sat</th>
      <th>evidence-based reading and writing_sat</th>
      <th>math_sat</th>
      <th>total_sat</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>participation_act</th>
      <td>1.000000</td>
      <td>-0.843501</td>
      <td>-0.861114</td>
      <td>-0.866620</td>
      <td>-0.835756</td>
      <td>-0.858134</td>
      <td>-0.841234</td>
      <td>0.716153</td>
      <td>0.682572</td>
      <td>0.701477</td>
    </tr>
    <tr>
      <th>english_act</th>
      <td>-0.843501</td>
      <td>1.000000</td>
      <td>0.967803</td>
      <td>0.985999</td>
      <td>0.979869</td>
      <td>0.990856</td>
      <td>0.686889</td>
      <td>-0.461345</td>
      <td>-0.420673</td>
      <td>-0.441947</td>
    </tr>
    <tr>
      <th>math_act</th>
      <td>-0.861114</td>
      <td>0.967803</td>
      <td>1.000000</td>
      <td>0.979630</td>
      <td>0.986860</td>
      <td>0.990451</td>
      <td>0.710697</td>
      <td>-0.486126</td>
      <td>-0.420456</td>
      <td>-0.454116</td>
    </tr>
    <tr>
      <th>reading_act</th>
      <td>-0.866620</td>
      <td>0.985999</td>
      <td>0.979630</td>
      <td>1.000000</td>
      <td>0.987760</td>
      <td>0.995069</td>
      <td>0.705352</td>
      <td>-0.488441</td>
      <td>-0.442410</td>
      <td>-0.466558</td>
    </tr>
    <tr>
      <th>science_act</th>
      <td>-0.835756</td>
      <td>0.979869</td>
      <td>0.986860</td>
      <td>0.987760</td>
      <td>1.000000</td>
      <td>0.994935</td>
      <td>0.653194</td>
      <td>-0.421383</td>
      <td>-0.364707</td>
      <td>-0.393776</td>
    </tr>
    <tr>
      <th>composite_act</th>
      <td>-0.858134</td>
      <td>0.990856</td>
      <td>0.990451</td>
      <td>0.995069</td>
      <td>0.994935</td>
      <td>1.000000</td>
      <td>0.694748</td>
      <td>-0.470382</td>
      <td>-0.417817</td>
      <td>-0.445020</td>
    </tr>
    <tr>
      <th>participation_sat</th>
      <td>-0.841234</td>
      <td>0.686889</td>
      <td>0.710697</td>
      <td>0.705352</td>
      <td>0.653194</td>
      <td>0.694748</td>
      <td>1.000000</td>
      <td>-0.874326</td>
      <td>-0.855091</td>
      <td>-0.867540</td>
    </tr>
    <tr>
      <th>evidence-based reading and writing_sat</th>
      <td>0.716153</td>
      <td>-0.461345</td>
      <td>-0.486126</td>
      <td>-0.488441</td>
      <td>-0.421383</td>
      <td>-0.470382</td>
      <td>-0.874326</td>
      <td>1.000000</td>
      <td>0.987056</td>
      <td>0.996661</td>
    </tr>
    <tr>
      <th>math_sat</th>
      <td>0.682572</td>
      <td>-0.420673</td>
      <td>-0.420456</td>
      <td>-0.442410</td>
      <td>-0.364707</td>
      <td>-0.417817</td>
      <td>-0.855091</td>
      <td>0.987056</td>
      <td>1.000000</td>
      <td>0.996822</td>
    </tr>
    <tr>
      <th>total_sat</th>
      <td>0.701477</td>
      <td>-0.441947</td>
      <td>-0.454116</td>
      <td>-0.466558</td>
      <td>-0.393776</td>
      <td>-0.445020</td>
      <td>-0.867540</td>
      <td>0.996661</td>
      <td>0.996822</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>



##### 26. Execute a hypothesis test comparing the SAT and ACT participation rates. Use $\alpha = 0.05$. Be sure to interpret your results.


```python
import scipy.stats as stats
```


```python
new[['participation_act','participation_sat']].describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>participation_act</th>
      <td>51.0</td>
      <td>0.652549</td>
      <td>0.321408</td>
      <td>0.08</td>
      <td>0.31</td>
      <td>0.69</td>
      <td>1.00</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>participation_sat</th>
      <td>51.0</td>
      <td>0.398039</td>
      <td>0.352766</td>
      <td>0.02</td>
      <td>0.04</td>
      <td>0.38</td>
      <td>0.66</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# def sampler(population, n=30, k=1000):
#     sample_means = []
    
#     for i in range(k):
#         sample = np.random.choice(population, size=n, replace=True)
#         sample_means.append(np.mean(sample))
    
#     return sample_means
```

#### Hypothesis Testing: Participation Rates
1. Construct null hypothesis (and alternative).
    - H0: The ACT participation rate is the same as SAT participation rate (difference in part. rates = 0)
    - H1: ACT_partic != SAT_partic (dif in part. rates != 0)
2. Specify a level of significance.
    - $\alpha = 0.05$

.   3. Calculate your point estimate


```python
experimental = new['participation_sat']
control = new['participation_act']
```

.   4. Calculate your test statistic


```python
stats.ttest_ind(experimental, control)
```




    Ttest_indResult(statistic=-3.8085778908170544, pvalue=0.00024134203698662353)



.    5. Find your p-value and make a conclusion


```python
alpha = 0.05
p_hyp = stats.ttest_ind(experimental, control)[1]
p_hyp < alpha
```




    True



Since p < $\alpha$, we have evidence to reject H0.

That is, the difference in participation rates between ACT and SAT across states is not 0, and not due to chance

##### 27. Generate and interpret 95% confidence intervals for SAT and ACT participation rates.


```python
def confidencer(sample, sd=0.95):
    """Take in sample and sig. level, then return CI
    sample = dataset
    sd = significance level, default 95%."""
    
    zscore = stats.norm.ppf(1-(1-sd)/2) 
    
    low_ci = sample.mean() - zscore*sample.sem()

    high_ci = sample.mean() + zscore*sample.sem()
    
#     interval = (low_ci, high_ci)
#     print((low_ci, high_ci))

#     print("{0:.0f}% of similar sample means will fall between the range above.".format(sd*100))
    
    return (low_ci, high_ci)
```


```python
confidencer(new['participation_act'])
```




    (0.5643385258470263, 0.7407595133686601)




```python
confidencer(new['participation_sat'], .95)
```




    (0.3012225501733267, 0.49485588119922247)



##### 28. Given your answer to 26, was your answer to 27 surprising? Why?

**A:** No, because knowing that the part. rates are significantly different, I would expect them to have different ranges for the sample means we're getting the 95% confidence intervals for

##### 29. Is it appropriate to generate correlation between SAT and ACT math scores? Why?

**A:** It depends. There are _many_ factors that go into how these avg. state scores came out: educational policies, funding, participation rates (perhaps we can weight correlations by that?), among others. Correlations are fine to look at in general since they are similarly-goaled aptitude tests. However, we should be careful about drawing any major conclusions from just the correlational data we have here.

##### 30. Suppose we only seek to understand the relationship between SAT and ACT data in 2017. Does it make sense to conduct statistical inference given the data we have? Why?

**A:** Yes, because this data comes from that year. From the README:
> These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017.

## EDA FOR PRESENTATION

### ** IGNORE EVERYTHING BELOW HERE FOR NOTEBOOK SCORING ** ###

#### Some questions for myself to explore:
- What states have highest participation rates for ACT? SAT?
    - What can we infer about them?
    
    
- What can we learn from states that have high part. rates of both? Low rates of both?
- What states have the highest deltas btwn SAT and ACT part. rate?
    - Anything else we can learn from these?


- Do we know which states have mandatory testing for either SAT / ACT?

**Some final questions to explore as takeaways for the 'client' group:**
* Do we have any data in regards to college acceptance rates by state that we can correlate to SAT/ACT participation?
* Any median income or other data (5 yrs out) for those who took one test or another?
* Any data on colleges accepting SAT vs. ACT? Common app, etc?
* Is there any benefit to taking both tests? 
    * if not, do you want to throw eggs more into one basket vs. another?


```python
eda = new.copy()
```


```python
eda = eda.rename(columns={
    'participation_act':'act_participation',
    'english_act':'act_eng',
    'math_act':'act_math',
    'reading_act':'act_reading',
    'science_act':'act_sci',
    'composite_act':'act_composite',
    'participation_sat':'sat_participation',
    'evidence-based reading and writing_sat':'sat_erbw',
    'math_sat':'sat_math',
    'total_sat':'sat_total'
})
```


```python
eda.head(2)
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
      <th>state</th>
      <th>act_participation</th>
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_participation</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda[['state','act_participation','sat_participation']].sort_values(by='act_participation', ascending=False)
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
      <th>state</th>
      <th>act_participation</th>
      <th>sat_participation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>0.05</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Kentucky</td>
      <td>1.00</td>
      <td>0.04</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Wisconsin</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Utah</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Tennessee</td>
      <td>1.00</td>
      <td>0.05</td>
    </tr>
    <tr>
      <th>41</th>
      <td>South Carolina</td>
      <td>1.00</td>
      <td>0.50</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Oklahoma</td>
      <td>1.00</td>
      <td>0.07</td>
    </tr>
    <tr>
      <th>34</th>
      <td>North Carolina</td>
      <td>1.00</td>
      <td>0.49</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Nevada</td>
      <td>1.00</td>
      <td>0.26</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Montana</td>
      <td>1.00</td>
      <td>0.10</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Mississippi</td>
      <td>1.00</td>
      <td>0.02</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Minnesota</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Louisiana</td>
      <td>1.00</td>
      <td>0.04</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Missouri</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Wyoming</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Colorado</td>
      <td>1.00</td>
      <td>0.11</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>35</th>
      <td>North Dakota</td>
      <td>0.98</td>
      <td>0.02</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Illinois</td>
      <td>0.93</td>
      <td>0.09</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Hawaii</td>
      <td>0.90</td>
      <td>0.55</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Nebraska</td>
      <td>0.84</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>42</th>
      <td>South Dakota</td>
      <td>0.80</td>
      <td>0.03</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Ohio</td>
      <td>0.75</td>
      <td>0.12</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Florida</td>
      <td>0.73</td>
      <td>0.83</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Kansas</td>
      <td>0.73</td>
      <td>0.04</td>
    </tr>
    <tr>
      <th>49</th>
      <td>West Virginia</td>
      <td>0.69</td>
      <td>0.14</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Iowa</td>
      <td>0.67</td>
      <td>0.02</td>
    </tr>
    <tr>
      <th>32</th>
      <td>New Mexico</td>
      <td>0.66</td>
      <td>0.11</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>0.38</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>0.30</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Georgia</td>
      <td>0.55</td>
      <td>0.61</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Texas</td>
      <td>0.45</td>
      <td>0.62</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Oregon</td>
      <td>0.40</td>
      <td>0.43</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Idaho</td>
      <td>0.38</td>
      <td>0.93</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Indiana</td>
      <td>0.35</td>
      <td>0.63</td>
    </tr>
    <tr>
      <th>31</th>
      <td>New Jersey</td>
      <td>0.34</td>
      <td>0.70</td>
    </tr>
    <tr>
      <th>9</th>
      <td>District of Columbia</td>
      <td>0.32</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Connecticut</td>
      <td>0.31</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>California</td>
      <td>0.31</td>
      <td>0.53</td>
    </tr>
    <tr>
      <th>33</th>
      <td>New York</td>
      <td>0.31</td>
      <td>0.67</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Michigan</td>
      <td>0.29</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Massachusetts</td>
      <td>0.29</td>
      <td>0.76</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Vermont</td>
      <td>0.29</td>
      <td>0.60</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Virginia</td>
      <td>0.29</td>
      <td>0.65</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Washington</td>
      <td>0.29</td>
      <td>0.64</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Maryland</td>
      <td>0.28</td>
      <td>0.69</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Pennsylvania</td>
      <td>0.23</td>
      <td>0.65</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Rhode Island</td>
      <td>0.21</td>
      <td>0.71</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Delaware</td>
      <td>0.18</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>30</th>
      <td>New Hampshire</td>
      <td>0.18</td>
      <td>0.96</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Maine</td>
      <td>0.08</td>
      <td>0.95</td>
    </tr>
  </tbody>
</table>
</div>




```python
# creating a column that measures difference in ACT and SAT participation
eda['particip_dif_act_sat'] = eda['act_participation'] - eda['sat_participation']
```


```python

fig, ax = plt.subplots(figsize=(15,10));
ax = plt.gca();
eda['particip_dif_act_sat'].sort_values().plot(kind='barh', color='mediumorchid');
ax.set_yticklabels([i for i in eda['state'][eda['particip_dif_act_sat'].sort_values().index]]);
```


![png](../images/starter-code_files/starter-code_154_0.png)


#### Creating a regional map for states to dig into the data a little deeper...

From here: https://en.wikipedia.org/wiki/List_of_regions_of_the_United_States#Interstate_regions


```python
# dict for state -> region
region_map = {'Connecticut': 'Northeast', 'Maine': 'Northeast', 'Massachusetts': 'Northeast',
             'New Hampshire': 'Northeast', 'Rhode Island': 'Northeast', 'Vermont': 'Northeast',
             'New Jersey': 'Northeast', 'New York': 'Northeast', 'Pennsylvania': 'Northeast',
             'Illinois': 'Midwest', 'Indiana': 'Midwest', 'Michigan': 'Midwest', 'Ohio': 'Midwest', 'Wisconsin': 'Midwest',
             'Iowa': 'Midwest', 'Kansas':'Midwest', 'Minnesota': 'Midwest', 'Missouri': 'Midwest', 'Nebraska': 'Midwest',
             'North Dakota':'Midwest', 'South Dakota': 'Midwest',
             'Delaware': 'South', 'Florida':'South', 'Georgia':'South', 'Maryland':'South', 'North Carolina':'South',
             'South Carolina':'South', 'Virginia':'South', 'District of Columbia':'South', 'West Virginia':'South',
             'West Virginia':'South', 'Alabama':'South', 'Kentucky':'South', 'Mississippi':'South', 'Tennessee':'South',
             'Arkansas':'South', 'Louisiana':'South', 'Oklahoma':'South', 'Texas':'South',
             'Arizona':'West', 'Colorado':'West', 'Idaho':'West', 'Montana':'West', 'Nevada':'West', 'New Mexico':'West',
             'Utah':'West', 'Wyoming':'West', 'Alaska':'West', 'California':'West', 'Hawaii':'West', 'Oregon':'West',
             'Washington':'West'}
```


```python
#creating a column to map a region for each state row
eda['region'] = [region_map[i] for i in eda['state']]
```


```python
eda.head()
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
      <th>state</th>
      <th>act_participation</th>
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_participation</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
      <th>particip_dif_act_sat</th>
      <th>region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
      <td>0.95</td>
      <td>South</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
      <td>0.27</td>
      <td>West</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Arizona</td>
      <td>0.62</td>
      <td>18.6</td>
      <td>19.8</td>
      <td>20.1</td>
      <td>19.8</td>
      <td>19.7</td>
      <td>0.30</td>
      <td>563.0</td>
      <td>553.0</td>
      <td>1116.0</td>
      <td>0.32</td>
      <td>West</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Arkansas</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>19.0</td>
      <td>19.7</td>
      <td>19.5</td>
      <td>19.4</td>
      <td>0.03</td>
      <td>614.0</td>
      <td>594.0</td>
      <td>1208.0</td>
      <td>0.97</td>
      <td>South</td>
    </tr>
    <tr>
      <th>5</th>
      <td>California</td>
      <td>0.31</td>
      <td>22.5</td>
      <td>22.7</td>
      <td>23.1</td>
      <td>22.2</td>
      <td>22.8</td>
      <td>0.53</td>
      <td>531.0</td>
      <td>524.0</td>
      <td>1055.0</td>
      <td>-0.22</td>
      <td>West</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda.groupby(by='region')['particip_dif_act_sat'].mean()
```




    region
    Midwest      0.605833
    Northeast   -0.528889
    South        0.332941
    West         0.370000
    Name: particip_dif_act_sat, dtype: float64




```python
eda.groupby(by='region')['particip_dif_act_sat'].mean().index
```




    Index(['Midwest', 'Northeast', 'South', 'West'], dtype='object', name='region')




```python
SO = eda[eda['region']=='South']['particip_dif_act_sat']
WE = eda[eda['region']=='West']['particip_dif_act_sat']
NE = eda[eda['region']=='Northeast']['particip_dif_act_sat']
MW = eda[eda['region']=='Midwest']['particip_dif_act_sat']

fig, ax = plt.subplots(nrows=2, ncols=2, figsize=(15,10));

width = 2
size = 14

ax[0,0].barh(y=eda.loc[SO.sort_values().index, 'state'].values, width=SO.sort_values(), color='mediumorchid');
ax[0,0].axvline(x=0, color='gray', linewidth=width);
ax[0,0].set_title('South Region', fontsize=size);
ax[0,0].set_xlim(left=-1, right=1);
ax[0,0].tick_params(labelleft=False);

ax[0,1].barh(y=eda.loc[WE.sort_values().index, 'state'].values, width=WE.sort_values(), color='mediumseagreen');
ax[0,1].axvline(x=0, color='gray', linewidth=width);
ax[0,1].set_title('West Region', fontsize=size);
ax[0,1].set_xlim(left=-1, right=1);
ax[0,1].tick_params(labelleft=False);

ax[1,0].barh(y=eda.loc[NE.sort_values().index, 'state'].values, width=NE.sort_values(), color='mediumslateblue');
ax[1,0].axvline(x=0, color='gray', linewidth=width);
ax[1,0].set_title('Northeast Region', fontsize=size);
ax[1,0].set_xlim(left=-1, right=1);
ax[1,0].tick_params(labelleft=False);

ax[1,1].barh(y=eda.loc[MW.sort_values().index, 'state'].values, width=MW.sort_values(), color='salmon');
ax[1,1].axvline(x=0, color='gray', linewidth=width);
ax[1,1].set_title('Midwest Region', fontsize=size);
ax[1,1].set_xlim(left=-1, right=1);
ax[1,1].tick_params(labelleft=False);
```


![png](../images/starter-code_files/starter-code_161_0.png)



```python
SO = eda[eda['region']=='South']['particip_dif_act_sat']
WE = eda[eda['region']=='West']['particip_dif_act_sat']
# NE = eda[eda['region']=='Northeast']['particip_dif_act_sat']
# MW = eda[eda['region']=='Midwest']['particip_dif_act_sat']

fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(20,8));

width = 2
size = 18

ax[0].barh(y=eda.loc[SO.sort_values().index, 'state'].values, width=SO.sort_values(), color='mediumorchid');
ax[0].axvline(x=0, color='gray', linewidth=width);
ax[0].set_title('South Region', fontsize=size, weight='bold');
ax[0].set_xlim(left=-1, right=1);
ax[0].tick_params(labelsize=16);

ax[1].barh(y=eda.loc[WE.sort_values().index, 'state'].values, width=WE.sort_values(), color='mediumseagreen');
ax[1].axvline(x=0, color='gray', linewidth=width);
ax[1].set_title('West Region', fontsize=size, weight='bold');
ax[1].set_xlim(left=-1, right=1);
ax[1].tick_params(labelsize=16);
```


![png](../images/starter-code_files/starter-code_162_0.png)



```python
# Checking out South

# getting aggregate data for South, just SAT participation
agg = eda[eda['region'] == 'South']['sat_participation'].sort_values()

#setting xtick labels
xlabs = [eda.iloc[i-1,0] for i in agg.index]

#setting up figsize
fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10,6));

#barplot by region for ACT participation
agg.plot(kind='bar', ax=fig.gca(), color='mediumseagreen');


#setting some labels
ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('South',fontsize=14);
ax.set_ylabel('SAT Participation Rate', fontsize=14);
```


![png](../images/starter-code_files/starter-code_163_0.png)



```python
eda['particip_total'] = eda['act_participation'] + eda['sat_participation']
```


```python
xlabs = [i for i in eda['state'][eda['particip_total'].sort_values().index]]

fig, ax = plt.subplots(figsize=(15,10));
ax = plt.gca();

eda['particip_total'].sort_values(ascending=False).plot(kind='bar', color='lightsteelblue');

ax.set_xticklabels(xlabs, fontsize=14);
```


![png](../images/starter-code_files/starter-code_165_0.png)



```python
# Checking out which regions over/under-index on ACT participation, compared to SAT participation

xlabs = [i for i in eda.groupby(by='region')['particip_dif_act_sat'].mean().index]

fig, ax = plt.subplots(figsize=(15,10));
ax = plt.gca();

eda.groupby(by='region')['particip_dif_act_sat'].mean().plot(kind='bar', color='g');

ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Region', fontsize=14);
ax.set_ylabel('Participation Rate Difference (ACT - SAT)', fontsize=14);

plt.axhline(y=0, linestyle='dashed', color='gray', linewidth=4, zorder=2);
```


![png](../images/starter-code_files/starter-code_166_0.png)



```python
# Checking out which regions over/under-index on ACT participation, compared to SAT participation

# getting aggregate data by region
agg = eda.groupby(by='region')[['act_participation', 'sat_participation']].mean()

#setting xtick labels
xlabs = [i for i in agg.index]

#setting up figsize
fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10,6));

#barplot by region for ACT and SAT participation
agg.plot(kind='bar', ax=fig.gca());


#setting some labels
ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Region',fontsize=14);
ax.set_ylabel('Test Participation Rate', fontsize=14);

ax.legend(('ACT Participation', 'SAT Participation'),fontsize=12);
```


![png](../images/starter-code_files/starter-code_167_0.png)



```python
agg = eda.groupby(by='region')[['act_participation', 'sat_participation']].mean()
agg
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
      <th>act_participation</th>
      <th>sat_participation</th>
    </tr>
    <tr>
      <th>region</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Midwest</th>
      <td>0.778333</td>
      <td>0.172500</td>
    </tr>
    <tr>
      <th>Northeast</th>
      <td>0.248889</td>
      <td>0.777778</td>
    </tr>
    <tr>
      <th>South</th>
      <td>0.734706</td>
      <td>0.401765</td>
    </tr>
    <tr>
      <th>West</th>
      <td>0.708462</td>
      <td>0.338462</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda[eda['region'] == 'Northeast']
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
      <th>state</th>
      <th>act_participation</th>
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_participation</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
      <th>particip_dif_act_sat</th>
      <th>region</th>
      <th>particip_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7</th>
      <td>Connecticut</td>
      <td>0.31</td>
      <td>25.5</td>
      <td>24.6</td>
      <td>25.6</td>
      <td>24.6</td>
      <td>25.2</td>
      <td>1.00</td>
      <td>530.0</td>
      <td>512.0</td>
      <td>1041.0</td>
      <td>-0.69</td>
      <td>Northeast</td>
      <td>1.31</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Maine</td>
      <td>0.08</td>
      <td>24.2</td>
      <td>24.0</td>
      <td>24.8</td>
      <td>23.7</td>
      <td>24.3</td>
      <td>0.95</td>
      <td>513.0</td>
      <td>499.0</td>
      <td>1012.0</td>
      <td>-0.87</td>
      <td>Northeast</td>
      <td>1.03</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Massachusetts</td>
      <td>0.29</td>
      <td>25.4</td>
      <td>25.3</td>
      <td>25.9</td>
      <td>24.7</td>
      <td>25.4</td>
      <td>0.76</td>
      <td>555.0</td>
      <td>551.0</td>
      <td>1107.0</td>
      <td>-0.47</td>
      <td>Northeast</td>
      <td>1.05</td>
    </tr>
    <tr>
      <th>30</th>
      <td>New Hampshire</td>
      <td>0.18</td>
      <td>25.4</td>
      <td>25.1</td>
      <td>26.0</td>
      <td>24.9</td>
      <td>25.5</td>
      <td>0.96</td>
      <td>532.0</td>
      <td>520.0</td>
      <td>1052.0</td>
      <td>-0.78</td>
      <td>Northeast</td>
      <td>1.14</td>
    </tr>
    <tr>
      <th>31</th>
      <td>New Jersey</td>
      <td>0.34</td>
      <td>23.8</td>
      <td>23.8</td>
      <td>24.1</td>
      <td>23.2</td>
      <td>23.9</td>
      <td>0.70</td>
      <td>530.0</td>
      <td>526.0</td>
      <td>1056.0</td>
      <td>-0.36</td>
      <td>Northeast</td>
      <td>1.04</td>
    </tr>
    <tr>
      <th>33</th>
      <td>New York</td>
      <td>0.31</td>
      <td>23.8</td>
      <td>24.0</td>
      <td>24.6</td>
      <td>23.9</td>
      <td>24.2</td>
      <td>0.67</td>
      <td>528.0</td>
      <td>523.0</td>
      <td>1052.0</td>
      <td>-0.36</td>
      <td>Northeast</td>
      <td>0.98</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Pennsylvania</td>
      <td>0.23</td>
      <td>23.4</td>
      <td>23.4</td>
      <td>24.2</td>
      <td>23.3</td>
      <td>23.7</td>
      <td>0.65</td>
      <td>540.0</td>
      <td>531.0</td>
      <td>1071.0</td>
      <td>-0.42</td>
      <td>Northeast</td>
      <td>0.88</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Rhode Island</td>
      <td>0.21</td>
      <td>24.0</td>
      <td>23.3</td>
      <td>24.7</td>
      <td>23.4</td>
      <td>24.0</td>
      <td>0.71</td>
      <td>539.0</td>
      <td>524.0</td>
      <td>1062.0</td>
      <td>-0.50</td>
      <td>Northeast</td>
      <td>0.92</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Vermont</td>
      <td>0.29</td>
      <td>23.3</td>
      <td>23.1</td>
      <td>24.4</td>
      <td>23.2</td>
      <td>23.6</td>
      <td>0.60</td>
      <td>562.0</td>
      <td>551.0</td>
      <td>1114.0</td>
      <td>-0.31</td>
      <td>Northeast</td>
      <td>0.89</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Checking out NE

# getting aggregate data for NE, just ACT participation
agg = eda[eda['region'] == 'Northeast']['act_participation'].sort_values()

#setting xtick labels
xlabs = [eda.iloc[i-1,0] for i in agg.index]

#setting up figsize
fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10,6));

#barplot by region for ACT participation
agg.plot(kind='bar', ax=fig.gca(), color='lightsteelblue');


#setting some labels
ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Northeast',fontsize=14);
ax.set_ylabel('ACT Participation Rate', fontsize=14);

# ax.legend(('ACT Participation', ''),fontsize=12);
```


![png](../images/starter-code_files/starter-code_170_0.png)



```python
# Checking out NE

# getting aggregate data for NE, just SAT participation
agg = eda[eda['region'] == 'Northeast']['sat_participation'].sort_values()

#setting xtick labels
xlabs = [eda.iloc[i-1,0] for i in agg.index]

#setting up figsize
fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10,6));

#barplot by region for SAT participation
agg.plot(kind='bar', ax=fig.gca(), color='lightsteelblue');


#setting some labels
ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Northeast',fontsize=14);
ax.set_ylabel('SAT Participation Rate', fontsize=14);

```


![png](../images/starter-code_files/starter-code_171_0.png)



```python
# Checking out low SAT participation region

# getting aggregate data for MW, just SAT participation
agg = eda[eda['region'] == 'Midwest']['sat_participation'].sort_values()

#setting xtick labels
xlabs = [eda.iloc[i-1,0] for i in agg.index]

#setting up figsize
fig, ax = plt.subplots(nrows=1, ncols=1, figsize=(10,6));

#barplot by region for SAT participation
agg.plot(kind='bar', ax=fig.gca(), color='lightsteelblue');


#setting some labels
ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Midwest',fontsize=14);
ax.set_ylabel('SAT Participation Rate', fontsize=14);

# ax.legend(('ACT Participation', ''),fontsize=12);
```


![png](../images/starter-code_files/starter-code_172_0.png)



```python
# Checking out which regions over/under-index on ACT participation, compared to SAT participation

xlabs = [i for i in eda.groupby(by='region')['particip_dif_act_sat'].mean().index]

fig, ax = plt.subplots(figsize=(15,10));
ax = plt.gca();

plt.bar(x=xlabs, height=[i*-1 for i in eda.groupby(by='region')['particip_dif_act_sat'].mean()], color='r');

ax.set_xticklabels(xlabs, fontsize=14);
ax.set_xlabel('Region', fontsize=14);
ax.set_ylabel('Participation Rate Difference (SAT - ACT)', fontsize=14);
# ax.set_yticklabels(ax.yaxis.get_majorticklabels(), fontsize=14)

# ax.yaxis.get_major_ticks()

# label = ax.yaxis.get_major_ticks()
# label.set_fontsize(14);

plt.axhline(y=0, linestyle='dashed', color='gray', linewidth=4, zorder=2);
```


![png](../images/starter-code_files/starter-code_173_0.png)


### Standardizing data


```python
norm = eda.copy()

norm.head(2)
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
      <th>state</th>
      <th>act_participation</th>
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_participation</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
      <th>particip_dif_act_sat</th>
      <th>region</th>
      <th>particip_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Alabama</td>
      <td>1.00</td>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>0.05</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
      <td>0.95</td>
      <td>South</td>
      <td>1.05</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Alaska</td>
      <td>0.65</td>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>0.38</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
      <td>0.27</td>
      <td>West</td>
      <td>1.03</td>
    </tr>
  </tbody>
</table>
</div>




```python
drop_cols = ['state', 'region', 'act_participation', 'sat_participation', 'particip_dif_act_sat','particip_total']
norm.drop(labels=drop_cols, axis=1, inplace=True)
norm.head(2)
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
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>18.9</td>
      <td>18.4</td>
      <td>19.7</td>
      <td>19.4</td>
      <td>19.2</td>
      <td>593.0</td>
      <td>572.0</td>
      <td>1165.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>18.7</td>
      <td>19.8</td>
      <td>20.4</td>
      <td>19.9</td>
      <td>19.8</td>
      <td>547.0</td>
      <td>533.0</td>
      <td>1080.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
norm = (norm - norm.mean()) / norm.std()

norm.head(8)
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
      <th>act_eng</th>
      <th>act_math</th>
      <th>act_reading</th>
      <th>act_sci</th>
      <th>act_composite</th>
      <th>sat_erbw</th>
      <th>sat_math</th>
      <th>sat_total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>-0.863063</td>
      <td>-1.403818</td>
      <td>-1.119218</td>
      <td>-1.179486</td>
      <td>-1.147926</td>
      <td>0.522969</td>
      <td>0.320823</td>
      <td>0.420585</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.948037</td>
      <td>-0.697457</td>
      <td>-0.780607</td>
      <td>-0.891393</td>
      <td>-0.850998</td>
      <td>-0.484326</td>
      <td>-0.506826</td>
      <td>-0.498385</td>
    </tr>
    <tr>
      <th>3</th>
      <td>-0.990524</td>
      <td>-0.697457</td>
      <td>-0.925726</td>
      <td>-0.949011</td>
      <td>-0.900486</td>
      <td>-0.133962</td>
      <td>-0.082390</td>
      <td>-0.109174</td>
    </tr>
    <tr>
      <th>4</th>
      <td>-0.863063</td>
      <td>-1.101092</td>
      <td>-1.119218</td>
      <td>-1.121867</td>
      <td>-1.048950</td>
      <td>0.982820</td>
      <td>0.787703</td>
      <td>0.885476</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.666458</td>
      <td>0.765719</td>
      <td>0.525463</td>
      <td>0.433834</td>
      <td>0.633640</td>
      <td>-0.834689</td>
      <td>-0.697822</td>
      <td>-0.768671</td>
    </tr>
    <tr>
      <th>6</th>
      <td>-0.353223</td>
      <td>-0.445185</td>
      <td>-0.393623</td>
      <td>-0.315207</td>
      <td>-0.356119</td>
      <td>0.807639</td>
      <td>0.808924</td>
      <td>0.809796</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1.941060</td>
      <td>1.724352</td>
      <td>1.734787</td>
      <td>1.816679</td>
      <td>1.821350</td>
      <td>-0.856586</td>
      <td>-0.952484</td>
      <td>-0.920030</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1.346246</td>
      <td>1.118900</td>
      <td>1.347803</td>
      <td>1.240494</td>
      <td>1.276983</td>
      <td>-1.447824</td>
      <td>-1.376919</td>
      <td>-1.406544</td>
    </tr>
  </tbody>
</table>
</div>




```python
norm.describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>act_eng</th>
      <td>51.0</td>
      <td>6.182418e-16</td>
      <td>1.0</td>
      <td>-1.967718</td>
      <td>-0.820577</td>
      <td>-0.098303</td>
      <td>1.006352</td>
      <td>1.941060</td>
    </tr>
    <tr>
      <th>act_math</th>
      <td>51.0</td>
      <td>1.155938e-15</td>
      <td>1.0</td>
      <td>-1.605636</td>
      <td>-0.899275</td>
      <td>-0.142459</td>
      <td>0.967536</td>
      <td>2.077532</td>
    </tr>
    <tr>
      <th>act_reading</th>
      <td>51.0</td>
      <td>9.970238e-16</td>
      <td>1.0</td>
      <td>-1.893185</td>
      <td>-0.756420</td>
      <td>-0.103385</td>
      <td>1.033379</td>
      <td>1.928279</td>
    </tr>
    <tr>
      <th>act_sci</th>
      <td>51.0</td>
      <td>-1.140700e-15</td>
      <td>1.0</td>
      <td>-1.870908</td>
      <td>-0.862584</td>
      <td>-0.084733</td>
      <td>0.952401</td>
      <td>1.989535</td>
    </tr>
    <tr>
      <th>act_composite</th>
      <td>51.0</td>
      <td>-1.306145e-17</td>
      <td>1.0</td>
      <td>-1.840757</td>
      <td>-0.850998</td>
      <td>-0.059191</td>
      <td>1.029543</td>
      <td>1.969814</td>
    </tr>
    <tr>
      <th>sat_erbw</th>
      <td>51.0</td>
      <td>-1.480297e-16</td>
      <td>1.0</td>
      <td>-1.907676</td>
      <td>-0.779944</td>
      <td>-0.221553</td>
      <td>0.960922</td>
      <td>1.639751</td>
    </tr>
    <tr>
      <th>sat_math</th>
      <td>51.0</td>
      <td>1.371452e-16</td>
      <td>1.0</td>
      <td>-1.886242</td>
      <td>-0.708433</td>
      <td>-0.188499</td>
      <td>0.893812</td>
      <td>1.997344</td>
    </tr>
    <tr>
      <th>sat_total</th>
      <td>51.0</td>
      <td>9.752547e-16</td>
      <td>1.0</td>
      <td>-1.903869</td>
      <td>-0.763265</td>
      <td>-0.206477</td>
      <td>0.928722</td>
      <td>1.826070</td>
    </tr>
  </tbody>
</table>
</div>




```python
norm.median().mean()
```




    -0.1380751625048331




```python
ecolors = {'act_eng':'ACT', 'act_math':'ACT', 'act_reading':'ACT', 
           'act_sci':'ACT', 'act_composite':'ACT',
           'sat_erbw':'SAT', 'sat_math':'SAT', 'sat_total':'SAT'}

xticks = ['ACT: Eng.', 'ACT: Math', 'ACT: Reading', 'ACT: Science', 'ACT: Composite','SAT: ERBW', 'SAT: Math','SAT: Total']

fig, ax = plt.subplots(1,1, figsize=(22,10));
ax=fig.gca();


sns.boxplot(x=norm.columns, y=[norm[i] for i in norm.columns], notch=True, hue=[ecolors[col] for col in norm.columns]);

ax.set_xticklabels(xticks)
ax.tick_params(labelsize=18);

# ax.axhline(y=norm.median().mean(), linestyle='dashed', color='gray', linewidth=2);

# ax.text(x=12, y=norm.median().mean()+0.3, s='Mean of boxplot medians', fontsize=12, color='white');

ax.legend(fontsize=14);
```

    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\seaborn\categorical.py:482: FutureWarning: remove_na is deprecated and is a private function. Do not use.
      box_data = remove_na(group_data[hue_mask])
    C:\Users\james\Anaconda3\envs\dsi\lib\site-packages\numpy\core\fromnumeric.py:52: FutureWarning: reshape is deprecated and will raise in a subsequent release. Please use .values.reshape(...) instead
      return getattr(obj, method)(*args, **kwds)
    


![png](../images/starter-code_files/starter-code_180_1.png)



```python
# gcolors = {'act_eng':'mediumpurple', 'act_math':'mediumpurple', 'act_reading':'mediumpurple', 
#            'act_sci':'mediumpurple', 'act_composite':'mediumpurple',
#            'sat_erbw':'gold', 'sat_math':'gold', 'sat_total':'gold'}

# fig, ax = plt.subplots(nrows=1, ncols=1, figsize = ((15, 8)));
# ax = fig.gca();

# fig.suptitle('Mean of Standardized Scores', fontsize=18);

# ax.bar(x=norm.columns, height=norm.mean(),color=[gcolors[col] for col in norm.columns]);

# ax.tick_params(labelsize=14);
# ax.legend(('ACT sections', 'SAT sections'), fontsize=14);
```


```python
print(norm.std()[:5].mean())
print(norm.std()[5:].mean())
```

    1.0
    1.0
    


```python
norm.describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>act_eng</th>
      <td>51.0</td>
      <td>6.182418e-16</td>
      <td>1.0</td>
      <td>-1.967718</td>
      <td>-0.820577</td>
      <td>-0.098303</td>
      <td>1.006352</td>
      <td>1.941060</td>
    </tr>
    <tr>
      <th>act_math</th>
      <td>51.0</td>
      <td>1.155938e-15</td>
      <td>1.0</td>
      <td>-1.605636</td>
      <td>-0.899275</td>
      <td>-0.142459</td>
      <td>0.967536</td>
      <td>2.077532</td>
    </tr>
    <tr>
      <th>act_reading</th>
      <td>51.0</td>
      <td>9.970238e-16</td>
      <td>1.0</td>
      <td>-1.893185</td>
      <td>-0.756420</td>
      <td>-0.103385</td>
      <td>1.033379</td>
      <td>1.928279</td>
    </tr>
    <tr>
      <th>act_sci</th>
      <td>51.0</td>
      <td>-1.140700e-15</td>
      <td>1.0</td>
      <td>-1.870908</td>
      <td>-0.862584</td>
      <td>-0.084733</td>
      <td>0.952401</td>
      <td>1.989535</td>
    </tr>
    <tr>
      <th>act_composite</th>
      <td>51.0</td>
      <td>-1.306145e-17</td>
      <td>1.0</td>
      <td>-1.840757</td>
      <td>-0.850998</td>
      <td>-0.059191</td>
      <td>1.029543</td>
      <td>1.969814</td>
    </tr>
    <tr>
      <th>sat_erbw</th>
      <td>51.0</td>
      <td>-1.480297e-16</td>
      <td>1.0</td>
      <td>-1.907676</td>
      <td>-0.779944</td>
      <td>-0.221553</td>
      <td>0.960922</td>
      <td>1.639751</td>
    </tr>
    <tr>
      <th>sat_math</th>
      <td>51.0</td>
      <td>1.371452e-16</td>
      <td>1.0</td>
      <td>-1.886242</td>
      <td>-0.708433</td>
      <td>-0.188499</td>
      <td>0.893812</td>
      <td>1.997344</td>
    </tr>
    <tr>
      <th>sat_total</th>
      <td>51.0</td>
      <td>9.752547e-16</td>
      <td>1.0</td>
      <td>-1.903869</td>
      <td>-0.763265</td>
      <td>-0.206477</td>
      <td>0.928722</td>
      <td>1.826070</td>
    </tr>
  </tbody>
</table>
</div>




```python
mask1 = (eda['region'] == 'South') & (eda['sat_participation'] > eda['act_participation'])
mask2 = (eda['region'] == 'South') & (eda['sat_participation'] < eda['act_participation'])
```


```python
eda[mask1].describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>act_participation</th>
      <td>7.0</td>
      <td>0.400000</td>
      <td>0.189385</td>
      <td>0.18</td>
      <td>0.285</td>
      <td>0.32</td>
      <td>0.500</td>
      <td>0.73</td>
    </tr>
    <tr>
      <th>act_eng</th>
      <td>7.0</td>
      <td>22.114286</td>
      <td>2.246055</td>
      <td>19.00</td>
      <td>20.250</td>
      <td>23.30</td>
      <td>23.800</td>
      <td>24.40</td>
    </tr>
    <tr>
      <th>act_math</th>
      <td>7.0</td>
      <td>22.042857</td>
      <td>1.671184</td>
      <td>19.40</td>
      <td>20.800</td>
      <td>23.10</td>
      <td>23.350</td>
      <td>23.50</td>
    </tr>
    <tr>
      <th>act_reading</th>
      <td>7.0</td>
      <td>23.228571</td>
      <td>1.783923</td>
      <td>21.00</td>
      <td>21.550</td>
      <td>24.20</td>
      <td>24.700</td>
      <td>24.90</td>
    </tr>
    <tr>
      <th>act_sci</th>
      <td>7.0</td>
      <td>22.171429</td>
      <td>1.648953</td>
      <td>19.40</td>
      <td>21.100</td>
      <td>23.00</td>
      <td>23.500</td>
      <td>23.60</td>
    </tr>
    <tr>
      <th>act_composite</th>
      <td>7.0</td>
      <td>22.514286</td>
      <td>1.829780</td>
      <td>19.80</td>
      <td>21.050</td>
      <td>23.60</td>
      <td>23.950</td>
      <td>24.20</td>
    </tr>
    <tr>
      <th>sat_participation</th>
      <td>7.0</td>
      <td>0.771429</td>
      <td>0.172378</td>
      <td>0.61</td>
      <td>0.635</td>
      <td>0.69</td>
      <td>0.915</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>sat_erbw</th>
      <td>7.0</td>
      <td>521.428571</td>
      <td>25.592037</td>
      <td>482.00</td>
      <td>508.000</td>
      <td>520.00</td>
      <td>535.500</td>
      <td>561.00</td>
    </tr>
    <tr>
      <th>sat_math</th>
      <td>7.0</td>
      <td>506.285714</td>
      <td>23.634116</td>
      <td>468.00</td>
      <td>494.500</td>
      <td>507.00</td>
      <td>519.500</td>
      <td>541.00</td>
    </tr>
    <tr>
      <th>sat_total</th>
      <td>7.0</td>
      <td>1027.857143</td>
      <td>48.779875</td>
      <td>950.00</td>
      <td>1006.500</td>
      <td>1020.00</td>
      <td>1055.000</td>
      <td>1102.00</td>
    </tr>
    <tr>
      <th>particip_dif_act_sat</th>
      <td>7.0</td>
      <td>-0.371429</td>
      <td>0.291343</td>
      <td>-0.82</td>
      <td>-0.545</td>
      <td>-0.36</td>
      <td>-0.135</td>
      <td>-0.06</td>
    </tr>
    <tr>
      <th>particip_total</th>
      <td>7.0</td>
      <td>1.171429</td>
      <td>0.215130</td>
      <td>0.94</td>
      <td>1.020</td>
      <td>1.16</td>
      <td>1.250</td>
      <td>1.56</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda[mask2].describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>act_participation</th>
      <td>10.0</td>
      <td>0.969</td>
      <td>0.098031</td>
      <td>0.69</td>
      <td>1.0000</td>
      <td>1.000</td>
      <td>1.0000</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>act_eng</th>
      <td>10.0</td>
      <td>18.830</td>
      <td>0.821989</td>
      <td>17.50</td>
      <td>18.2750</td>
      <td>18.900</td>
      <td>19.4750</td>
      <td>20.00</td>
    </tr>
    <tr>
      <th>act_math</th>
      <td>10.0</td>
      <td>18.900</td>
      <td>0.442217</td>
      <td>18.10</td>
      <td>18.6500</td>
      <td>18.900</td>
      <td>19.2750</td>
      <td>19.40</td>
    </tr>
    <tr>
      <th>act_reading</th>
      <td>10.0</td>
      <td>19.860</td>
      <td>0.678561</td>
      <td>18.80</td>
      <td>19.6250</td>
      <td>19.750</td>
      <td>20.1000</td>
      <td>21.20</td>
    </tr>
    <tr>
      <th>act_sci</th>
      <td>10.0</td>
      <td>19.560</td>
      <td>0.516828</td>
      <td>18.80</td>
      <td>19.3250</td>
      <td>19.550</td>
      <td>19.8250</td>
      <td>20.50</td>
    </tr>
    <tr>
      <th>act_composite</th>
      <td>10.0</td>
      <td>19.410</td>
      <td>0.556677</td>
      <td>18.60</td>
      <td>19.1250</td>
      <td>19.400</td>
      <td>19.7250</td>
      <td>20.40</td>
    </tr>
    <tr>
      <th>sat_participation</th>
      <td>10.0</td>
      <td>0.143</td>
      <td>0.188447</td>
      <td>0.02</td>
      <td>0.0400</td>
      <td>0.050</td>
      <td>0.1225</td>
      <td>0.50</td>
    </tr>
    <tr>
      <th>sat_erbw</th>
      <td>10.0</td>
      <td>588.300</td>
      <td>40.100014</td>
      <td>530.00</td>
      <td>549.0000</td>
      <td>602.000</td>
      <td>620.7500</td>
      <td>634.00</td>
    </tr>
    <tr>
      <th>sat_math</th>
      <td>10.0</td>
      <td>568.000</td>
      <td>38.924428</td>
      <td>517.00</td>
      <td>529.7500</td>
      <td>579.000</td>
      <td>601.5000</td>
      <td>616.00</td>
    </tr>
    <tr>
      <th>sat_total</th>
      <td>10.0</td>
      <td>1156.600</td>
      <td>79.075491</td>
      <td>1047.00</td>
      <td>1082.2500</td>
      <td>1181.500</td>
      <td>1223.0000</td>
      <td>1247.00</td>
    </tr>
    <tr>
      <th>particip_dif_act_sat</th>
      <td>10.0</td>
      <td>0.826</td>
      <td>0.211933</td>
      <td>0.50</td>
      <td>0.6450</td>
      <td>0.950</td>
      <td>0.9600</td>
      <td>0.98</td>
    </tr>
    <tr>
      <th>particip_total</th>
      <td>10.0</td>
      <td>1.112</td>
      <td>0.212906</td>
      <td>0.83</td>
      <td>1.0325</td>
      <td>1.045</td>
      <td>1.0650</td>
      <td>1.50</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda[mask1].describe().T - eda[mask2].describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>act_participation</th>
      <td>-3.0</td>
      <td>-0.569000</td>
      <td>0.091354</td>
      <td>-0.51</td>
      <td>-0.7150</td>
      <td>-0.680</td>
      <td>-0.5000</td>
      <td>-0.27</td>
    </tr>
    <tr>
      <th>act_eng</th>
      <td>-3.0</td>
      <td>3.284286</td>
      <td>1.424065</td>
      <td>1.50</td>
      <td>1.9750</td>
      <td>4.400</td>
      <td>4.3250</td>
      <td>4.40</td>
    </tr>
    <tr>
      <th>act_math</th>
      <td>-3.0</td>
      <td>3.142857</td>
      <td>1.228968</td>
      <td>1.30</td>
      <td>2.1500</td>
      <td>4.200</td>
      <td>4.0750</td>
      <td>4.10</td>
    </tr>
    <tr>
      <th>act_reading</th>
      <td>-3.0</td>
      <td>3.368571</td>
      <td>1.105362</td>
      <td>2.20</td>
      <td>1.9250</td>
      <td>4.450</td>
      <td>4.6000</td>
      <td>3.70</td>
    </tr>
    <tr>
      <th>act_sci</th>
      <td>-3.0</td>
      <td>2.611429</td>
      <td>1.132126</td>
      <td>0.60</td>
      <td>1.7750</td>
      <td>3.450</td>
      <td>3.6750</td>
      <td>3.10</td>
    </tr>
    <tr>
      <th>act_composite</th>
      <td>-3.0</td>
      <td>3.104286</td>
      <td>1.273103</td>
      <td>1.20</td>
      <td>1.9250</td>
      <td>4.200</td>
      <td>4.2250</td>
      <td>3.80</td>
    </tr>
    <tr>
      <th>sat_participation</th>
      <td>-3.0</td>
      <td>0.628429</td>
      <td>-0.016069</td>
      <td>0.59</td>
      <td>0.5950</td>
      <td>0.640</td>
      <td>0.7925</td>
      <td>0.50</td>
    </tr>
    <tr>
      <th>sat_erbw</th>
      <td>-3.0</td>
      <td>-66.871429</td>
      <td>-14.507976</td>
      <td>-48.00</td>
      <td>-41.0000</td>
      <td>-82.000</td>
      <td>-85.2500</td>
      <td>-73.00</td>
    </tr>
    <tr>
      <th>sat_math</th>
      <td>-3.0</td>
      <td>-61.714286</td>
      <td>-15.290312</td>
      <td>-49.00</td>
      <td>-35.2500</td>
      <td>-72.000</td>
      <td>-82.0000</td>
      <td>-75.00</td>
    </tr>
    <tr>
      <th>sat_total</th>
      <td>-3.0</td>
      <td>-128.742857</td>
      <td>-30.295617</td>
      <td>-97.00</td>
      <td>-75.7500</td>
      <td>-161.500</td>
      <td>-168.0000</td>
      <td>-145.00</td>
    </tr>
    <tr>
      <th>particip_dif_act_sat</th>
      <td>-3.0</td>
      <td>-1.197429</td>
      <td>0.079410</td>
      <td>-1.32</td>
      <td>-1.1900</td>
      <td>-1.310</td>
      <td>-1.0950</td>
      <td>-1.04</td>
    </tr>
    <tr>
      <th>particip_total</th>
      <td>-3.0</td>
      <td>0.059429</td>
      <td>0.002224</td>
      <td>0.11</td>
      <td>-0.0125</td>
      <td>0.115</td>
      <td>0.1850</td>
      <td>0.06</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda.groupby(by='region').agg('mean').loc[:,'act_composite']
```




    region
    Midwest      21.633333
    Northeast    24.422222
    South        20.688235
    West         20.492308
    Name: act_composite, dtype: float64




```python
region_means = [i for i in eda.groupby(by='region').agg('mean').loc[:,'act_composite']]
```


```python
exp_sample = [i for i in eda[eda['region'] == 'South']['act_composite']]
```


```python
the = [j for j in eda[eda['region'] == 'West']['act_composite']]
```


```python
the
```




    [19.8, 19.7, 22.8, 20.8, 19.0, 22.3, 20.3, 17.8, 19.7, 21.8, 20.3, 21.9, 20.2]




```python
for i in the:
    exp_sample.append(i)
```


```python
control_sample = [i for i in eda[eda['region'] == 'Northeast']['act_composite']]
```


```python
the2 = [j for j in eda[eda['region'] == 'Midwest']['act_composite']]
```


```python
for i in the2:
    control_sample.append(i)
```


```python
results = stats.ttest_ind(control_sample, exp_sample)
```


```python
results
```




    Ttest_indResult(statistic=4.578287351417986, pvalue=3.229546377554633e-05)




```python
results[1] < 0.05
```




    True




```python
print(np.mean(exp_sample))
print(np.mean(control_sample))
```

    20.60333333333333
    22.82857142857143
    


```python
np.mean(control_sample) / np.mean(exp_sample) - 1
```




    0.10800379041763941




```python
eda.groupby(by='region').describe().T[:24]
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
      <th>region</th>
      <th>Midwest</th>
      <th>Northeast</th>
      <th>South</th>
      <th>West</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="8" valign="top">act_composite</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>21.633333</td>
      <td>24.422222</td>
      <td>20.688235</td>
      <td>20.492308</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.043014</td>
      <td>0.744610</td>
      <td>1.977335</td>
      <td>1.406806</td>
    </tr>
    <tr>
      <th>min</th>
      <td>20.300000</td>
      <td>23.600000</td>
      <td>18.600000</td>
      <td>17.800000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>21.175000</td>
      <td>23.900000</td>
      <td>19.400000</td>
      <td>19.700000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>21.600000</td>
      <td>24.200000</td>
      <td>19.800000</td>
      <td>20.300000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>21.925000</td>
      <td>25.200000</td>
      <td>21.400000</td>
      <td>21.800000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>24.100000</td>
      <td>25.500000</td>
      <td>24.200000</td>
      <td>22.800000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">act_eng</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>20.925000</td>
      <td>24.311111</td>
      <td>20.182353</td>
      <td>19.576923</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.287086</td>
      <td>0.885218</td>
      <td>2.246730</td>
      <td>1.721024</td>
    </tr>
    <tr>
      <th>min</th>
      <td>19.000000</td>
      <td>23.300000</td>
      <td>17.500000</td>
      <td>16.300000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>20.250000</td>
      <td>23.800000</td>
      <td>18.900000</td>
      <td>18.600000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>20.950000</td>
      <td>24.000000</td>
      <td>19.500000</td>
      <td>19.400000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>21.200000</td>
      <td>25.400000</td>
      <td>21.000000</td>
      <td>20.900000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>24.100000</td>
      <td>25.500000</td>
      <td>24.400000</td>
      <td>22.500000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">act_math</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>21.341667</td>
      <td>24.066667</td>
      <td>20.194118</td>
      <td>20.330769</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.994035</td>
      <td>0.784219</td>
      <td>1.923366</td>
      <td>1.298322</td>
    </tr>
    <tr>
      <th>min</th>
      <td>19.900000</td>
      <td>23.100000</td>
      <td>18.100000</td>
      <td>18.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>20.775000</td>
      <td>23.400000</td>
      <td>18.800000</td>
      <td>19.800000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>21.300000</td>
      <td>24.000000</td>
      <td>19.400000</td>
      <td>19.900000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>21.525000</td>
      <td>24.600000</td>
      <td>20.900000</td>
      <td>21.500000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>23.700000</td>
      <td>25.300000</td>
      <td>23.500000</td>
      <td>22.700000</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda.groupby(by='region').describe().T[24:48]
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
      <th>region</th>
      <th>Midwest</th>
      <th>Northeast</th>
      <th>South</th>
      <th>West</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="8" valign="top">act_participation</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.778333</td>
      <td>0.248889</td>
      <td>0.734706</td>
      <td>0.708462</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.243491</td>
      <td>0.082378</td>
      <td>0.319651</td>
      <td>0.290426</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.290000</td>
      <td>0.080000</td>
      <td>0.180000</td>
      <td>0.290000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.715000</td>
      <td>0.210000</td>
      <td>0.450000</td>
      <td>0.400000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.820000</td>
      <td>0.290000</td>
      <td>1.000000</td>
      <td>0.660000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.985000</td>
      <td>0.310000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
      <td>0.340000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">act_reading</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>22.050000</td>
      <td>24.922222</td>
      <td>21.247059</td>
      <td>20.969231</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1.140574</td>
      <td>0.725909</td>
      <td>2.091088</td>
      <td>1.439551</td>
    </tr>
    <tr>
      <th>min</th>
      <td>20.500000</td>
      <td>24.100000</td>
      <td>18.800000</td>
      <td>18.100000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>21.400000</td>
      <td>24.400000</td>
      <td>19.700000</td>
      <td>20.400000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>22.100000</td>
      <td>24.700000</td>
      <td>20.500000</td>
      <td>20.800000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>22.525000</td>
      <td>25.600000</td>
      <td>22.000000</td>
      <td>22.100000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>24.500000</td>
      <td>26.000000</td>
      <td>24.900000</td>
      <td>23.100000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">act_sci</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>21.691667</td>
      <td>23.877778</td>
      <td>20.635294</td>
      <td>20.600000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.884676</td>
      <td>0.685160</td>
      <td>1.710242</td>
      <td>1.190938</td>
    </tr>
    <tr>
      <th>min</th>
      <td>20.500000</td>
      <td>23.200000</td>
      <td>18.800000</td>
      <td>18.200000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>21.200000</td>
      <td>23.300000</td>
      <td>19.400000</td>
      <td>19.900000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>21.650000</td>
      <td>23.700000</td>
      <td>19.900000</td>
      <td>20.600000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>22.025000</td>
      <td>24.600000</td>
      <td>21.300000</td>
      <td>21.700000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>23.800000</td>
      <td>24.900000</td>
      <td>23.600000</td>
      <td>22.200000</td>
    </tr>
  </tbody>
</table>
</div>




```python
eda.groupby(by='region').describe().T[64:88]
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
      <th>region</th>
      <th>Midwest</th>
      <th>Northeast</th>
      <th>South</th>
      <th>West</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="8" valign="top">sat_erbw</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>605.250000</td>
      <td>536.555556</td>
      <td>560.764706</td>
      <td>569.230769</td>
    </tr>
    <tr>
      <th>std</th>
      <td>46.411450</td>
      <td>14.748823</td>
      <td>47.968127</td>
      <td>36.088211</td>
    </tr>
    <tr>
      <th>min</th>
      <td>509.000000</td>
      <td>513.000000</td>
      <td>482.000000</td>
      <td>513.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>573.250000</td>
      <td>530.000000</td>
      <td>530.000000</td>
      <td>544.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>630.500000</td>
      <td>532.000000</td>
      <td>546.000000</td>
      <td>563.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>640.250000</td>
      <td>540.000000</td>
      <td>611.000000</td>
      <td>605.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>644.000000</td>
      <td>562.000000</td>
      <td>634.000000</td>
      <td>626.000000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">sat_math</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>599.666667</td>
      <td>526.333333</td>
      <td>542.588235</td>
      <td>557.230769</td>
    </tr>
    <tr>
      <th>std</th>
      <td>50.027871</td>
      <td>16.763055</td>
      <td>45.187192</td>
      <td>35.038440</td>
    </tr>
    <tr>
      <th>min</th>
      <td>495.000000</td>
      <td>499.000000</td>
      <td>468.000000</td>
      <td>493.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>566.500000</td>
      <td>520.000000</td>
      <td>515.000000</td>
      <td>534.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>623.000000</td>
      <td>524.000000</td>
      <td>528.000000</td>
      <td>553.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>632.000000</td>
      <td>531.000000</td>
      <td>586.000000</td>
      <td>591.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>651.000000</td>
      <td>551.000000</td>
      <td>616.000000</td>
      <td>614.000000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">sat_participation</th>
      <th>count</th>
      <td>12.000000</td>
      <td>9.000000</td>
      <td>17.000000</td>
      <td>13.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.172500</td>
      <td>0.777778</td>
      <td>0.401765</td>
      <td>0.338462</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.311773</td>
      <td>0.151144</td>
      <td>0.364353</td>
      <td>0.272576</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.020000</td>
      <td>0.600000</td>
      <td>0.020000</td>
      <td>0.030000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.030000</td>
      <td>0.670000</td>
      <td>0.050000</td>
      <td>0.110000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.030000</td>
      <td>0.710000</td>
      <td>0.490000</td>
      <td>0.300000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>0.097500</td>
      <td>0.950000</td>
      <td>0.650000</td>
      <td>0.530000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.930000</td>
    </tr>
  </tbody>
</table>
</div>



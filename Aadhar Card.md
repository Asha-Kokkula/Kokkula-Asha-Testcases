```python
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/11.abc.csv")
data
```

    C:\Users\admin\AppData\Local\Temp\ipykernel_10800\3954809446.py:2: DtypeWarning: Columns (5) have mixed types. Specify dtype option on import or set low_memory=False.
      data=pd.read_csv("C:/Users/admin/Downloads/11.abc.csv")
    




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
      <th>Registrar</th>
      <th>Enrolment Agency</th>
      <th>State</th>
      <th>District</th>
      <th>Sub District</th>
      <th>Pin Code</th>
      <th>Gender</th>
      <th>Age</th>
      <th>Aadhaar generated</th>
      <th>Enrolment Rejected</th>
      <th>Residents providing email</th>
      <th>Residents providing mobile number</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Allahabad Bank</td>
      <td>A-Onerealtors Pvt Ltd</td>
      <td>Uttar Pradesh</td>
      <td>Allahabad</td>
      <td>Meja</td>
      <td>212303</td>
      <td>F</td>
      <td>7</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Allahabad Bank</td>
      <td>Asha Security Guard Services</td>
      <td>Uttar Pradesh</td>
      <td>Sonbhadra</td>
      <td>Robertsganj</td>
      <td>231213</td>
      <td>M</td>
      <td>8</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Allahabad Bank</td>
      <td>SGS INDIA PVT LTD</td>
      <td>Uttar Pradesh</td>
      <td>Sultanpur</td>
      <td>Sultanpur</td>
      <td>227812</td>
      <td>F</td>
      <td>13</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Allahabad Bank</td>
      <td>Sri Ramraja Sarkar Lok Kalyan Trust</td>
      <td>Uttar Pradesh</td>
      <td>Shamli</td>
      <td>Shamli</td>
      <td>247775</td>
      <td>M</td>
      <td>6</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Allahabad Bank</td>
      <td>Transmoovers India</td>
      <td>Uttar Pradesh</td>
      <td>Gorakhpur</td>
      <td>Sahjanwa</td>
      <td>273001</td>
      <td>M</td>
      <td>8</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>440813</th>
      <td>Women and Child Development Govt. of Jharkhand</td>
      <td>Women and Child Development</td>
      <td>Jharkhand</td>
      <td>Palamu</td>
      <td>Patan</td>
      <td>822123</td>
      <td>M</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>440814</th>
      <td>Women and Child Development Govt. of Jharkhand</td>
      <td>Women and Child Development</td>
      <td>Jharkhand</td>
      <td>Palamu</td>
      <td>Patan</td>
      <td>822123</td>
      <td>M</td>
      <td>2</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>440815</th>
      <td>Women and Child Development Govt. of Jharkhand</td>
      <td>Women and Child Development</td>
      <td>Jharkhand</td>
      <td>Palamu</td>
      <td>Patan</td>
      <td>822123</td>
      <td>M</td>
      <td>3</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>440816</th>
      <td>Women and Child Development Govt. of Jharkhand</td>
      <td>Women and Child Development</td>
      <td>Jharkhand</td>
      <td>Palamu</td>
      <td>Patan</td>
      <td>822123</td>
      <td>M</td>
      <td>4</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>440817</th>
      <td>Women and Child Development Govt. of Jharkhand</td>
      <td>Women and Child Development</td>
      <td>Jharkhand</td>
      <td>Ranchi</td>
      <td>Ranchi</td>
      <td>834002</td>
      <td>F</td>
      <td>3</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>440818 rows × 12 columns</p>
</div>




```python
cards_apporved_by_state=data.groupby('State')['Aadhaar generated'].sum()
cards_apporved_by_state
```




    State
    Andaman and Nicobar Islands         5
    Andhra Pradesh                   5798
    Arunachal Pradesh                 913
    Assam                            3213
    Bihar                          162607
    Chandigarh                        259
    Chhattisgarh                     6604
    Dadra and Nagar Haveli            140
    Daman and Diu                     105
    Delhi                            8426
    Goa                              1167
    Gujarat                         34844
    Haryana                          6804
    Himachal Pradesh                 1547
    Jammu and Kashmir                1234
    Jharkhand                        9868
    Karnataka                       19764
    Kerala                          15143
    Lakshadweep                         4
    Madhya Pradesh                  53276
    Maharashtra                     26085
    Manipur                          1323
    Meghalaya                         277
    Mizoram                          6279
    Nagaland                          545
    Odisha                          18182
    Others                             12
    Puducherry                         83
    Punjab                           6506
    Rajasthan                       39570
    Sikkim                             50
    Tamil Nadu                      32485
    Telangana                        5018
    Tripura                           908
    Uttar Pradesh                  103767
    Uttarakhand                     13227
    West Bengal                    119901
    Name: Aadhaar generated, dtype: int64




```python
card_Enrolment_rejected_by_state=data.groupby('State')['Enrolment Rejected'].sum()
card_Enrolment_rejected_by_state
```




    State
    Andaman and Nicobar Islands       2
    Andhra Pradesh                  373
    Arunachal Pradesh                79
    Assam                            28
    Bihar                          7209
    Chandigarh                        9
    Chhattisgarh                    380
    Dadra and Nagar Haveli            3
    Daman and Diu                     2
    Delhi                           591
    Goa                             127
    Gujarat                        2500
    Haryana                         532
    Himachal Pradesh                123
    Jammu and Kashmir               204
    Jharkhand                       477
    Karnataka                      1445
    Kerala                          538
    Lakshadweep                       1
    Madhya Pradesh                 3509
    Maharashtra                    1818
    Manipur                         190
    Meghalaya                         2
    Mizoram                         185
    Nagaland                         43
    Odisha                         1596
    Others                            0
    Puducherry                       10
    Punjab                          421
    Rajasthan                      2035
    Sikkim                            2
    Tamil Nadu                     1193
    Telangana                       274
    Tripura                          62
    Uttar Pradesh                  5286
    Uttarakhand                     955
    West Bengal                    6372
    Name: Enrolment Rejected, dtype: int64




```python
cards_apporved_by_District=data.groupby('District')['Aadhaar generated'].sum()
cards_apporved_by_District
```




    District
    Adilabad         265
    Agra            2283
    Ahmadnagar       476
    Ahmedabad       4212
    Aizawl          1095
                    ... 
    Wokha             32
    Yadgir           325
    Yamuna Nagar     197
    Yavatmal         712
    Zunheboto          8
    Name: Aadhaar generated, Length: 664, dtype: int64




```python
card_Enrolment_rejected_by_District=data.groupby('District')['Enrolment Rejected'].sum()
card_Enrolment_rejected_by_District
```




    District
    Adilabad          7
    Agra            137
    Ahmadnagar       45
    Ahmedabad       278
    Aizawl          111
                   ... 
    Wokha             2
    Yadgir           28
    Yamuna Nagar     11
    Yavatmal         78
    Zunheboto         0
    Name: Enrolment Rejected, Length: 664, dtype: int64




```python
total_count=data['Gender'].value_counts()
total_count
```




    M    292798
    F    148013
    T         7
    Name: Gender, dtype: int64




```python
Age_lt_25=len(data[data['Age'] <25 ])
Age_lt_25_to_35=len(data[(data['Age'] >=25) & (data['Age'] <=35)])
Age_lt_45=len(data[data['Age'] > 45])
print("Count of records with age <25:" ,Age_lt_25)
print("Count of records with age between 25 and 35:" ,Age_lt_25_to_35)
print("Count of records with age >45:" ,Age_lt_45)

```

    Count of records with age <25: 296836
    Count of records with age between 25 and 35: 62512
    Count of records with age >45: 50610
    


```python

```


```python

```

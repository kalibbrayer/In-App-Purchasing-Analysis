

```python
import pandas as pd
import numpy as np
import os
```


```python
purchase_data = os.path.join('purchase_data.json')
purchase_data2 = os.path.join('purchase_data2.json') 
```


```python
t1 = pd.read_json('purchase_data.json')
t2 = pd.read_json('purchase_data2.json')
```


```python
pymoli_df = pd.concat([t1,t2]) 
```


```python
pymoli_df.sort_values(by=['SN'])
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Price</th>
      <th>SN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>144</th>
      <td>20</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>2.46</td>
      <td>Adairialis76</td>
    </tr>
    <tr>
      <th>308</th>
      <td>37</td>
      <td>Male</td>
      <td>79</td>
      <td>Alpha, Oath of Zeal</td>
      <td>2.88</td>
      <td>Aduephos78</td>
    </tr>
    <tr>
      <th>377</th>
      <td>37</td>
      <td>Male</td>
      <td>174</td>
      <td>Primitive Blade</td>
      <td>2.46</td>
      <td>Aduephos78</td>
    </tr>
    <tr>
      <th>431</th>
      <td>37</td>
      <td>Male</td>
      <td>92</td>
      <td>Final Critic</td>
      <td>1.36</td>
      <td>Aduephos78</td>
    </tr>
    <tr>
      <th>224</th>
      <td>26</td>
      <td>Male</td>
      <td>106</td>
      <td>Crying Steel Sickle</td>
      <td>2.29</td>
      <td>Aeduera68</td>
    </tr>
    <tr>
      <th>647</th>
      <td>26</td>
      <td>Male</td>
      <td>156</td>
      <td>Soul-Forged Steel Shortsword</td>
      <td>1.16</td>
      <td>Aeduera68</td>
    </tr>
    <tr>
      <th>721</th>
      <td>26</td>
      <td>Male</td>
      <td>39</td>
      <td>Betrayal, Whisper of Grieving Widows</td>
      <td>2.35</td>
      <td>Aeduera68</td>
    </tr>
    <tr>
      <th>394</th>
      <td>25</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>2.46</td>
      <td>Aela49</td>
    </tr>
    <tr>
      <th>4</th>
      <td>23</td>
      <td>Male</td>
      <td>63</td>
      <td>Stormfury Mace</td>
      <td>1.27</td>
      <td>Aela59</td>
    </tr>
    <tr>
      <th>0</th>
      <td>38</td>
      <td>Male</td>
      <td>165</td>
      <td>Bone Crushing Silver Skewer</td>
      <td>3.37</td>
      <td>Aelalis34</td>
    </tr>
    <tr>
      <th>529</th>
      <td>38</td>
      <td>Male</td>
      <td>172</td>
      <td>Blade of the Grave</td>
      <td>1.69</td>
      <td>Aelalis34</td>
    </tr>
    <tr>
      <th>315</th>
      <td>24</td>
      <td>Male</td>
      <td>54</td>
      <td>Eternal Cleaver</td>
      <td>3.14</td>
      <td>Aelin32</td>
    </tr>
    <tr>
      <th>359</th>
      <td>20</td>
      <td>Male</td>
      <td>32</td>
      <td>Orenmir</td>
      <td>4.95</td>
      <td>Aeliriam77</td>
    </tr>
    <tr>
      <th>637</th>
      <td>20</td>
      <td>Male</td>
      <td>18</td>
      <td>Torchlight, Bond of Storms</td>
      <td>1.77</td>
      <td>Aeliriam77</td>
    </tr>
    <tr>
      <th>341</th>
      <td>20</td>
      <td>Male</td>
      <td>9</td>
      <td>Thorn, Conqueror of the Corrupted</td>
      <td>2.04</td>
      <td>Aeliriarin93</td>
    </tr>
    <tr>
      <th>333</th>
      <td>22</td>
      <td>Male</td>
      <td>30</td>
      <td>Stormcaller</td>
      <td>4.15</td>
      <td>Aeliru63</td>
    </tr>
    <tr>
      <th>317</th>
      <td>22</td>
      <td>Male</td>
      <td>173</td>
      <td>Stormfury Longsword</td>
      <td>4.83</td>
      <td>Aeliru63</td>
    </tr>
    <tr>
      <th>503</th>
      <td>25</td>
      <td>Male</td>
      <td>125</td>
      <td>Whistling Mithril Warblade</td>
      <td>4.32</td>
      <td>Aellyria80</td>
    </tr>
    <tr>
      <th>220</th>
      <td>33</td>
      <td>Male</td>
      <td>152</td>
      <td>Darkheart</td>
      <td>3.15</td>
      <td>Aellyrialis39</td>
    </tr>
    <tr>
      <th>676</th>
      <td>25</td>
      <td>Male</td>
      <td>107</td>
      <td>Splitter, Foe Of Subtlety</td>
      <td>3.61</td>
      <td>Aellysup38</td>
    </tr>
    <tr>
      <th>233</th>
      <td>25</td>
      <td>Male</td>
      <td>129</td>
      <td>Fate, Vengeance of Eternal Justice</td>
      <td>1.55</td>
      <td>Aelollo59</td>
    </tr>
    <tr>
      <th>17</th>
      <td>22</td>
      <td>Female</td>
      <td>59</td>
      <td>Lightning, Etcher of the King</td>
      <td>1.65</td>
      <td>Aenarap34</td>
    </tr>
    <tr>
      <th>770</th>
      <td>22</td>
      <td>Male</td>
      <td>141</td>
      <td>Persuasion</td>
      <td>3.27</td>
      <td>Aenasu69</td>
    </tr>
    <tr>
      <th>41</th>
      <td>19</td>
      <td>Female</td>
      <td>124</td>
      <td>Venom Claymore</td>
      <td>2.72</td>
      <td>Aeral43</td>
    </tr>
    <tr>
      <th>705</th>
      <td>25</td>
      <td>Male</td>
      <td>115</td>
      <td>Spectral Diamond Doomblade</td>
      <td>4.25</td>
      <td>Aeral85</td>
    </tr>
    <tr>
      <th>361</th>
      <td>14</td>
      <td>Male</td>
      <td>39</td>
      <td>Betrayal, Whisper of Grieving Widows</td>
      <td>2.35</td>
      <td>Aeral97</td>
    </tr>
    <tr>
      <th>57</th>
      <td>23</td>
      <td>Female</td>
      <td>107</td>
      <td>Splitter, Foe Of Subtlety</td>
      <td>4.15</td>
      <td>Aeri79</td>
    </tr>
    <tr>
      <th>251</th>
      <td>19</td>
      <td>Female</td>
      <td>115</td>
      <td>Spectral Diamond Doomblade</td>
      <td>4.25</td>
      <td>Aeri84</td>
    </tr>
    <tr>
      <th>62</th>
      <td>19</td>
      <td>Female</td>
      <td>39</td>
      <td>Betrayal, Whisper of Grieving Widows</td>
      <td>2.35</td>
      <td>Aeri84</td>
    </tr>
    <tr>
      <th>351</th>
      <td>25</td>
      <td>Male</td>
      <td>179</td>
      <td>Wolf, Promise of the Moonwalker</td>
      <td>1.88</td>
      <td>Aerillorin70</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>752</th>
      <td>15</td>
      <td>Female</td>
      <td>116</td>
      <td>Renewed Skeletal Katana</td>
      <td>2.37</td>
      <td>Yalostiphos68</td>
    </tr>
    <tr>
      <th>478</th>
      <td>40</td>
      <td>Male</td>
      <td>168</td>
      <td>Sun Strike, Jaws of Twisted Visions</td>
      <td>2.64</td>
      <td>Yaralnura48</td>
    </tr>
    <tr>
      <th>281</th>
      <td>40</td>
      <td>Male</td>
      <td>47</td>
      <td>Alpha, Reach of Ending Hope</td>
      <td>1.55</td>
      <td>Yaralnura48</td>
    </tr>
    <tr>
      <th>34</th>
      <td>22</td>
      <td>Male</td>
      <td>47</td>
      <td>Alpha, Reach of Ending Hope</td>
      <td>1.55</td>
      <td>Yararmol43</td>
    </tr>
    <tr>
      <th>274</th>
      <td>20</td>
      <td>Male</td>
      <td>79</td>
      <td>Alpha, Oath of Zeal</td>
      <td>2.88</td>
      <td>Yarirarn35</td>
    </tr>
    <tr>
      <th>81</th>
      <td>38</td>
      <td>Male</td>
      <td>175</td>
      <td>Woeful Adamantite Claymore</td>
      <td>1.24</td>
      <td>Yaristi64</td>
    </tr>
    <tr>
      <th>14</th>
      <td>8</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>4.36</td>
      <td>Yarith71</td>
    </tr>
    <tr>
      <th>236</th>
      <td>22</td>
      <td>Male</td>
      <td>154</td>
      <td>Feral Katana</td>
      <td>2.19</td>
      <td>Yarithllodeu72</td>
    </tr>
    <tr>
      <th>382</th>
      <td>25</td>
      <td>Male</td>
      <td>39</td>
      <td>Betrayal, Whisper of Grieving Widows</td>
      <td>2.35</td>
      <td>Yarithphos28</td>
    </tr>
    <tr>
      <th>65</th>
      <td>23</td>
      <td>Male</td>
      <td>181</td>
      <td>Reaper's Toll</td>
      <td>4.12</td>
      <td>Yarithrgue83</td>
    </tr>
    <tr>
      <th>720</th>
      <td>7</td>
      <td>Male</td>
      <td>82</td>
      <td>Nirvana</td>
      <td>1.11</td>
      <td>Yarithsurgue62</td>
    </tr>
    <tr>
      <th>291</th>
      <td>7</td>
      <td>Male</td>
      <td>53</td>
      <td>Vengeance Cleaver</td>
      <td>3.70</td>
      <td>Yarithsurgue62</td>
    </tr>
    <tr>
      <th>212</th>
      <td>40</td>
      <td>Male</td>
      <td>111</td>
      <td>Misery's End</td>
      <td>2.91</td>
      <td>Yarmol79</td>
    </tr>
    <tr>
      <th>56</th>
      <td>17</td>
      <td>Male</td>
      <td>79</td>
      <td>Alpha, Oath of Zeal</td>
      <td>1.31</td>
      <td>Yarmol79</td>
    </tr>
    <tr>
      <th>297</th>
      <td>24</td>
      <td>Male</td>
      <td>84</td>
      <td>Arcane Gem</td>
      <td>2.23</td>
      <td>Yarolwen77</td>
    </tr>
    <tr>
      <th>686</th>
      <td>24</td>
      <td>Male</td>
      <td>46</td>
      <td>Hopeless Ebon Dualblade</td>
      <td>4.75</td>
      <td>Yarolwen77</td>
    </tr>
    <tr>
      <th>515</th>
      <td>40</td>
      <td>Male</td>
      <td>11</td>
      <td>Brimstone</td>
      <td>2.52</td>
      <td>Yasriphos60</td>
    </tr>
    <tr>
      <th>527</th>
      <td>40</td>
      <td>Male</td>
      <td>55</td>
      <td>Vindictive Glass Edge</td>
      <td>4.26</td>
      <td>Yasriphos60</td>
    </tr>
    <tr>
      <th>545</th>
      <td>40</td>
      <td>Male</td>
      <td>171</td>
      <td>Scalpel</td>
      <td>3.62</td>
      <td>Yasriphos60</td>
    </tr>
    <tr>
      <th>266</th>
      <td>39</td>
      <td>Female</td>
      <td>143</td>
      <td>Frenzied Scimitar</td>
      <td>2.60</td>
      <td>Yasrisu92</td>
    </tr>
    <tr>
      <th>119</th>
      <td>19</td>
      <td>Male</td>
      <td>180</td>
      <td>Stormcaller</td>
      <td>2.78</td>
      <td>Yasur35</td>
    </tr>
    <tr>
      <th>115</th>
      <td>23</td>
      <td>Male</td>
      <td>9</td>
      <td>Thorn, Conqueror of the Corrupted</td>
      <td>2.04</td>
      <td>Yasur85</td>
    </tr>
    <tr>
      <th>96</th>
      <td>22</td>
      <td>Female</td>
      <td>54</td>
      <td>Eternal Cleaver</td>
      <td>3.14</td>
      <td>Yasurra52</td>
    </tr>
    <tr>
      <th>241</th>
      <td>32</td>
      <td>Male</td>
      <td>135</td>
      <td>Warped Diamond Crusader</td>
      <td>4.66</td>
      <td>Yathecal72</td>
    </tr>
    <tr>
      <th>363</th>
      <td>32</td>
      <td>Male</td>
      <td>16</td>
      <td>Restored Bauble</td>
      <td>3.11</td>
      <td>Yathecal72</td>
    </tr>
    <tr>
      <th>580</th>
      <td>23</td>
      <td>Male</td>
      <td>178</td>
      <td>Oathbreaker, Last Hope of the Breaking Storm</td>
      <td>2.41</td>
      <td>Yathecal82</td>
    </tr>
    <tr>
      <th>437</th>
      <td>17</td>
      <td>Male</td>
      <td>82</td>
      <td>Nirvana</td>
      <td>1.11</td>
      <td>Zhisrisu83</td>
    </tr>
    <tr>
      <th>16</th>
      <td>24</td>
      <td>Male</td>
      <td>174</td>
      <td>Primitive Blade</td>
      <td>1.36</td>
      <td>Zhisrisu83</td>
    </tr>
    <tr>
      <th>376</th>
      <td>17</td>
      <td>Male</td>
      <td>33</td>
      <td>Curved Axe</td>
      <td>1.35</td>
      <td>Zhisrisu83</td>
    </tr>
    <tr>
      <th>192</th>
      <td>20</td>
      <td>Male</td>
      <td>91</td>
      <td>Celeste</td>
      <td>3.71</td>
      <td>Zontibe81</td>
    </tr>
  </tbody>
</table>
<p>858 rows × 6 columns</p>
</div>




```python
total_players = pymoli_df['SN'].nunique() 
total_players
```




    612




```python
table1 = pymoli_df.agg({'Item ID': ['nunique','count']}).rename({'nunique': 'Unique Items', 'count': 'Total Transactions'})
table1
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Unique Items</th>
      <td>184</td>
    </tr>
    <tr>
      <th>Total Transactions</th>
      <td>858</td>
    </tr>
  </tbody>
</table>
</div>




```python
table2 = pymoli_df.agg({'Price': ['mean', 'sum']}).rename({'mean': 'Average_Price', 'sum': 'Total_Revenue'})
table2 = table2.apply(lambda x: round (x,2)) 
table2
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Average_Price</th>
      <td>2.93</td>
    </tr>
    <tr>
      <th>Total_Revenue</th>
      <td>2514.43</td>
    </tr>
  </tbody>
</table>
</div>




```python
gender_demo = pymoli_df.drop_duplicates(['SN']).groupby(['Gender']).agg({'Gender': 'count'})
del gender_demo.index.name
gender_demo = gender_demo.rename(columns= {'Gender': 'Gender_Count'}) 
gender_demo['Gender_Percentage']= gender_demo['Gender_Count']/np.sum(gender_demo['Gender_Count'])*100 
gender_demo = gender_demo.apply(lambda x: round(x,2)) 
gender_demo
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender_Count</th>
      <th>Gender_Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>108</td>
      <td>17.65</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>495</td>
      <td>80.88</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>9</td>
      <td>1.47</td>
    </tr>
  </tbody>
</table>
</div>




```python
table3 = pymoli_df.groupby(['Gender']).agg({'Price': ['count', 'mean', 'sum']}).rename(columns={'count': 'Purchase_Count', 'mean': 'Average_Purchase', 'sum': 'Total_Purchases'})
table3.columns = table3.columns.droplevel()  
table3['Normalized_Totals'] = table3['Total_Purchases']/np.sum(table3['Total_Purchases'])*100
table3 = round(table3, 2)
table3 
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase_Count</th>
      <th>Average_Purchase</th>
      <th>Total_Purchases</th>
      <th>Normalized_Totals</th>
    </tr>
    <tr>
      <th>Gender</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>149</td>
      <td>2.85</td>
      <td>424.29</td>
      <td>16.87</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>697</td>
      <td>2.94</td>
      <td>2052.28</td>
      <td>81.62</td>
    </tr>
    <tr>
      <th>Other / Non-Disclosed</th>
      <td>12</td>
      <td>3.15</td>
      <td>37.86</td>
      <td>1.51</td>
    </tr>
  </tbody>
</table>
</div>




```python
bins = [4, 8, 12, 16, 20, 24, 28, 32, 36, 40, 44, 48]
```


```python
pymoli_df["Age_Demographics"] = pd.cut(pymoli_df["Age"], bins)
age_demo_table = pymoli_df.groupby(["Age_Demographics"]).agg({'Price': ['count', 'mean', 'sum']}).rename(columns={'count': 'Purchase_Count', 'mean': 'Average_Purchases', 'sum': 'Total_Purchases'})
age_demo_table.columns = age_demo_table.columns.droplevel(0) 
age_demo_table['Normalized_Totals'] = age_demo_table['Total_Purchases']/np.sum(age_demo_table['Total_Purchases'])*100
age_demo_table = round(age_demo_table, 2)
age_demo_table
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase_Count</th>
      <th>Average_Purchases</th>
      <th>Total_Purchases</th>
      <th>Normalized_Totals</th>
    </tr>
    <tr>
      <th>Age_Demographics</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>(4, 8]</th>
      <td>26</td>
      <td>2.72</td>
      <td>70.63</td>
      <td>2.81</td>
    </tr>
    <tr>
      <th>(8, 12]</th>
      <td>28</td>
      <td>3.38</td>
      <td>94.74</td>
      <td>3.77</td>
    </tr>
    <tr>
      <th>(12, 16]</th>
      <td>91</td>
      <td>2.75</td>
      <td>250.38</td>
      <td>9.96</td>
    </tr>
    <tr>
      <th>(16, 20]</th>
      <td>178</td>
      <td>2.89</td>
      <td>514.48</td>
      <td>20.46</td>
    </tr>
    <tr>
      <th>(20, 24]</th>
      <td>264</td>
      <td>2.94</td>
      <td>777.45</td>
      <td>30.92</td>
    </tr>
    <tr>
      <th>(24, 28]</th>
      <td>113</td>
      <td>2.97</td>
      <td>335.48</td>
      <td>13.34</td>
    </tr>
    <tr>
      <th>(28, 32]</th>
      <td>70</td>
      <td>3.00</td>
      <td>210.06</td>
      <td>8.35</td>
    </tr>
    <tr>
      <th>(32, 36]</th>
      <td>45</td>
      <td>2.97</td>
      <td>133.76</td>
      <td>5.32</td>
    </tr>
    <tr>
      <th>(36, 40]</th>
      <td>40</td>
      <td>2.97</td>
      <td>118.81</td>
      <td>4.73</td>
    </tr>
    <tr>
      <th>(40, 44]</th>
      <td>2</td>
      <td>2.96</td>
      <td>5.92</td>
      <td>0.24</td>
    </tr>
    <tr>
      <th>(44, 48]</th>
      <td>1</td>
      <td>2.72</td>
      <td>2.72</td>
      <td>0.11</td>
    </tr>
  </tbody>
</table>
</div>




```python
top_spenders = pymoli_df.groupby(["SN"]).agg({'Price': ['count', 'mean', 'sum']}).rename(columns={'count': 'Purchase_Count', 'mean': 'Average_Purchases', 'sum': 'Total_Purchases'})
top_spenders.columns = top_spenders.columns.droplevel(0)
top_5_spenders = top_spenders.nlargest(5, 'Total_Purchases')
top_5_spenders.index.name= "Top_5_Spenders"
top_5_spenders
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Purchase_Count</th>
      <th>Average_Purchases</th>
      <th>Total_Purchases</th>
    </tr>
    <tr>
      <th>Top_5_Spenders</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Undirrala66</th>
      <td>5</td>
      <td>3.412</td>
      <td>17.06</td>
    </tr>
    <tr>
      <th>Aerithllora36</th>
      <td>4</td>
      <td>3.775</td>
      <td>15.10</td>
    </tr>
    <tr>
      <th>Saedue76</th>
      <td>4</td>
      <td>3.390</td>
      <td>13.56</td>
    </tr>
    <tr>
      <th>Sondim43</th>
      <td>4</td>
      <td>3.255</td>
      <td>13.02</td>
    </tr>
    <tr>
      <th>Mindimnya67</th>
      <td>4</td>
      <td>3.185</td>
      <td>12.74</td>
    </tr>
  </tbody>
</table>
</div>




```python
most_popular_items = pymoli_df.groupby(["Item ID", "Item Name"]).agg({'Price': ['mean', 'count', 'sum']}).rename(columns={'mean': 'Average_Purchase_Price', 'count': 'Purchase_Count', 'sum': 'Total_Purchase_Value'})
most_popular_items.columns = most_popular_items.columns.droplevel(0)
most_popular_items = most_popular_items.nlargest(5, 'Purchase_Count')
most_popular_items
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Average_Purchase_Price</th>
      <th>Purchase_Count</th>
      <th>Total_Purchase_Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th>Item Name</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>84</th>
      <th>Arcane Gem</th>
      <td>2.445</td>
      <td>12</td>
      <td>29.34</td>
    </tr>
    <tr>
      <th>39</th>
      <th>Betrayal, Whisper of Grieving Widows</th>
      <td>2.350</td>
      <td>11</td>
      <td>25.85</td>
    </tr>
    <tr>
      <th>31</th>
      <th>Trickster</th>
      <td>2.322</td>
      <td>10</td>
      <td>23.22</td>
    </tr>
    <tr>
      <th>13</th>
      <th>Serenity</th>
      <td>1.490</td>
      <td>9</td>
      <td>13.41</td>
    </tr>
    <tr>
      <th>34</th>
      <th>Retribution Axe</th>
      <td>4.140</td>
      <td>9</td>
      <td>37.26</td>
    </tr>
  </tbody>
</table>
</div>




```python
most_profitable_items = pymoli_df.groupby(["Item ID", "Item Name"]).agg({'Price': ['mean', 'count', 'sum']}).rename(columns={'mean': 'Average_Purchase_Price', 'count': 'Purchase_Count', 'sum': 'Total_Purchase_Value'})
most_profitable_items.columns = most_profitable_items.columns.droplevel(0)
most_profitable_items = most_profitable_items.nlargest(5, 'Total_Purchase_Value')
most_profitable_items
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Average_Purchase_Price</th>
      <th>Purchase_Count</th>
      <th>Total_Purchase_Value</th>
    </tr>
    <tr>
      <th>Item ID</th>
      <th>Item Name</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>34</th>
      <th>Retribution Axe</th>
      <td>4.140</td>
      <td>9</td>
      <td>37.26</td>
    </tr>
    <tr>
      <th>107</th>
      <th>Splitter, Foe Of Subtlety</th>
      <td>3.670</td>
      <td>9</td>
      <td>33.03</td>
    </tr>
    <tr>
      <th>115</th>
      <th>Spectral Diamond Doomblade</th>
      <td>4.250</td>
      <td>7</td>
      <td>29.75</td>
    </tr>
    <tr>
      <th>32</th>
      <th>Orenmir</th>
      <td>4.950</td>
      <td>6</td>
      <td>29.70</td>
    </tr>
    <tr>
      <th>84</th>
      <th>Arcane Gem</th>
      <td>2.445</td>
      <td>12</td>
      <td>29.34</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
# Pandas-HW-4-

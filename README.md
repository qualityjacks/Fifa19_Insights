# FIFA 19 Insights Using Pandas In Python
<img src="https://camo.githubusercontent.com/5e1e40bde51a836bec3ce9c7493e453f64ac1f1b/687474703a2f2f696e63682d63692e6f72672f6769746875622f6477796c2f686170692d617574682d6a7774322e7376673f6272616e63683d6d6173746572" alt="Inline docs" data-canonical-src="http://inch-ci.org/github/dwyl/hapi-auth-jwt2.svg?branch=master" style="max-width:100%;"> <a href="http://badges.mit-license.org" rel="nofollow"><img src="https://camo.githubusercontent.com/107590fac8cbd65071396bb4d04040f76cde5bde/687474703a2f2f696d672e736869656c64732e696f2f3a6c6963656e73652d6d69742d626c75652e7376673f7374796c653d666c61742d737175617265" alt="License" data-canonical-src="http://img.shields.io/:license-mit-blue.svg?style=flat-square" style="max-width:100%;"></a> <img src="https://camo.githubusercontent.com/cfcaf3a99103d61f387761e5fc445d9ba0203b01/68747470733a2f2f7472617669732d63692e6f72672f6477796c2f657374612e7376673f6272616e63683d6d6173746572" alt="Build Status" data-canonical-src="https://travis-ci.org/dwyl/esta.svg?branch=master" style="max-width:100%;"> <img src="https://camo.githubusercontent.com/facfcb6afd684d2c9701c7d6add65f391fdf86fc/68747470733a2f2f696d672e736869656c64732e696f2f636f6465636f762f632f6769746875622f6477796c2f686170692d617574682d6a7774322e7376673f6d61784167653d32353932303030" alt="codecov.io Code Coverage" data-canonical-src="https://img.shields.io/codecov/c/github/dwyl/hapi-auth-jwt2.svg?maxAge=2592000" style="max-width:100%;">

## Installation
* Download the latest version of [Python](https://www.python.org/downloads/) (3.7) and install it on your system
* Download [Anaconda Distribution](https://www.anaconda.com/download/) for Python 3.7 and install it on your system
* Run "Anaconda Prompt" and type "jupyter notebook" in the command prompt

## Documentation 
Importing the Pandas and Matplotlib Library
```python
import pandas as pd
import matplotlib.pyplot as plt
```
Reading the [Dataset](https://www.kaggle.com/karangadiya/fifa19) into a DataFrame
```python
filename = 'data.csv'
data_raw = pd.read_csv(filename)
```
Print the imported data
```python
data_raw
```
Get First 10 rows
```python
data_raw.head(10)
```
<div class="output_subarea output_html rendered_html output_result"><div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>ID</th>
      <th>Name</th>
      <th>Age</th>
      <th>Photo</th>
      <th>Nationality</th>
      <th>Flag</th>
      <th>Overall</th>
      <th>Potential</th>
      <th>Club</th>
      <th>...</th>
      <th>Composure</th>
      <th>Marking</th>
      <th>StandingTackle</th>
      <th>SlidingTackle</th>
      <th>GKDiving</th>
      <th>GKHandling</th>
      <th>GKKicking</th>
      <th>GKPositioning</th>
      <th>GKReflexes</th>
      <th>Release Clause</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>158023</td>
      <td>L. Messi</td>
      <td>31</td>
      <td>https://cdn.sofifa.org/players/4/19/158023.png</td>
      <td>Argentina</td>
      <td>https://cdn.sofifa.org/flags/52.png</td>
      <td>94</td>
      <td>94</td>
      <td>FC Barcelona</td>
      <td>...</td>
      <td>96.0</td>
      <td>33.0</td>
      <td>28.0</td>
      <td>26.0</td>
      <td>6.0</td>
      <td>11.0</td>
      <td>15.0</td>
      <td>14.0</td>
      <td>8.0</td>
      <td>€226.5M</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>20801</td>
      <td>Cristiano Ronaldo</td>
      <td>33</td>
      <td>https://cdn.sofifa.org/players/4/19/20801.png</td>
      <td>Portugal</td>
      <td>https://cdn.sofifa.org/flags/38.png</td>
      <td>94</td>
      <td>94</td>
      <td>Juventus</td>
      <td>...</td>
      <td>95.0</td>
      <td>28.0</td>
      <td>31.0</td>
      <td>23.0</td>
      <td>7.0</td>
      <td>11.0</td>
      <td>15.0</td>
      <td>14.0</td>
      <td>11.0</td>
      <td>€127.1M</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>190871</td>
      <td>Neymar Jr</td>
      <td>26</td>
      <td>https://cdn.sofifa.org/players/4/19/190871.png</td>
      <td>Brazil</td>
      <td>https://cdn.sofifa.org/flags/54.png</td>
      <td>92</td>
      <td>93</td>
      <td>Paris Saint-Germain</td>
      <td>...</td>
      <td>94.0</td>
      <td>27.0</td>
      <td>24.0</td>
      <td>33.0</td>
      <td>9.0</td>
      <td>9.0</td>
      <td>15.0</td>
      <td>15.0</td>
      <td>11.0</td>
      <td>€228.1M</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>193080</td>
      <td>De Gea</td>
      <td>27</td>
      <td>https://cdn.sofifa.org/players/4/19/193080.png</td>
      <td>Spain</td>
      <td>https://cdn.sofifa.org/flags/45.png</td>
      <td>91</td>
      <td>93</td>
      <td>Manchester United</td>
      <td>...</td>
      <td>68.0</td>
      <td>15.0</td>
      <td>21.0</td>
      <td>13.0</td>
      <td>90.0</td>
      <td>85.0</td>
      <td>87.0</td>
      <td>88.0</td>
      <td>94.0</td>
      <td>€138.6M</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>192985</td>
      <td>K. De Bruyne</td>
      <td>27</td>
      <td>https://cdn.sofifa.org/players/4/19/192985.png</td>
      <td>Belgium</td>
      <td>https://cdn.sofifa.org/flags/7.png</td>
      <td>91</td>
      <td>92</td>
      <td>Manchester City</td>
      <td>...</td>
      <td>88.0</td>
      <td>68.0</td>
      <td>58.0</td>
      <td>51.0</td>
      <td>15.0</td>
      <td>13.0</td>
      <td>5.0</td>
      <td>10.0</td>
      <td>13.0</td>
      <td>€196.4M</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>183277</td>
      <td>E. Hazard</td>
      <td>27</td>
      <td>https://cdn.sofifa.org/players/4/19/183277.png</td>
      <td>Belgium</td>
      <td>https://cdn.sofifa.org/flags/7.png</td>
      <td>91</td>
      <td>91</td>
      <td>Chelsea</td>
      <td>...</td>
      <td>91.0</td>
      <td>34.0</td>
      <td>27.0</td>
      <td>22.0</td>
      <td>11.0</td>
      <td>12.0</td>
      <td>6.0</td>
      <td>8.0</td>
      <td>8.0</td>
      <td>€172.1M</td>
    </tr>
    <tr>
      <th>6</th>
      <td>6</td>
      <td>177003</td>
      <td>L. Modrić</td>
      <td>32</td>
      <td>https://cdn.sofifa.org/players/4/19/177003.png</td>
      <td>Croatia</td>
      <td>https://cdn.sofifa.org/flags/10.png</td>
      <td>91</td>
      <td>91</td>
      <td>Real Madrid</td>
      <td>...</td>
      <td>84.0</td>
      <td>60.0</td>
      <td>76.0</td>
      <td>73.0</td>
      <td>13.0</td>
      <td>9.0</td>
      <td>7.0</td>
      <td>14.0</td>
      <td>9.0</td>
      <td>€137.4M</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>176580</td>
      <td>L. Suárez</td>
      <td>31</td>
      <td>https://cdn.sofifa.org/players/4/19/176580.png</td>
      <td>Uruguay</td>
      <td>https://cdn.sofifa.org/flags/60.png</td>
      <td>91</td>
      <td>91</td>
      <td>FC Barcelona</td>
      <td>...</td>
      <td>85.0</td>
      <td>62.0</td>
      <td>45.0</td>
      <td>38.0</td>
      <td>27.0</td>
      <td>25.0</td>
      <td>31.0</td>
      <td>33.0</td>
      <td>37.0</td>
      <td>€164M</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8</td>
      <td>155862</td>
      <td>Sergio Ramos</td>
      <td>32</td>
      <td>https://cdn.sofifa.org/players/4/19/155862.png</td>
      <td>Spain</td>
      <td>https://cdn.sofifa.org/flags/45.png</td>
      <td>91</td>
      <td>91</td>
      <td>Real Madrid</td>
      <td>...</td>
      <td>82.0</td>
      <td>87.0</td>
      <td>92.0</td>
      <td>91.0</td>
      <td>11.0</td>
      <td>8.0</td>
      <td>9.0</td>
      <td>7.0</td>
      <td>11.0</td>
      <td>€104.6M</td>
    </tr>
    <tr>
      <th>9</th>
      <td>9</td>
      <td>200389</td>
      <td>J. Oblak</td>
      <td>25</td>
      <td>https://cdn.sofifa.org/players/4/19/200389.png</td>
      <td>Slovenia</td>
      <td>https://cdn.sofifa.org/flags/44.png</td>
      <td>90</td>
      <td>93</td>
      <td>Atlético Madrid</td>
      <td>...</td>
      <td>70.0</td>
      <td>27.0</td>
      <td>12.0</td>
      <td>18.0</td>
      <td>86.0</td>
      <td>92.0</td>
      <td>78.0</td>
      <td>88.0</td>
      <td>89.0</td>
      <td>€144.5M</td>
    </tr>
  </tbody>
</table>
<p>10 rows × 89 columns</p>
</div></div>

Check out the columns data
```python
data_raw.columns
```
<div class="output_subarea output_text output_result"><pre>Index(['Unnamed: 0', 'ID', 'Name', 'Age', 'Photo', 'Nationality', 'Flag',
       'Overall', 'Potential', 'Club', 'Club Logo', 'Value', 'Wage', 'Special',
       'Preferred Foot', 'International Reputation', 'Weak Foot',
       'Skill Moves', 'Work Rate', 'Body Type', 'Real Face', 'Position',
       'Jersey Number', 'Joined', 'Loaned From', 'Contract Valid Until',
       'Height', 'Weight', 'LS', 'ST', 'RS', 'LW', 'LF', 'CF', 'RF', 'RW',
       'LAM', 'CAM', 'RAM', 'LM', 'LCM', 'CM', 'RCM', 'RM', 'LWB', 'LDM',
       'CDM', 'RDM', 'RWB', 'LB', 'LCB', 'CB', 'RCB', 'RB', 'Crossing',
       'Finishing', 'HeadingAccuracy', 'ShortPassing', 'Volleys', 'Dribbling',
       'Curve', 'FKAccuracy', 'LongPassing', 'BallControl', 'Acceleration',
       'SprintSpeed', 'Agility', 'Reactions', 'Balance', 'ShotPower',
       'Jumping', 'Stamina', 'Strength', 'LongShots', 'Aggression',
       'Interceptions', 'Positioning', 'Vision', 'Penalties', 'Composure',
       'Marking', 'StandingTackle', 'SlidingTackle', 'GKDiving', 'GKHandling',
       'GKKicking', 'GKPositioning', 'GKReflexes', 'Release Clause'],
      dtype='object')</pre></div>
      
Basic Information about columns (datatype, count etc)
```python
data_raw.info()
```

<div class="output_subarea output_text output_stream output_stdout"><pre>&lt;class 'pandas.core.frame.DataFrame'&gt;
RangeIndex: 18207 entries, 0 to 18206
Data columns (total 89 columns):
Unnamed: 0                  18207 non-null int64
ID                          18207 non-null int64
Name                        18207 non-null object
Age                         18207 non-null int64
Photo                       18207 non-null object
Nationality                 18207 non-null object
Flag                        18207 non-null object
Overall                     18207 non-null int64
Potential                   18207 non-null int64
Club                        17966 non-null object
Club Logo                   18207 non-null object
Value                       18207 non-null object
Wage                        18207 non-null object
Special                     18207 non-null int64
Preferred Foot              18159 non-null object
International Reputation    18159 non-null float64
Weak Foot                   18159 non-null float64
Skill Moves                 18159 non-null float64
Work Rate                   18159 non-null object
Body Type                   18159 non-null object
Real Face                   18159 non-null object
Position                    18147 non-null object
Jersey Number               18147 non-null float64
Joined                      16654 non-null object
Loaned From                 1264 non-null object
Contract Valid Until        17918 non-null object
Height                      18159 non-null object
Weight                      18159 non-null object
LS                          16122 non-null object
ST                          16122 non-null object
RS                          16122 non-null object
LW                          16122 non-null object
LF                          16122 non-null object
CF                          16122 non-null object
RF                          16122 non-null object
RW                          16122 non-null object
LAM                         16122 non-null object
CAM                         16122 non-null object
RAM                         16122 non-null object
LM                          16122 non-null object
LCM                         16122 non-null object
CM                          16122 non-null object
RCM                         16122 non-null object
RM                          16122 non-null object
LWB                         16122 non-null object
LDM                         16122 non-null object
CDM                         16122 non-null object
RDM                         16122 non-null object
RWB                         16122 non-null object
LB                          16122 non-null object
LCB                         16122 non-null object
CB                          16122 non-null object
RCB                         16122 non-null object
RB                          16122 non-null object
Crossing                    18159 non-null float64
Finishing                   18159 non-null float64
HeadingAccuracy             18159 non-null float64
ShortPassing                18159 non-null float64
Volleys                     18159 non-null float64
Dribbling                   18159 non-null float64
Curve                       18159 non-null float64
FKAccuracy                  18159 non-null float64
LongPassing                 18159 non-null float64
BallControl                 18159 non-null float64
Acceleration                18159 non-null float64
SprintSpeed                 18159 non-null float64
Agility                     18159 non-null float64
Reactions                   18159 non-null float64
Balance                     18159 non-null float64
ShotPower                   18159 non-null float64
Jumping                     18159 non-null float64
Stamina                     18159 non-null float64
Strength                    18159 non-null float64
LongShots                   18159 non-null float64
Aggression                  18159 non-null float64
Interceptions               18159 non-null float64
Positioning                 18159 non-null float64
Vision                      18159 non-null float64
Penalties                   18159 non-null float64
Composure                   18159 non-null float64
Marking                     18159 non-null float64
StandingTackle              18159 non-null float64
SlidingTackle               18159 non-null float64
GKDiving                    18159 non-null float64
GKHandling                  18159 non-null float64
GKKicking                   18159 non-null float64
GKPositioning               18159 non-null float64
GKReflexes                  18159 non-null float64
Release Clause              16643 non-null object
dtypes: float64(38), int64(6), object(45)
memory usage: 12.4+ MB
</pre></div>

Check out the shape of DataFrame object
```python
data_raw.shape
```

<div class="output_subarea output_text output_result"><pre>(18207, 89)</pre></div>

Check if there are null values in the DataFrame
```python
data_raw.isnull().any().any() # If true is returned --> there are null values in the DataFrame
```

<div class="output_subarea output_text output_result"><pre>True</pre></div>

Get the columns having null values
```python
data_raw.isnull().any()
```

<div class="output_subarea output_text output_result"><pre>Unnamed: 0                  False
ID                          False
Name                        False
Age                         False
Photo                       False
Nationality                 False
Flag                        False
Overall                     False
Potential                   False
Club                         True
Club Logo                   False
Value                       False
Wage                        False
Special                     False
Preferred Foot               True
International Reputation     True
Weak Foot                    True
Skill Moves                  True
Work Rate                    True
Body Type                    True
Real Face                    True
Position                     True
Jersey Number                True
Joined                       True
Loaned From                  True
Contract Valid Until         True
Height                       True
Weight                       True
LS                           True
ST                           True
                            ...  
Dribbling                    True
Curve                        True
FKAccuracy                   True
LongPassing                  True
BallControl                  True
Acceleration                 True
SprintSpeed                  True
Agility                      True
Reactions                    True
Balance                      True
ShotPower                    True
Jumping                      True
Stamina                      True
Strength                     True
LongShots                    True
Aggression                   True
Interceptions                True
Positioning                  True
Vision                       True
Penalties                    True
Composure                    True
Marking                      True
StandingTackle               True
SlidingTackle                True
GKDiving                     True
GKHandling                   True
GKKicking                    True
GKPositioning                True
GKReflexes                   True
Release Clause               True
Length: 89, dtype: bool</pre></div>

Get the total number of null values
```python
data_raw.isnull().sum().sum()
```

<div class="output_subarea output_text output_result"><pre>76984</pre></div>

Get the number of null values for each of the columns
```python
data_raw.isnull().sum()
```

<div class="output_subarea output_text output_result"><pre>Unnamed: 0                      0
ID                              0
Name                            0
Age                             0
Photo                           0
Nationality                     0
Flag                            0
Overall                         0
Potential                       0
Club                          241
Club Logo                       0
Value                           0
Wage                            0
Special                         0
Preferred Foot                 48
International Reputation       48
Weak Foot                      48
Skill Moves                    48
Work Rate                      48
Body Type                      48
Real Face                      48
Position                       60
Jersey Number                  60
Joined                       1553
Loaned From                 16943
Contract Valid Until          289
Height                         48
Weight                         48
LS                           2085
ST                           2085
                            ...  
Dribbling                      48
Curve                          48
FKAccuracy                     48
LongPassing                    48
BallControl                    48
Acceleration                   48
SprintSpeed                    48
Agility                        48
Reactions                      48
Balance                        48
ShotPower                      48
Jumping                        48
Stamina                        48
Strength                       48
LongShots                      48
Aggression                     48
Interceptions                  48
Positioning                    48
Vision                         48
Penalties                      48
Composure                      48
Marking                        48
StandingTackle                 48
SlidingTackle                  48
GKDiving                       48
GKHandling                     48
GKKicking                      48
GKPositioning                  48
GKReflexes                     48
Release Clause               1564
Length: 89, dtype: int64</pre></div>

## Contributing
Fork it (https://github.com/qualityjacks/Fifa19_Insights/fork)<br>
Create your feature branch
```python
git checkout -b feature
```
Commit your changes
```python
git commit -m 'some-text'
```
Push to the branch
```python
git push origin feature
```
Create a new Pull Request

## Resources
[Awesome Data Science](https://github.com/bulutyazilim/awesome-datascience) <a href="https://github.com/sindresorhus/awesome"><img src="https://camo.githubusercontent.com/13c4e50d88df7178ae1882a203ed57b641674f94/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667" alt="Awesome" data-canonical-src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" style="max-width:100%;"></a><br>[Fifa 19 Dataset](https://www.kaggle.com/karangadiya/fifa19)

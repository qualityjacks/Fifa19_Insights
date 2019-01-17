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
Basic Information about columns (datatype, count etc)
```python
data_raw.info()
```
Check out the shape of DataFrame object
```python
data_raw.shape
```
Check if there are null values in the DataFrame
```python
data_raw.isnull().any().any() # If true is returned --> there are null values in the DataFrame
```
Get the columns having null values
```python
data_raw.isnull().any()
```
Get the total number of null values
```python
data_raw.isnull().sum().sum()
```
Get the number of null values for each of the columns
```python
data_raw.isnull().sum()
```

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

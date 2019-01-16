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
[Awesome Data Science](https://github.com/bulutyazilim/awesome-datascience) <a href="https://github.com/sindresorhus/awesome"><img src="https://camo.githubusercontent.com/13c4e50d88df7178ae1882a203ed57b641674f94/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667" alt="Awesome" data-canonical-src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" style="max-width:100%;"></a>

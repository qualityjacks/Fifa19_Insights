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


## Contributing
Fork it (https://github.com/qualityjacks/Fifa19_Insights/fork)<br>
Create your feature branch
```python
git checkout -b feature
```
<br>Commit your changes
```python
  git commit -m 'some-text'
```
<br>Push to the branch
```python
git push origin feature
```
<br>Create a new Pull Request

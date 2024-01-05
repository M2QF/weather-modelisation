# Weather modelisation
Machine learning project that aims to model weather conditions in Paris.

## Context

The goal of this project is to study 
the temporal evolution of temperature and wind in France, across one year.

## Required packages
- `pandas` : to manipulate dataframes.
- `numpy` : to manipulate arrays.
- `matplotlib` : to plot graphs.
- `cartopy` : to plot maps.
- `IPython` : to display dataframes in Jupyter Notebook.
- `scikit-learn` : to perform machine learning tasks.
- Other packages that are available by default in any Python distribution (`datetime`...).

## Data
Data are provided through 3 files, localted in the `data` folder:
- `dataGPS.csv` : contains the GPS coordinates of the cities.
- `dataTemp.csv` : contains the temperature data.
- `dataWind.csv` : contains the wind data.

All of them share a common ID, that can be used to merge them into a single dataframe.

Below are the first rows of each dataframe, after removing the ID prefix in each column to have better readability.
### GPS data
|   ID |   Lattitude |   Longitude |
|-----:|------------:|------------:|
| 3426 |         2.5 |        51   |
| 3510 |         2   |        50.5 |
| 3511 |         2.5 |        50.5 |
| 3512 |         3   |        50.5 |
| 3513 |         3.5 |        50.5 |
### Temperature data
|   ID |   01-01 00:00:00 |   01-01 01:00:00 |   01-01 02:00:00 |   01-01 03:00:00 |   01-01 04:00:00 |
|-----:|----------------------:|----------------------:|----------------------:|----------------------:|----------------------:|
| 3426 |                   1.5 |                   2.2 |                   2.8 |                   3.5 |                   4.1 |
| 3510 |                   0.8 |                   1.8 |                   2.9 |                   3.9 |                   4.3 |
| 3511 |                   1   |                   1.6 |                   2.4 |                   3.1 |                   3.5 |
| 3512 |                   1.4 |                   1.9 |                   2.4 |                   2.9 |                   3.4 |
| 3513 |                   1.4 |                   1.8 |                   2.3 |                   2.7 |                   3.1 |
### Wind data
|   ID |   01-01 00:00:00 |   01-01 01:00:00 |   01-01 02:00:00 |   01-01 03:00:00 |   01-01 04:00:00 |
|-----:|----------------------:|----------------------:|----------------------:|----------------------:|----------------------:|
| 3426 |               17.1607 |               17.2627 |               17.3666 |               17.5034 |               17.0188 |
| 3510 |               18.2784 |               18.1728 |               18.2395 |               18.3    |               17.818  |
| 3511 |               17.0658 |               17.0426 |               17.1657 |               17.2142 |               16.8003 |
| 3512 |               16.1409 |               16.1276 |               16.2364 |               16.2693 |               15.9154 |
| 3513 |               16.4551 |               16.5387 |               16.646  |               16.7765 |               16.4247 |
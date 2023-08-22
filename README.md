# EXP-2--Implementation-of-time-series-analysis-and-decomposition
## AIM:
Illustrates how to perform time series analysis and decomposition on the monthly average
temperature of a city/country and for airline passengers.
## ALGORITHM:

1. Import the required packages like pandas and numpy

2. Read the data using the pandas

3. Perform the decomposition process for the required data.

4. Plot the data according to need, either seasonal_decomposition or trend plot.

5. Display the overall results.
## PROGRAM:
```
import pandas as pd
import numpy as np
from statsmodels.tsa.seasonal import seasonal_decompose
df=pd.read_csv('AirPassengers.csv')
df.head()
df.set_index('Month',inplace=True)
df.index=pd.to_datetime(df.index)
df.dropna(inplace=True)
df.plot()
result=seasonal_decompose(df['#Passengers'], model='multiplicable',period=12)
result.seasonal.plot()
result.trend.plot()
result.plot()

```
## OUTPUT:
## FIRST FIVE ROWS:
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/f551bfff-dca1-45fe-b927-763ed6bf8b0e)

## PLOTTING THE DATA:
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/51a16859-c920-42f1-aa53-28bb97411a8b)

## SEASONAL PLOT REPRESENTATION :
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/0a0a618b-6bbe-4dba-a7d3-ac0b699dce14)

## TREND PLOT REPRESENTATION :
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/a441bdb8-0877-43fd-85b5-ab2d701bb4aa)

## OVERAL REPRESENTATION:
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/364b8e2e-390b-4481-bd83-8dbd4696a03c)
![image](https://github.com/swethamohanraj/plementation-of-time-series-analysis-and-decomposition/assets/94228215/f62d2d61-a207-4cd7-8d9c-4716291dfa7f)

## RESULT:
Thus we have created the python code for the time series analysis and decomposition.

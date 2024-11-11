# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 09:8:24

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
### Developed by:Ajmera Hanumantha Rao
### Reference Number:212222240016
## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```
## MARKET PRICE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## TEMPERATURE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```








# OUTPUT:
## Population

![1 1](https://github.com/Hanumanth26/TSA_EXP1/assets/121033192/a091f768-9238-47d6-a693-a6a9881b49f9)

## Stock price
![1 2](https://github.com/Hanumanth26/TSA_EXP1/assets/121033192/4a775f9c-086a-450f-9179-62dc72727997)
![1 3](https://github.com/Hanumanth26/TSA_EXP1/assets/121033192/914a84fb-1eb0-4732-bb2f-a197e0ddf3a4)


## Temperature
![1 4](https://github.com/Hanumanth26/TSA_EXP1/assets/121033192/aa627a4a-afa2-44d0-90e5-14b3acf01d13)


# RESULT:
Thus we have created the python code for plotting the time series of given data.

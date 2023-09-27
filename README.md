# EX-2 Time series analysis and decomposition on the monthly average temperature of a city/country.

## AIM:
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country.

## Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook.

## Procedure:
1 Import the numpy and matplotlib.pyplot modules.
2 Read the dataset using pandas
3 plot the data using matplotlib.pyplot library function
4 Plot the data according to need, either seasonal_decomposition or trend plot.
5 Display the overall results.

## Program:
```
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country 
Developed by: GOKUL VIJAYA RAMANUJA P
RegisterNumber:  212222240030
*/
import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose
data =pd.read_csv("/content/temperatures.csv",parse_dates=["YEAR"])
data.head()

data.set_index("YEAR",inplace=True)
data.index=pd.to_datetime(data.index)

data.dropna(inplace=True)
data.plot()

result=seasonal_decompose(data["ANNUAL"],model="multiplicable",period=12)

result.seasonal.plot()

result.trend.plot()

result.plot()
```
## Output:

### data.head()

![261831938-9611d5be-5ea5-4ddd-be74-dbcd7a4a7dbc](https://github.com/gokulvijayaramanuja/time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/119577543/e8120c8d-c632-43e2-8ca0-cf87351ad6a0)

### data.plot()
![261831905-5bcf5dc7-53d1-4cb6-b010-22e9940c62d3](https://github.com/gokulvijayaramanuja/time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/119577543/4f22dc88-a35b-4e45-ace1-1dfe88bc3900)


### result.seasonal.plot()
![261831908-a15d8391-c63f-4d81-a84b-78de8fa21f39](https://github.com/gokulvijayaramanuja/time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/119577543/a357c1bf-0a85-41e9-b407-bf8e0e4ea988)


### result.trend.plot()
![261831914-7cd52086-4702-425e-95a9-5fe48a01f57b](https://github.com/gokulvijayaramanuja/time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/119577543/0e727e6a-369d-4f9d-bda5-7440406f634e)


### result.plot()
![261831917-855e6de5-a200-4b67-ab72-c1bff2bda08a](https://github.com/gokulvijayaramanuja/time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city-country/assets/119577543/6cbdc841-7620-48cc-a399-fb179935d886)


## Result:
Thus the program to time series analysis and decomposition on the monthly average temperature of a city/country is written and verified using python programming.

# Day 1
## Prediction
```python
import pandas as pd
from sklearn.tree import DecisionTreeClassifier

music_data = pd.read_csv("music.csv")  # import our dataset
X = music_data.drop(columns=['genre']) #input  set
y = music_data['genre']                #output set

model= DecisionTreeClassifier()         #create a model
model.fit(X,y)                          # train the model
predictions = model.predict([ [32,1], [22,0]])
predictions
```

# Day 2
Today I learn something about the csv files that gifted a huge amount of errors and tackling and learning about those errors were interesting to learn.
Basically I encountered with "errno2 error" which says they didn't find the mentioned directory and at the end trying to shift the location of "weather_data", the issue was solved at an instant. I algo got to familier with the installation of pip (Preferred Installer Program). I also learn about the way how we can get particular section or convert the csv file to Dictionary.

## coding section
```python
import pandas as pd

weather_data = pd.read_csv("weather_data.csv")
# print(type(weather_data))                   
print(weather_data)

data_dict = weather_data.to_dict()
# print(data_dict)
temp_list = weather_data['temp'].to_dict()
# print(temp_list)

print(f"The no of list is {len(temp_list)}")
# average_temp = sum(weather_data["temp"] / len(temp_list))                 # traditional way to find mean
# print(f"The total sum of the temperature is {sum(weather_data["temp"])}")
# print(f"The average temperature of the weekend is {average_temp}")

print(weather_data["temp"].mean())                                         # modern way to find an average 
```

# Day 3
Today, I jumped into the famous project of machine learning project "Dragon Real State" and worked in jupyter notebook. I learned the basic concept of matplotib and pandas.

### read_excel(".xlsx") function
This particular function is used to import the excel file where read_csv(".csv") only worked where the data were saved in csv format.
```python
data = read_excel(".xlsx)
```

### .head()
.head() function is used to display the first five columns and all rows of the csv or excel data and it mainly check wheather the data is working or not.
```python
data.head()
```

### .describe()
.describe() function is used to describe the nature of the data and displays the statistic values like count, mean, standard deviation, percentile, mean, median etc

```python
head.describe()
```
### .info()
.info() displays the count of the data of each rows to confirm if there is missing data or space inbetween the cells.

```python
head.info()
```

### .value_counts()
In this function, it displays the number of 0 and 1 in the certain row

syntax:
```python
data['CRIM'].value_counts()
```
### %matplotlib inline
The %matplotlib inline command tells the IPython environment to draw the plots immediately after the current cell. 

### import matplotlib.pyplot as plt and housing.hist(bins= 50, figsize =(20,15)) are used to import the pyplot of matplotlib and plot a histogram


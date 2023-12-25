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

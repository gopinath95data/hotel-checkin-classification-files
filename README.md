# hotel-checkin-classification-files

### PART 1:

  1. Write a regex to extract all the numbers with orange color background from
  the below text in italics.
  {"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"i
  d":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP
  Warning #2] count(): Parameter must be an array or an object that implements Countable
  (153)"}]}

 #### li =  [i for i in re.findall(":(\d*)",test) if i != '']

### PART 2:

 Customer checkin classification model
 1. Trained model are present in this repo
 2. The model has been tested and test results can be found in the file 'model_test.ipynb'
 3. The model is deployed to streamlit on the link https://gopinath95data-hotel-checkin-classification-app-g0ex4q.streamlitapp.com/

### BONUS POINTS:

 1. Write about any difficult problem that you solved. (According to us difficult - is something which 90% of people would have only 10% probability in getting a
similarly good solution).

I worked on a machine learning system to predict human activity classification. The data I had was sensor readings of each person performing a certain activity. This data was in a form of timestamps of length 3000 or more. It was very diffcult to load it directly with models as RNN models loose data after a specific sequence length.
Also since there were some outliers suring the sensor readings it didnt perform well by feeding the raw data. So I decided to choose a random continuous sequence of smaller sequences. This data was suitable to be fed into a model as well as mostly didnt have any outliers. 
 
 2. Explain back propagation and tell us how you handle a dataset if 4 out of 30 parameters have null values more than 40 percentage

Backpropogation is the process where the values of the weights and biases are updated in a deep learning neural network model. After forward propagation the loss is calculated and based on the loss the contribution of each weight and bias is calculated using chain rule and the parameters are continuosly updated unitl a satisfiable loss is obtained

If a feature has mode than 40% as null values I will mostly drop it since it might contribute to additional noise if we try to impute it.
If the feature is said to be an import one by the domain expert, despite having 40% missing values i will try to impute it with mean, median, mode or other methods, the method i choose depends on whichever method doesnt disturb the distribution of the feature
 

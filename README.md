## PERSONAL OVERVIEW

#### I began this project with the intent to use knowledge I had gained about Machine Learning during last semester, but I ended up learning a lot of new things as well. With this project, I aimed to create a visualization of the data as well as train a Machine Learning model with the data. I was able to accomplish both of these things but I encountered a lot of struggles whilst attempting to preprocess the data before training the model. However, I was able to figure out what I was doing wrong and fix my errors. I was then pretty easily able to train the logistic regression model and display its results.

# PROJECT OVERVIEW

## 1. Reading the dataset into a dataframe
#### I used the pandas library to read the CSV file into a python dataframe. This allowed me to manipulate the data and use it effectively. 
## 2. Data Visualization
#### Using the Matplotlib library, I created a frequency histogram of the data which displayed how much of each star type was in the dataset. This histogram showed me that there were 40 of each star type in the dataset.
<img width="412" alt="hist1" src="https://user-images.githubusercontent.com/67293796/216226918-b133b81c-4eb6-4773-8ee2-f4ab397cc3c1.png">

## 3. Data Preprocessing
#### For the data processing, there was only one major thing I had to do since the dataset was already well maintained and was not missing any data. I had to convert the categorical variables in the dataset such as the Star color and Spectral Class into numeric data. This was necessary preprocessing as machine learning only understand and accept numeric data. I ended up using a built-in pandas function called get_dummies which essentially transforms the categorical variable into a column header and the data in that column is mostly zero's with a one at the row with the correct star. For example if a star is red, this function makes red a whole new columns and fills it in with zero's except for the rows with red stars which it fills in with ones's. After transforming the dataframe to only contain numeric data, it is ready to be processed by the model.

## 4. Training a multiclass logistic regression model
#### Using the preprocessed data, I created the x variable which was all the data assocatiated with the star type and the y variable which was what the model wouuld predict which was the star type. I used the test_train_split function to split the data so that the model could be trained on 70% of the data and tested on the other 30% of the data. I then created the logistic regression model using the LogisticRegression function and fitted it with the training data. 

## 5. Accuracy and Heatmap of the model
The model ended up having 99% accuracy. This is probably due to each star type being unique and so the model was able to perform well. I also created a confusion matrix heatmap to display the results of the model. The heatmap shows that the logistic regression model performed perfectly on all the star type except the 4th star type(Supergiant) where it had a 89% accuracy, hence, the overall 99% accuracy.

<img width="412" alt="Screenshot 2023-02-01 at 10 28 18 PM" src="https://user-images.githubusercontent.com/67293796/216231790-c9145a36-16dd-485c-816e-5d92daae94e2.png">


## 6. Sources used
#### https://www.freecodecamp.org/news/how-to-build-and-train-linear-and-logistic-regression-ml-models-in-python/





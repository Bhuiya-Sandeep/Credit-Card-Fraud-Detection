# Credit Card Detection
### Case
Assume that you are employed to help a credit card company to detect potential fraud cases so that the customers are ensured that they won’t be charged for the items they did not purchase. You are given a dataset containing the transactions between people, the information that they are fraud or not, and you are asked to differentiate between them. This is the case we are going to deal with. Our ultimate intent is to tackle this situation by building classification models to classify and distinguish fraud transactions.
### Steps Involved
Importing the required packages into our python environment.
Importing the data
Processing the data to our needs and Exploratory Data Analysis
Feature Selection and Data Split
Building six types of classification models
Evaluating the created classification models using the evaluation metrics
We are using python for this project because it is really effortless to make use of a bunch of methods, has an extensive amount of packages for machine learning, and can be learned easily. In recent days, the job market for python is seamlessly higher than any other programming language and companies like Netflix are using python for data science and many other applications. With that, let’s dive into the coding part.

## Getting the Data
The data used was made available by some European credit card companies. In the dataset used, we have only 492 frauds among almost 290 thousand transactions, the transactions presented occurred on only two days.

It is possible to observe how extremely unbalanced this dataset is, where frauds represent only 0.17% of the total transactions. Therefore, we will have a considerable amount of work to do when balancing the data.

Some other interesting details are the fact that the variables are all numeric and are private (to preserve the privacy of the clients and for security) and this is why the columns are presented to us as [V1, V2, V3… V28].

This method allows dimensionality reduction while keeping as much information as possible. To do this, the algorithm finds a new set of features called components.

These components are fewer or equal to the original variables. In the case of this project, the components found by the PCA transformation are the columns [V1,V2,V3…V28] themselves.

Once we have the data imported into a DataFrame, we can begin our exploratory analysis and ultimately prepare a Machine Learning model or even some.

## Exploratory Data Analysis
Here is where I will show you some relevant information, so that you can better understand the analysis and feel comfortable while reading.

We can start by checking the first 5 entries of the DataFrame and see what they tell us.

So we can notice that the columns Time and Amount have been kept at their original values, so as not to harm the analysis. We can also clarify that our target variable is located in the Classcolumn, where 0 is a common transaction and 1 is a fraudulent transaction.
## Models Presentation
To show the difference in performance between models trained with balanced and unbalanced data, 8 models were built, being:

4 Logistic Regression Models, where one of them will be trained with unbalanced data and the other three will be trained with balanced data by different methods.

4 Decision Tree Models, which will be distributed in the same way as the Logistic Regression Models.

## Separate Training and Testing
In order for the models to perform well, it is necessary to separate the data between training and testing, so that it can make more accurate predictions when dealing with data that it has not had contact with.

## Data Balancing
Finally, data balancing was done so that the models perform better in identifying fraudulent transactions. With balancing done, it is possible to avoid overfitting (when a model becomes great at making predictions with known data, but performs less well when dealing with new data that has a smaller footprint).

For balancing, 3 methods were used, these being:

RandomUnderSampling (RUS) — This method discards a random subset of the majority class, preserving the characteristics of the minority class, ideal when you have a large volume of data. This method can lead to lower performance when making predictions of the majority class.
ADASYN — Generates new samples, close to the original ones, that are misclassified using a K-Nearest Neighbors classifier. To better understand this method, click here.
SMOTE — The basic implementation of SMOTE, meanwhile, will not distinguish between easy and difficult samples to be classified, as is done in ADASYN.
## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install credit-card.

```bash
pip install credit-card
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

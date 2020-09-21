# Label-Encoding
This module encode(label) values based on the values of another feature  
## conventional label encoding modules such as LabelEncoder from sklearn.preprocessing library usually determine the order of assigning labels to values based on alphabatical sequence,
## however, there are situations that we face values which have intrinsic order such as days in a week, or when we create features which their order can be define by the values of
## another feature, eg. when you decide to bin age feature in a dataset and then you need to encode the values of this new feature to feed an algorithm such as linear regression
## or KNN which are sensitive to the order of values, in this case LabelEncoder cannot provide us with a desire output, so I have defined a fuction which can be useful in this 
## situation.
### I have defined five arguments for this function which I adress below:
### train_frame: is the train dataset which we want to encode its feature/features
### test_frame: if there is a test dataset, for sure we nead to encode its values before performing ML and making any prediction, however, it's possible to make this function optional
### feature: you need to pinpoint the column/feature you want to perform label encoding, if you need to encode more than one feature you can use label encoding fuction in a loop
### order: it is a numerical column/feature which we want to sort/order our values based on it, Age, Fare, etc.
### func: the last argument is the fuction we want our numerical column/feature to be calculated, since I have applyed groupby function to label the values, we need to specify a numpy function such as np.mean, np.median, etc.
## I hope you enjoy using this fuction in your data munging, and for sure please feel free to manupilate the code to improve its applicability:)

# opensource_Finalproject

## About me👋
Name : Hyungjun Jung <br>
CAU ID : 20212132 <br>
Department : Applied Statistics <br>
Double major in AI department <br>
<br>
## About this project
This is our Final-term Project in opensource-sw lecture. <br>
In this project, we classifies Brain Tumors🧠 as Glioma, meningioma, pituitary and no tumor. <br>
To classify brain tumor, I used sklearn module in python and chose one of best classifier in sklearn package which shows higest accuracy score. <br>
Let's check which classifier I chose in this project!
<br>
## About training💪 dataset
Professor gave us image sets of brain tumor which was classified into four areas. <br>
###### glioma, meningioma, no❌, pituitary tumor. <br>
<br>
> number of test datasets📄 -> glioma: 826, meningioma: 825, no: 332, pituitary: 827 <br>
<br>
To train classifier model, I split these data 70% as train data, 30% as test data.

## About Algorithm I chose
I operated many classifiers in sklearn. <br>

```python
from sklearn.ensemble import GradientBoostingClassifier
from sklearn.ensemble import AdaBoostClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.linear_model import Perceptron
from sklearn.tree import DecisionTreeClassifier
from sklearn.svm import SVC
from sklearn.naive_bayes import GaussianNB
from sklearn.neighbors import KNeighborsClassifier
```
I tried all these classifiers to classify brain tumor. <br>
<br>
By accuracy score, I chose SVC(svm) for brain tumor algorithm. <br>
SVC is used in classification and one of supervised learning model. <br>
And it can minimize the upper limit of generalization errors based on structural risk minimization. <br>
<br>
## About hyper-parameter
In SVC, there is many hyper-parameters. <br>
C, kernel, degree, gamma, coef0, shrinking, probability, tol, cache_weight, <br>
verbose, max_iter, decision_function_shape, break_ties, random_state <br>
<br>
Among these, I manipulated C, gamma and kernel! <br>
<br>
C : regularization parameter and it's default is 1.0. <br>
kernel : Specifies the kernel type to be used in the algorithm. If none is given, rbf will be used. <br>
gamma : kernel coefficient for 'rbf', 'poly' and 'sigmoid' which are types of kernel. <br>
<br>
```python
params = {
    'C' : [0.1, 1.0, 10, 100],
    'kernel' : ["rbf", "poly", "sigmoid"],
    'gamma' : [1.0, 0.1, 0.01, 0.001]
}
```
<br>
In kernel, I put {'rbf', poly', 'sigmoid'} <br>
<br>
By accuracy score, kernel parameter is best when it is 'rbf'. <br>
Then I fixed kernel as 'rbf' and manipulated C and gamma, and tried to find best parameters. <br>
<br>
In C, I put {0.1, 1, 10, 100} <br>
In gamma, I put {1.0, 0.1, 0.01, 0.001} <br>
<br>
By accuracy score, when C=10, gamma=1.0, kernel='rbf', my classifier had greatest score!!🥇 <br>
And when gamma is 0.9, it had little bit higher accuracy score. <br> 
That's why I chose 0.9 at gamma. <br>
<br>
Thank you for watching my readme!😊😊

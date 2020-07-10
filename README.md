# PROJECTS

# [Using Climate Data to Uncover Crime Patters in Toronto](https://github.com/calvinchoi21/toronto-crime-clustering)

The aim of this project is to combine crime data obtained from the Toronto Police Service (TPS) with Toronto based climate data from the Government of Canada to uncover patterns in criminal activity in the city as it relates to climate. Cluster analysis is employed to group the data such that objects in the same cluster share more similar properties than objects in other clusters.

- Each record in the preprocessed dataset represents a unique occurrence, including details of the crime committed and temperature/climate on the day of the occurrence.
- Substantial data cleansing and preprocessing was required to transform the raw data into a format suitable for clustering analysis.
- The k-prototypes algorithm from the kmodes package is used to handle the mix of categorical and numerical features in the preprocessed dataset. 
- The more popular k-means algorithm is also employed after some additional preprocessing, however the more versatile k-protoypes algorithm yielded more insightful information due to its ability to handle catagorical data.
- The k-prototypes algorithm was able to locate 5 meaningful clusters. Each record was then assigned to one of these clusters.
- Data visualization and the aggregation of records by cluster was used to understand the charateristics of each cluster. 
- Code: [Link](https://github.com/calvinchoi21/toronto-crime-clustering/blob/master/Toronto_Crime.ipynb)

![](/images/download.png)

# [Predicting Hotel Cancellations](https://github.com/calvinchoi21/predicting-booking-cancellations)

This project uses information entered by the customer at the time of booking to predict whether they will end up cancelling the booking. Several classification algorithms are trained on the dataset to build models that will assign one of two labels to each record, cancelled or not cancelled. 

- Dataset contains records on 119,390 bookings made between two hotels. Extensive EDA was conducted to determine preprocessing needs.
- Custom data transformers are built to automatically discretize, bin, and group specific features, as well as creating new features using existing data. 
- Off-the-shelf sklearn preprocessors are also used to impute missing values, encode categorical data, perform feature selection, etc. 
- Pipelines are constructed to bind together transformers and estimators for further automation. 
- Five classifiers are intially tested, and two were shortlisted (KNN and Random Forest) based on highest f1-score. 
- Used GridsearchCV on pipeline to tweak both estimator and transformer parameters to arrive at the strongest model. 

![](/images/predicting_cancellations.png)

# [Predicting Customer Churns with Classification Algorithms](https://github.com/calvinchoi21/predicting-customer-churn/blob/master/Classification_Customer_Churn.ipynb)

The purpose of this project is to predict whether a telco customer will leave the company, i.e. churn, by utilizing supervised learning in the form of classification. An example of why a company would employ this task is to identify exisiting customers that are likely to churn so that resources such as promotional material be allocated appropriately in an effort to retain them.

For this task, six classification algorthims are initially considered using cross-validation on the training set. Of those six, three are shortlisted for further modelling. For each of those models, the hyperparameters are tuned and the validation set is used to test the performance increase from the tuning. After a model is tuned, a precision and recall trade-off that is appropriate for the task is chosen for it. The final models are then tested on the validation set to compare performance. Finally, the models are tested once more on unseen data via the test set to determine the best performing model.

![](/images/pr%20curve.png)

# Calvin Choi

Calvin Choi is an analytics professional who partners with business and leadership teams to strategize, drive production, and exceed growth objectives. He specializes in different areas of analytics such as visualization, time series, forecasting, predictive analytics, and other data science practices. He enjoys working with messy data using creative problem solving to mine hard-to-obtain insights. All his solutions are geared toward simplicity and explainability regardless of how complex the requirement. Currently he is pursuing a Master of Science degree at Georgia Tech with a focus in statistical analysis, machine learning, and big data techniques. 

# MY PROJECTS

# [Detecting Sarcasm in Text with NLP and Text Classification](https://github.com/calvinchoi21/sarcasm-detection)

The goal of this study is to develop a model that can accurately differentiate sarcastic text from non-sarcastic text. Data for this model included user comments scraped from the popular social news website, Reddit. Natural Language Processing (NLP) techniques were applied to the corpus for text preprocessing and topic modelling. Finally, this study trained and tested several supervised learning algorithms to classify sarcastic and non-sarcastic comments using the bag-of-ngrams approach, along with engineered features that  were also fed into the model. 

- The labelled dataset contains sarcastic and non-sarcastic comments scraped from Reddit ([source](https://www.kaggle.com/danofer/sarcasm)).
- EDA of the comments included 3 main areas: analyzing N-grams of the sarcastic class, exploring the structure of the comments, and analysis on the parts of speech (POS) and named entity recognition (NER) of the comments. 
- For text preprocessing, the comments are first normalized and lemmatized. The text is then converted into a bag-of-unigrams and bag-of-bigrams, and tf-idf weights are also applied to each word, which determines its importance in the overall corpus. 
- Additional features engineered for the model include the length of the comment (by words), the number of ellipses, exclamation marks, question marks, quotation marks, smiley face emoticons, and the number of repeating characters. 
- These text preprocessing and feature engineering steps were built into a single pipeline to allow for quick cross-validation of models when bound to scikit-learn classifiers.
- Five separate classifiers were evaluated and compared. The strongest models utilized the Multinomial Naive Bayes classifier and the Logistic Regression classifier. 
- EDA Code: [Link](https://github.com/calvinchoi21/sarcasm-detection/blob/main/EDA%20-%20Detecting%20Sarcasm%20in%20Text.ipynb)
- Modelling Code: [Link](https://github.com/calvinchoi21/sarcasm-detection/blob/main/Modelling%20-%20Detecting%20Sarcasm%20in%20Text.ipynb)
- Link to full report: [Link](https://github.com/calvinchoi21/sarcasm-detection/blob/main/Report/Final%20Report%20-%20Detecting%20Sarcasm.docx)

![](/images/sarcasm_detection.jpg)

# [Using Climate Data to Uncover Crime Patterns in Toronto](https://github.com/calvinchoi21/toronto-crime-clustering)

The aim of this project is to combine crime data obtained from the Toronto Police Service (TPS) with Toronto based climate data from the Government of Canada to uncover patterns in criminal activity in the city as it relates to climate. Cluster analysis is employed to group the data such that objects in the same cluster share more similar properties than objects in other clusters.

- Each record in the preprocessed dataset represents a unique occurrence, including details of the crime committed and temperature/climate on the day of the occurrence.
- Substantial data cleansing and preprocessing was required to transform the raw data into a format suitable for clustering analysis.
- The k-prototypes algorithm from the kmodes package is used to handle the mix of categorical and numerical features in the preprocessed dataset. 
- The more popular k-means algorithm is also employed after some additional preprocessing, however the more versatile k-protoypes algorithm yielded more insightful information due to its ability to handle catagorical data.
- The k-prototypes algorithm was able to locate 5 meaningful clusters. Each record was then assigned to one of these clusters.
- Data visualization and the aggregation of records by cluster was used to understand the charateristics of each cluster. 
- Code: [Link](https://github.com/calvinchoi21/toronto-crime-clustering/blob/master/Toronto_Crime.ipynb)

![](/images/crime_clusters.jpg)

# [Predicting Hotel Cancellations](https://github.com/calvinchoi21/predicting-booking-cancellations)

This project uses information entered by the customer at the time of booking to predict whether they will end up cancelling the booking. Several classification algorithms are trained on the dataset to build models that will assign one of two labels to each record, cancelled or not cancelled. 

- Dataset contains records on 119,390 bookings made between two hotels. Extensive EDA was conducted to determine preprocessing needs.
- Custom data transformers are built to automatically discretize, bin, and group specific features, as well as creating new features using existing data. 
- Off-the-shelf sklearn preprocessors are also used to impute missing values, encode categorical data, perform feature selection, etc. 
- Pipelines are constructed to bind together transformers and estimators for further automation. 
- Five classifiers are initially tested, and two were shortlisted (KNN and Random Forest) based on highest f1-score. 
- Used GridsearchCV on pipeline to tweak both estimator and transformer parameters to arrive at the strongest model.
- Code: [Link](https://github.com/calvinchoi21/predicting-booking-cancellations/blob/master/Predicting_cancellations.ipynb) 

![](/images/predicting_cancellations.png)

# [Predicting Customer Churns](https://github.com/calvinchoi21/predicting-customer-churn)

This is a binary classification problem and was my foray into supervised machine learning. The purpose of the project was to utilize customer record data from a telco company to predict whether they would leave the company, or in other words churn. Six classification algorithms are tested and shortlisted for this task. The precision and recall trade-off for each model is also considered to simulate the real-life business decision made by an organization. 

- Dataset contains 3,333 records, each containing customer information. Target feature is either 'yes' or 'no', indicating whether that customer churned. 
- Due to heavy class imbalance of target feature, custom metric (based on f1-score of the minority class) is used to grade each model. 
- Six classifiers are initially tested using 5-fold cross-validation, and three are shortlisted based on score of custom metric. 
- Optimized shortlisted models using GridSearchCV to find the best models. 
- Tweaked decision threshold of each model to arrive at desirable precision/recall tradeoff. 
- Plotted PR curves to visualize and compare strength of final models.
- Code: [Link](https://github.com/calvinchoi21/predicting-customer-churn/blob/master/Classification_Customer_Churn.ipynb)

![](/images/churn_curves.jpg)

# [Application of Statistical Testing in Python](https://github.com/calvinchoi21/statistical-testing-in-python)

While Python is a powerful, general purpose, language that is widely used in data science, R is a domain-specific language designed for statistical analysis. The application of statistical formulas are much simplier with R language and the outputs tend to be more informative than Python. This project demonstrate how one can obtain similar functionality as R when conducting parametric and non-parametic testing in Python.

- Built functions using Numpy and Scipy to perform parametic and non-parametric testing and provide similar output to R. 
- Included tests for paried and unpaired samples for comparing two groups, as well as sample and block design tests for comparing more than two groups.
- Code: [Link](https://github.com/calvinchoi21/statistical-testing-in-python/blob/master/statistical_testing_in_python.ipynb)

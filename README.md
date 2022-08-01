
# TANZANIA-WATER-POINTS PREDICTION USING CLASSIFICATION MODELS

For this project, I used different classification models to predict the status of different water points in Tanzania. There are three status groups to be predicted i.e 
- Functional,
- Non-functional and 
- Functional Needs repair. 
This makes this problem a Ternary classification but for  better classification I combined functional water points and functional needs repair as class 1 and non-funtional water points as class 0. 
## Business Problem:
An NGO focused on locating wells that needs repair. The Tanzanian government is looking to find patterns in non-functional wells to influence how new wells are built. As an employee of the NGO i have been tasked with presenting findings on how the Ministry of Water can identify wells that are non-functional or in need of repair, so
## Requirements
This project requires that;

Your Jupyter Notebook should demonstrate an iterative approach to modeling. This means that you begin with a basic model, evaluate it, and then provide justification for and proceed to a new model. After you finish refining your models, you should provide 1-3 paragraphs discussing your final model - this should include interpreting at least 3 important parameter estimates or statistics.
## Data used
The original data was obtained from the DrivenData 'Pump it Up: Data Mining the Water Table' competition. Basically, there are 4 different data sets; submission format, training set, test set and train labels set which contains status of wells. With given training set and labels set, competitors are wanted to build predictive model and apply it to test set to determine status of the wells and submit.

In this project, we used train set and train label set which have 59400 water points data with 40 features.
## Methodology
1.Understanding Data

2.Cleaning and Exploring Data

3.Preparing Data to Modeling

4.Finding Binary Model & Baseline

5.Ternary Target Modeling

Metric: The metric of the competition was defined as balanced accuracy. So, we choose this metric and also to make sure about our results we also used ROC-AUC score to see our model works well or not.

Understanding Data: I realized that most columns had other columns with similar information and that some other columns had zeros which did not make sense hence the need for cleaning.

Cleaning and Exploring Data: Mainly, null, zero and missing values changed to mean or collected in a group as named unknown according to nature of the column.

Preparing Data to Modeling: To prepare our data to machine learning, we did some feature engineering, encoding and scaling for dealing with first challenge. For binary model WoE Encoding and Robust Scaler were used. For, ternary target model, Target Encoder and Robust Scaler used.

Finding Binary Model: To make our ternary target modeling easily, first we simplified the problem in binary target. Logistic Regression was chosen as baseline. To see best results, Decision Tree,Random Forest, K-Neighbors were used to classify and compare results. Parameter Tuning was done for the best Model. 


## Findings:
- The best result for binary problem is taken by using Random Forest which had an accuracy of 85% accuracy for the roc_Auc.

- 4272 wells were dried but they have good water quality. With finding a solution to give source again these wells, they can be functional. Finding clean water sources is not the only problem, to continue to feed these sources are equaly important.

- 2226 (7%) wells have enough and soft water but needs repair. Authorities must invest on repairing. Otherwise these will be non-functional.

- 8035 (27%) wells has enough, good quality water but they are non-functional. This shows that authorities must work and invest on technology to pump these good sources.

- From the confusion matrxi 6625 water points were correctly classified as functional while 683 water points were wrongly classified as Non-functional but were actually funtional water points. Also, 3522 Water points correctly classified as non-functional while 1050 water points were wrongly classiied as functional but were actually non-functional water points.
## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [sklearn_documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.RobustScaler.html)
 - [Data science process lesson](https://github.com/learn-co-curriculum/dsc-data-science-processes)


## Authors

- [waitipeter](https://github.com/waitipeter)


## Lessons Learned

What did you learn while building this project? What challenges did you face and how did you overcome them?

Data understanding.

Data cleaning

Data modelling using classification models.

Researching.

Data Analysis

## CONCLUSIONS & RECOMMENDATIONS

- I can conclude that the best and most efficient model for this business problem was Random forest classier.

- Feature selection will be done, and feature engineering on categorical columns will be good idea to handle first challange.

- Wells can be monitored well and model can be improved according to more accurate and recent data.

- Different regions have different factors like climate, rainfall season etc. So, from the main model, different models can be build for each region.

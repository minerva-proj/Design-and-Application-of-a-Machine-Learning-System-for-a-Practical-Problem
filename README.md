# Design-and-Application-of-a-Machine-Learning-System-for-a-Practical-Problem

objectives
This document specifies the coursework assignment to be submitted by students taking CE802.
Aims of this assignment are: a) to learn to identify machine learning techniques appropriate for
a particular practical problem; and b) to undertake a comparative evaluation of several machine
learning procedures when applied to the specific problem.
Assignment description
1. Pilot-Study Proposal
Imagine that you work as Machine Learning independent consultant, providing scientific advisory
and consulting services to companies seeking to apply data analytics to their business activities.
The energy company AENERGY would like to predict if a customer is going to encounter
difficulties in paying the (increasing!) electricity cost on the basis of a few features (demographic,
heating system power, habits, family composition, etc.). A manager from AENERGY contacts
you to investigate the feasibility of using machine learning to predict whether a customer is going
to suffer from the increasing energy prices. The manager has access to historical data of recent
costumers and she offers to provide you with information about several features of the customers
(e.g. age, family composition, heating system model, habits, etc.), and whether they are currently
struggling with paying their energy bills or not.
In the first part of your assignment, you are asked to write a detailed proposal for a pilot study
to investigate whether the machine learning procedures could be used to successfully solve this
problem. Your report should discuss several aspects of the problem, including the following main
points:
• the type of predictive task that must be performed (e.g., classification, regression, clustering,
rules mining, ...);
• examples of possibly informative features that you would like to be provided with (what type
of information AENERGY could obtain from/about the customers is likely to be a good
predictor?);
1
• the learning procedure or procedures (e.g., DTs, k-NN, k-means, linear regression, Apriori,
SVMs, ...) you would choose and the reason for your choice;
• how you would evaluate the performance of your system before deploying it.
You can assume that the manager has some knowledge of machine learning and you do not need to
explain how the recommended learning method works. Simply discuss your recommendation and
back it with sound arguments and/or references.
This document should consist of approximately 500–750 words of narrative (i.e. excluding
references, pictures, and diagrams). Please report your word count on the title page. The document
must be submitted in PDF format with file name CE802_Pilot.pdf.
2. Comparative Study
Thanks to the convincing arguments in your pilot-study proposal, AENERGY decides to collect the
data that you suggested and to hire you to perform the proposed study. They provide you with a
training set of historical data containing features of each customer and a label representing whether
the customer belongs to the class of people who had problems with paying their energy bills during
the last few months (the value TRUE in the data means ”Yes, they suffered from the increasing
energy prices”). These data are available in the CE802_P2_Data.zip archive available from the
CE802 moodle page. In this part of the assignment, you are asked to perform the following two
tasks.
a) Investigate the performance of a number of machine learning procedures on this
dataset. Using the data in the file CE802_P2_Data.csv contained in the CE802_P2_Data.zip
archive, you are required to perform a comparative study of the following machine learning procedures:
• a Decision Tree classifier;
• at least two more ML techniques to predict if a new customer is prone to suffer from energy
rising prices.
You will notice that one of the features, is missing for some of the instances. You are therefore
required to deal with the problem of missing features before you can proceed with the prediction
step. As a baseline approach, you may try to discard the feature altogether and train on the
remaining features. You are then encouraged to experiment with different imputation methods.
AENERGY uses Python internally and therefore Python with scikit-learn is the required language
and machine learning library for the problem. For this task, you are expected to submit a
Jupyter Notebook called CE802_P2_Notebook.ipynb containing the Python code used to perform
the comparative analysis and produce the results, as well as the code used to perform the predictions
described in task “b” below.
b) Prediction on a hold-out test set. An additional dataset, CE802_P2_Test.csv, is provided
inside the CE802_P2_Data.zip archive. Binary outcomes are withheld for this test set (i.e. the
“Class” column is empty). In this second task, you are required to produce class predictions of
the records in the test set using one approach of your choice among those tested in task “a” (for
example the one achieving the best performance). These data must not be used other than to test
the algorithm trained on the training data.
As part of your submission, you should submit a new version of the file CE802_P2_Test.csv in
CSV format with the missing class replaced with the output predictions obtained using the approach
chosen. This second task will be marked based on the prediction accuracy on the test set.
2
3. Additional Comparative Study
Thanks to the good results obtained in the comparative study, the company AENERGY has deployed
your system and is obtaining good results. Now they want to hire you for another job: to
design another system to predict the variation in the annual expenditure that a customer is going
to have due to the increase of the energy cost (in £/year, positive if next year the customer is going
to spend more, negative if they are going to spend less).
They did a pilot study to assess the annual variation in the total expenditure for energy. They
provide you with a training set of historical data containing features of each customer and a numerical
value representing the variation in the annual expenditure for each customer included in the
pilot study. This value may be negative because there were also customers who spent less money
despite the rising costs of energy thanks to the correct use of a new and more efficient heating system.
These data are available in the CE802_P3_Data.zip archive available from the CE802 moodle
page. In this part of the assignment, you are asked to perform the following two tasks.
a) Investigate the performance of a number of machine learning procedures on this
dataset. Using the data in the file CE802_P3_Data.csv contained in the CE802_P3_Data.zip
archive, you are required to perform a comparative study of the following machine learning procedures:
• Linear Regression;
• at least two more ML techniques to predict the value of the variation in annual expenditure
for each customer ( in £/year ).
The company AENERGY uses Python internally and therefore Python with scikit-learn is the
required language and machine learning library for the problem.

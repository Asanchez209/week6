# SVM 
#SVM is a supervised machine learning algorithm used for classification and regression tasks. It aims to find the optimal hyperplane that best separates different classes in the data by maximizing the margin between them.

#For the SVM model, we can calculate accuracy using:

accuracyrate <- sum(diag(tab)) / sum(tab)

accuracyrate

#The accuracy for the SVM model is 97.3% We can conclude the model classified 97.3% of cases correctly, it did a good work at predicting cases correctly.

# C50 
#C50 is a supervised machine learning algorithm used for classification tasks. It constructs decision trees using a combination of information gain and gain ratio techniques.

#For the C50 model, we can calculate accuracy using:

accuracyrate <- mean(testData$Species == predict(dtModel, testData))

accuracyrate

#The accuracy for the C50 model is 88.8% We can conclude the model classified 88.8% of cases correctly, it did a good work at predicting cases correctly.

# K-means 
#K-Means is an unsupervised machine learning algorithm used for clustering data points into groups (clusters) based on their similarity. It aims to partition the data into K clusters, where each point belongs to the cluster with the nearest mean.

#For the K Means model, we can calculate accuracy using:

setosa_correct <- table(result$cluster,iris.class)[2,1] #correct setosa

versicolor_correct <- table(result$cluster,iris.class)[3,2] #correct versicolor

virginica_correct <- table(result$cluster,iris.class)[1,3] #correct setosavirginica

accuracyrate <- (setosa_correct + versicolor_correct + virginica_correct)/total_classified

accuracyrate

#The accuracy for the K means model is 13%. We can conclude the model classified 13% of cases correctly, it did not do a good work at predicting cases correctly.

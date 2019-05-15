Error Analysis
-----------------
#### 360-420-DW - Section 02
#### Natiah Randrianasolo

## Distributions of Model Accuracy
----------------------------------

##### 1. Why do we get a different accuracy each time we run the classification model?

In DataSet.java, the line 150 refers to the method "shuffle" from the "Collections" class which randomly accesses different elements from a given string. So, for each time we run the code, the positions where the data are cut are set randomly, and this makes us work with a different section of data for every trial, affecting the accuracy for each run. 

##### 2. How much does performance can be expected to vary on unseen data?

Performance can be expected to vary slightly on unseen data each time the classification model is run. Since the standard deviation is very small, the performance can be considered to be good. 

Mean: 0.9576214336890432

Standard Deviation: 1.7245764556367892 x 10^-4

##### 3. What is a sensible baseline against which we should compare our model's performance?

A sensible baseline that we should use to compare our model's performance is random identification. For example, if the majority of data shows positive, then we can run the classification model assuming that all of the data are positives. By doing this, we will get a maximum accuracy equal to the actual number of positive data. In DataSet.java, line 200 refers to a method that indicates the frequency of a given label. For instance, if the frquency of a label is 70%, we can conclude that we are 70% accurate that all
the data correspond to that label. 

## Analysis of different error types
---------------------------------

##### 4. What is a False Positive?

A False Positive is getting a test result which inducates that a particularion condition is present when it's not actually the case. For example, a False Positive would be getting the result that the breast cancer is malignant when it is in fact benign. 

##### 5. What is a False Negative?

A False Negative is getting a test result which indicates that a person does not have a particular condition when it is actually the case. For example, a False Negative would be getting the result that the breast cancer is benign when it is in fact malignant. 

##### 6. Extend your analysis in the previous step (with the 1000 runs) to keep track of Recall and Precision as well.

a. What makes these two measures different?

Recall corresponds to the fraction of relevant elements received over the total number of relevant elements. It is the fraction of the true positives over the total number of positives where that number is the sum of the false negatives and the true positives. 
	
  Mean Recall: 0.9443746131060761 
 
 Precision correspons to the fraction of relevant elements received over the total number of selected elements. 
	it's the fraction of true positives over the number of predicted positvies where that number is the sum of the true
	positives and the false positives.
  
  Mean Precision: 0.94581414569178056
			
  Recall and Precision are different measures since they calculate two different proportions of the data. 
	Most of the time, the ratio between the two measures are similar since the total number of positives is
	approximately equal to the number of predicted positives. 
  
  b. What are sensible baseline for each of these measures?	

The sensible baseline for each of these measures would be 1 since the closer the ratio is to 1, the more precise it will be. If the number is close to 1, it means that the predicitons made were good. In the case of the recall, the baseline is also 1 because both the recall and the precision have similar ratios. 

##### 7. How do the above results change with the hyperparameter k?

The hyperparameter k indicates the number of closest neighbors used to determine the class of an element. 
When k is big, it is harder to figure out the class of the element since the program will have to go through a bigger
number of neighbors' classes before assigning the right class to the element. Also, the k should be odd to avoid tied votes. 

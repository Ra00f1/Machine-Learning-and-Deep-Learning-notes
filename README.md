# Metrics
## Accuracy
Out of all the predictions we made, how many were true?
![image](https://github.com/user-attachments/assets/b09e13d8-3550-46cb-b423-a37372977ea4)

## Precision 
Out of all the positive predictions we made, how many were true?

![image](https://github.com/user-attachments/assets/48d3eb38-f2f0-4856-848f-792bee87f328)

## Recall 
Out of all the data points that should be predicted as true, how many did we correctly predict as true?

![image](https://github.com/user-attachments/assets/db2603a2-34b3-4697-be84-246245a05de8)

## F1 Score
F1 Score is a measure that combines recall and precision. As we have seen there is a trade-off between precision and recall, F1 can therefore be used to measure how effectively our models make that trade-off.

![image](https://github.com/user-attachments/assets/f8e9cbc3-dfd9-443c-aa3b-2ba7c5c9b6ff)

# Confusion matrix
* True Positive: You predicted positive, and it’s true.
* True Negative: You predicted negative, and it’s true.
* False Positive: (Type 1 Error): You predicted positive, and it’s false.
* False Negative: (Type 2 Error): You predicted negative, and it’s false.
* Accuracy: the proportion of the total number of correct predictions that were correct.
* Positive Predictive Value or Precision: the proportion of positive cases that were correctly identified.
* Negative Predictive Value: the proportion of negative cases that were correctly identified.
* Sensitivity or Recall: the proportion of actual positive cases which are correctly identified.
* Specificity: the proportion of actual negative cases which are correctly identified.
* Rate: It is a measuring factor in a confusion matrix. It has also 4 types TPR, FPR, TNR, and FNR.
![image](https://github.com/user-attachments/assets/8e174093-ab54-40a7-a442-549c3c2f6764)

# Logarithmic Loss
Log loss penalizes the false (false positive) classification. It usually works well with multi-class classification. 
![image](https://github.com/user-attachments/assets/7de4276f-e9ba-4423-a074-4010892d56c4)

# Area Under Curve (AUC)
It is one of the widely used metrics and basically used for binary classification. The AUC of a classifier is defined as the probability of a classifier will rank a randomly chosen positive example higher than a negative example. 

# Mean Absolute Error (MAE)
Mean Absolute Error(MAE) is the average distance between predicted and original values. Basically, it gives how we have predicted from the actual output. However, there is one limitation i.e. it doesn't give any idea about the direction of the error which is whether we are under-predicting or over-predicting our data.
![image](https://github.com/user-attachments/assets/59d9223c-37c5-4f60-83a8-bef715f423ce)

# Mean Squared Error (MSE)

# Root Mean Squared Error (RMSE)


# Machine Learning Summary
## Unsupervised Learning
### Clustering 
#### K-Means Clustering
![image](https://github.com/user-attachments/assets/1104db5d-2747-46e3-8b35-ac1cfe2c2792)
![image](https://github.com/user-attachments/assets/03c702bd-b51e-45ed-8914-878e03ddc4f4)
##### Cost functions:
###### MSE
![image](https://github.com/user-attachments/assets/ed3764b0-9124-4c03-a6b9-7c8e9a62a310)
##### WCSS
![image](https://github.com/user-attachments/assets/c76192c8-1f0b-4191-8e4a-aa3a40498ef1)
##### Cross-Entropy Loss
![image](https://github.com/user-attachments/assets/f13616d0-d3e9-43f5-9edc-a3fcbacf2b6d)

![image](https://github.com/user-attachments/assets/e6557ca9-4e4e-4871-9ec7-aba752868219)

#### Inertia 
Calculated at the end to see how compacted the groups are and can be used with the "Elbow Method" to determine the ideal number for k.
![image](https://github.com/user-attachments/assets/9398bfb9-fc5c-4554-9cc4-d1b015997d54)
![image](https://github.com/user-attachments/assets/9da37e1b-5adc-49b4-ae37-fe8822d10ec1)

#### Initializing K-Means
 One of the best ways is to have hundreds of test cases at which centroids are chosen at random and to train them and choose the one with the lowest cost.

#### Choosing the best 
While "Eblow Method" can be used there is an other method as well which uses the silhoette of the model to choose the ideal number for k.

For each data point 𝑖:
- Compute Cohesion (𝑎𝑖) → The average distance between 𝑖 and all other points in the same cluster.
- Compute Separation (𝑏𝑖) → The average distance between 𝑖 and the nearest cluster (not including its own cluster).
- Calculate the Silhouette Score for point 𝑖:

  ![image](https://github.com/user-attachments/assets/f897fe64-7588-4624-86c5-a5771889921c)

𝑆𝑖 ranges from -1 to 1:
- Close to 1 → Well-clustered (correct assignment).
- Close to 0 → Overlapping clusters.
- Negative → Misclassified point.

Overall Formulla:

![image](https://github.com/user-attachments/assets/46b6a21c-3b0b-46b1-a390-9b7beb5a45c5)

![image](https://github.com/user-attachments/assets/9d29e3aa-eaa6-4304-888b-906ff8f5c03f)


___________________________________________________________________________________________________________________________________________________________
# Convolutional Neural Networks Summary
## Notes
f: Filter Size, s: Stride, p: Padding, n: Input Size, b: bias
- Filter Output Size: ((n + 2p - f) / s ) + 1
- Total Parameters: (n * f) + b
- Output after Max Pooling: ((n * f) / s) + 1
- Padding for "same" convolution: (f - s - 1) / 2 
## Classic Networks
### -AlexNet
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/0651433d-ced9-4a65-91bd-7fe9de5499ad)
###  -VGG-16
- Smaller and easier compared to other networks
- Conv Layers: has the same filter size(3x3), stride of 1, and "same" padding
- Max-Pool: 2x2 and stride 2
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/f133ea64-99fc-476d-8895-a78c8d7acdc1)

## ResNet
ResNets are like normal networks but they have jumps every few layers which normally is either 2 or 3 layers and each one witj a jump is called a residual block.

One of experts I talked to explained it like this: while plain networks try to find which data the input resembles to, ResNets try to change the image into a data that it has worked with before.

### Residual Block:     ![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/daf88f55-c510-4783-b1ea-9a414dfddcb7)

### Residual Block Formula: ![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/44ce9aaa-9297-46b3-8e00-3310c0adb310)

<img src="https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/42b42fdd-632b-4334-8063-69923e6e33b8" width="1100" height="400">

# Coding Notes
This part is mostely for translating math formulas into code when practicing and for future use.
```
np.linalg.norm(X[i] - centroids[j]) 
```
![image](https://github.com/user-attachments/assets/eac29917-41c1-47ff-9b20-e1b1aab36fb9)
- https://numpy.org/doc/stable/reference/generated/numpy.linalg.norm.html
______________________________________________________________
```
points = X[idx == k]
```
- get all the points in X that have the idx equal to k
______________________________________________________________
```
centroids[k] = np.mean(points, axis = 0)
```
![image](https://github.com/user-attachments/assets/164dab95-944f-443c-93bd-2631f051e837)

- The formula looks complicated however it is jsut a mean of the group formula
- https://numpy.org/doc/stable/reference/generated/numpy.mean.html
# Notes
Loss function: Error for a single training example.

Cost function: Average of the loss functions of the entire training set.



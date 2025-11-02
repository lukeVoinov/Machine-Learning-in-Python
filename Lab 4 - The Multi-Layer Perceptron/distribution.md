# **Points/Work Distrbution for Lab 4 - The Multi-Layer Perception**
3 points are distributed among the team members: Nimai, Emmanuel, Luke, and Tiffany. Some parts may overlap and may need more support from rest of team members. If one person is done with their part, they should be available to help out with other people's parts. 

## Luke (3 points total)
### **Load, Split, and Balance (2 points total)**

- [x] **[.5 points]** (1) Load the data into memory and save it to a pandas data frame. Do not normalize or one-hot encode any of the features until asked to do so later in the rubric. (2) Remove any observations that having missing data. (3) Encode any string data as integers for now. (4) You have the option of keeping the "county" variable or removing it. Be sure to discuss why you decided to keep/remove this variable. 
The next two requirements will need to be completed together as they might depend on one another:
- [x] **[.5 points]** Balance the dataset so that about the same number of instances are within each class. Choose a method for balancing the dataset and explain your reasoning for selecting this method. One option is to choose quantization thresholds for the "ChildPoverty" variable that equally divide the data into four classes. Should balancing of the dataset be done for both the training and testing set? Explain.
- [x] **[1.0 points]** Assume you are equally interested in the classification performance for each class in the dataset. Split the dataset into 80% for training and 20% for testing. There is no need to split the data multiple times for this lab.
Note: You will need to one hot encode the target, but do not one hot encode the categorical data until instructed to do so in the lab.
### **Exceptional Work (1 points total)**
- [ ] One idea (required for 7000 level students):  Implement adaptive momentum (AdaM) in the five layer neural network and quantify the performance compared to other methods.  
You can turn this assignment in late (up to three days) but you will receive 0 points for the exceptional credit. 

## Tiffany (3.25 points, 0.75 split with Luke)
### **Pre-processing and Initial Modeling (2.5 points total)**
You will be using a two layer perceptron from class for the next few parts of the rubric. There are several versions of the two layer perceptron covered in class, with example code. When selecting an example two layer network from class be sure that you use: (1) vectorized gradient computation, (2) mini-batching, (3) cross entropy loss, and (4) proper Glorot initialization, at a minimum. There is no need to use momentum or learning rate reduction (assuming you choose a sufficiently small learning rate). It is recommended to use sigmoids throughout the network, but not required.
- [X] [.5 points] Use the example two-layer perceptron network from the class example and quantify performance using accuracy. Do not normalize or one-hot encode the feature data (not yet). Be sure that training converges by graphing the loss function versus the number of epochs. 
- [X] [.5 points] Now (1) normalize the continuous numeric feature data. Use the example two-layer perceptron network from the class example and quantify performance using accuracy. Be sure that training converges by graphing the loss function versus the number of epochs.  
- [X] [.5 points] Now(1) normalize the continuous numeric feature data AND (2) one hot encode the categorical feature data. Use the example two-layer perceptron network from the class example and quantify performance using accuracy. Be sure that training converges by graphing the loss function versus the number of epochs. 
- [X] [1 points] Compare the performance of the three models you just trained. Are there any meaningful differences in performance? Explain, in your own words, why these models have (or do not have) different performances.  
Use one-hot encoding and normalization on the dataset for the remainder of this lab assignment.
### **Modeling**
- [X] [1.5 points] Add support for a third layer in the multi-layer perceptron. Add support for saving (and plotting after training is completed) the average magnitude of the gradient for each layer, for each epoch (like we did in the flipped module for back propagation). For magnitude calculation, you are free to use either the average absolute values or the L1/L2 norm.
Quantify the performance of the model and graph the magnitudes for each layer versus the number of epochs.
    - Split this with part w/ Luke

## Emmanuel & Nimai (6.5 total)
### **Modeling**
- [x] Quantify the performance of the model and graph the magnitudes for each layer versus the number of epochs.
- [x] [1.5 points] Repeat the previous step, adding support for a fourth layer.
- [x] [1.5 points] Repeat the previous step, adding support for a fifth layer. 
- [ ] [2 points] Implement an adaptive learning technique that was discussed in lecture and use it on the five layer network (choose either RMSProp or AdaDelta). Discuss which adaptive method you chose. Compare the performance of your five layer model with and without the adaptive learning strategy. Do not use AdaM for the adaptive learning technique as it is part of the exceptional work.

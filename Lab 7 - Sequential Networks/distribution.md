# **Points & Work Distribution for Lab 7 -- Sequential Networks**

https://www.kaggle.com/datasets/programmer3/grammar-error-correction-dataset

We could use this dataset to input the text and output the error type. Thus, if a person says "He bought two breads.", the sequential network should output "Noun Form" 

**Notes from Town Hall**:

Preparation:
- do not try to do translation, don't go beyond what Larson has shown us to do
- first step: go through the process of tokenization (why you did certain X things), give histograms/graphs showcasing anything
- evaluation metrics: justify business case (why you should care between different classes, here's how you're gonna evaluate it, etc.)
      - finding perfect argument for evaluation metrics
- dataset may be divided

Modeling:
- 4 trained models (and change hyper parameter, can change CNN for ex)
    - can add more layers, or change dimensionality of feed forward network, or self attention to make it convolutionally more ???
    - showing to make sure that everything converges
- how to figure out which parameter is the best?
- add transformer layer (second)
- 2nd last point: refer to 13 sequences notebook from class
- statistical comparison to test which model is superior (same thing last lab)
    - does it work? which one is the best one? relate it to the business case

Exceptional Work:
- RoPE??
  

In this lab, you will select a prediction task to perform on your dataset, evaluate a sequential architecture and tune hyper-parameters. If any part of the assignment is not clear, ask the instructor to clarify. 

This report is worth 11% of the final grade. Please upload a report (one per team) with all code used, visualizations, and text in a rendered Jupyter notebook. Any visualizations that cannot be embedded in the notebook, please provide screenshots of the output. The results should be reproducible using your report. Please carefully describe every assumption and every step in your report.

Dataset Selection

Select a dataset that is text. That is, the dataset should be text data (that has not yet been preprocessed). You will perform the pre-processing on the dataset. In terms of generalization performance, it is helpful to have a medium sized dataset of similar sized text documents. You must perform multi-class classification (binary classification is not allowed). The classification should be "many-to-one" sequence classification. Be sure to provide a link or citation to your chosen dataset.

Grading Rubric

Preparation (3 points total)
[1 points] Define and prepare your class variables. Use proper variable representations (int, float, one-hot, etc.). Use pre-processing methods (as needed). Describe the final dataset that is used for classification/regression (include a description of any newly formed variables you created). Discuss methods of tokenization in your dataset as well as any decisions to force a specific length of sequence.  

[1 points] Choose and explain what metric(s) you will use to evaluate your algorithm’s performance. You should give a detailed argument for why this (these) metric(s) are appropriate on your data and your business/policy case. That is, why is the metric appropriate for the task (e.g., in terms of the business case for the task). Please note: rarely is accuracy the best evaluation metric to use. Think deeply about an appropriate measure of performance.

[1 points] Choose the method you will use for dividing your data into training and testing (i.e., are you using Stratified 10-fold cross validation?   Shuffle splits?   Why?). As part of this argument, be sure to discuss how image processing influences sequential modeling.  Explain why your chosen method is appropriate or use more than one method as appropriate. Convince me that your train/test splitting method is a realistic mirroring of how an algorithm would be used in practice. 


Modeling (6 points total)

[3 points] Investigate two different sequential network architectures (e.g., a CNN and a Transformer). Alternatively, you may also choose a recurrent network and Transformer network. Be sure to use an embedding layer (it is fine to use either pre-trained or your own embedding). Adjust one hyper-parameter of each sequential network architecture to potentially improve generalization performance (train a total of at least four models).  Visualize the performance of training and validation sets versus the training iterations, showing that the models converge.
As an example, you might choose to train two CNN architectures (perhaps with a different number of filters or different number of layers). You may also choose to train two transformers (perhaps with a different number of heads).

[2 points] Using the best parameters and architecture from the Transformer in the previous step, add a second Transformer layer (that uses multi-headed self attention) to your network. That is, the input to the second transformer layer should be the output sequence of the first transformer layer.  Be sure to use some kind of learning rate scheduler. Visualize the performance of training and validation sets versus the training iterations, showing that the model converges. 

[2 points] Use the method of train/test splitting and evaluation criteria that you argued for at the beginning of the lab to compare performances. Visualize the results of all the models you trained.  Use proper statistical comparison techniques to determine which method(s) is (are) superior.  

Exceptional Work (1 points total)

You have free reign to provide additional analyses.
One idea (required for 7000 level students to do one of these options):
Use rotary positional encoding (RoPE) in your best performing transformer model. Compare this performance to using another kind of positional encoding.  

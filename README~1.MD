# Facial Emotion Recognition Model implementation for FER-2013 to use in assessment 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
100 words to explain what your project is about to a general audience.

The project is for implement a model for Facial Emotion Recognition as in the area of clinical pscyhologyst could get some help for getting more precise assessment using Facial Emotion Recognition and contrast the emotions detected with what the clinical psychologist can perceive in the psychology interviews for Gessell chambers. The relevant aspect will be the design of a ML model to assess the tasks for Facial Emotion recognition and help with it for better psychology assessments.


## DATA
A summary of the data you’re using, remembering to include where you got it and any relevant citations. 

I chose the FER-2013 as it is dataset specific for Facial Emotion Recognition and it can be open downloaded and used. The FER-2013 is typically provided in a CSV (Comma-Separated Values) format. Each row in the CSV file represents an image and its associated label (facial expression). i got the FER-2013 dataset from Kaggle.
The FER-2013 dataset contains a total of 35,887 grayscale images of facial expressions. These images are divided into three subsets: training, validation, and testing. But for our application we will only use the happy, sad, surprise and neutral expression for hardware limitations anc trainnig cost.


## MODEL 
A summary of the model you’re using and why you chose it. 
As ths is a classification task, I will try to use a resnet and a vgg16 but in the test it looks that both did not perform too good. So I implement a new model using CNN 7 layers and 2 fully connected layers. I finally choose this as the data input is small and it produced the best results and using Bayessian Optimization for hyperparameter optimization it gets even better results in the performance metrics.


## HYPERPARAMETER OPTIMISATION
Description of which hyperparameters you have and how you chose to optimise them. 
For the scope of the task and the some limitation of hardware and cost as I used colab with GPU  to train the model , validate and test, I tunned one hyperparameter that it was the learning rate, using Bayessian  Optimization and giving good great results with high accuracies for the validation set and very good improvement in the test set.

## RESULTS
A summary of your results and what you can learn from your model 

with the best hyperparameter learning rate found we got this:

Found 128 images belonging to 4 classes.
4/4 [==============================] - 0s 10ms/step
              precision    recall  f1-score   support

           0       0.81      0.78      0.79        32
           1       0.66      0.59      0.62        32
           2       0.56      0.62      0.59        32
           3       0.88      0.88      0.88        32

    accuracy                           0.72       128
   macro avg       0.72      0.72      0.72       128
weighted avg       0.72      0.72      0.72       128

images can see in the jupyter notebook in the confussion matrix.

You can include images of plots using the code below:
![Screenshot](image.png)

I learn from the model the power of the Bayessian Optimization as it improves the performance a lot  and the searching ranges as it can be selected in the hyperopt library it helps to refine the search spaces. In the results it can see that a couple of emotions got a greater misclassification that could be attributed for the lower quantity of pictures, noise in the images and similar factors. All these can be improved with bigger datasets.

## (OPTIONAL: CONTACT DETAILS)
If you are planning on making your github repo public you may wish to include some contact information such as a link to your twitter or an email address. 


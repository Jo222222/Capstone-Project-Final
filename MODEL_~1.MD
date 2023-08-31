# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** Describe the inputs of your model 

The inputs of my model will be the the image training dataset from the FER-2013 but only for the four emotions selected that are 
happy, surprise, sad and neutral. All of them are represent by an array of numbers and we will use one channel for them and all in gray scale, the data will be prepared and splitted with imagedatagenerator from keras.

**Output:** Describe the output(s) of your model

The outputs will be the four emotions selected to classify that are happy, surprise, sad and neutral, for our case it will be organized in this order the classes: classes = ['happy', 'sad', 'neutral', 'surprise']

**Model Architecture:** Describe the model architecture you’ve used

For the model architecture for the artificial neural network I choose to use Convolutions, dropouts, Relu, in summary the model is composed of 7 CNN and 2 Fully connected networks with a total of these parameters:
Total params: 7,842,500
Trainable params: 7,840,068
Non-trainable params: 2,432

## Performance

Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

The performance will be measured using the metrics of accuracy, precision, recall and F1-score. The graphics and results can see in the notebook of the programming implemented.
Some metrics obtained for the test:

4/4 [==============================] - 1s 14ms/step
              precision    recall  f1-score   support

           0       0.93      0.78      0.85        32
           1       0.57      0.62      0.60        32
           2       0.56      0.62      0.59        32
           3       0.97      0.91      0.94        32

    accuracy                           0.73       128
   macro avg       0.75      0.73      0.74       128
weighted avg       0.75      0.73      0.74       128




## Limitations

Outline the limitations of your model.

Some limitation of my model is the reduced quantity of images as it cannot be good for generalized if the images are input in more channels or colors.
If the images are blurred or not so clear it wont work good to classify. Some other limitation can be overfitting as the dataset could be small, the data quality as shown before for blurring, image clarity, the resolution that is small, maybe it could be improved for new datasets, interpretability as deep neural networks as CNN are not to easy to understand and other limitation could be class imbalance. 


## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 

In the context of deep learning and neural networks, there are several trade-offs that you need to consider when choosing a model architecture and training approach. These trade-offs involve factors such as model complexity, training time, and performance. Here are some of the key trade-offs in where the model can exhibit performance issues:

Model Complexity vs. Training Data:
   - Trade-off: Increasing model complexity (e.g., adding more layers or neurons) can potentially lead to better model performance. However, it also increases the risk of overfitting, especially when you have limited training data.
   - Consideration: Balance model complexity with the amount and quality of training data. If we have a small dataset, use simpler models or apply regularization techniques to prevent overfitting. As the data was small I chooose to make an artificial neural network

Training Time vs. Model Performance:
   - Trade-off: Training deep neural networks can be computationally expensive and time-consuming, especially for large models. Smaller models train faster but may not achieve the same level of performance.
   - Consideration: Choose a model size that aligns with your available computational resources and time constraints. You may also consider transfer learning to leverage pre-trained models.

Bias vs. Variance:
   - Trade-off: Increasing model complexity can reduce bias (underfitting) but may increase variance (overfitting). Balancing these two factors is crucial for achieving good generalization.
   - Consideration: Use techniques like cross-validation to find the right level of model complexity that minimizes both bias and variance.

Interpretability vs. Complexity:
   - Trade-off: Complex neural network architectures, such as deep convolutional networks, can be challenging to interpret. Simpler models like linear regression are more interpretable but may have limited capacity in visual recognition tasks.
   - Consideration: Depending on the application, it is recommenden to choose a model that strikes the right balance between interpretability and complexity. Techniques like feature importance analysis can help interpret complex models.

Data Augmentation vs. Model Complexity:
   - Trade-off: Data augmentation techniques can increase the effective size of your training dataset and help improve model generalization. However, they also introduce some additional complexity into the training pipeline.
   - Consideration: Use data augmentation when we have limited training data, as we did in the project,  but it is good to be mindful of how it impacts training time and complexity.






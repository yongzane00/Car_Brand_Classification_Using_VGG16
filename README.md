# Car_Brand_Classification_Using_VGG16
 Modifying VGG16 pre-trainned CNN to classify car brands

# Problem Statement
 VGG16 model is a relatively large model tends to overfit with small sample size. Using accuracy as the evaluation metrics will result in fluctuation of the validation accuracy, therfore, reducing the robustness of the model.

# Methodology 
 1. Unfreezing last covolutional block of the VGG16
    In order to fine-tune the VGG16 so that it fit wells to classify car brands. This step is cruicial to train the last convolutional block and update the weights of each nodes during each epoch.
 2. Add in Regularization term
    Unfreezing the convolutional block has the tendancy to overfit the data, which can fits better to the train data but fails to converge for the test data. L2 Regularization term is added here to avoid overfitting.
 3. Optimize the other parameters
    Optimize parameters such as learning rate, number of epoch, switching to F1 evaluation metrics to obtain better results.

# Conclusion
 We can see there's significant improvements based on the confusion metrics below after modifying the VGG16 CNN. 

 Before:
 ![Alt text](image.png)

 After:
 ![Alt text](image-1.png)


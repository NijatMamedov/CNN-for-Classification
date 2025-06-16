# CNN-for-Classification
 1. Import necessary libraries

 First, I import all the essential libraries like TensorFlow, NumPy, and Matplotlib.

 I also load image processing tools like ImageDataGenerator from Keras for efficient image handling.

⸻

 2. Upload train and test images and convert them into data

 I upload train.zip and test.zip.

 Then I unzip the files and organize the images into proper folders by class.

 After that, I use ImageDataGenerator to preprocess the images and load them into generators for training and validation.

⸻

 3. Create model (CNN + ANN + compile)

 I build a CNN model using layers like Conv2D, MaxPooling2D, and Flatten to extract image features.

 Then I add ANN layers using Dense for classification.

 Finally, I compile the model with:

	•	Optimizer: adam
	•	Loss: categorical_crossentropy
	•	Metric: accuracy

⸻

 4. Optimize hyperparameters with Optuna TPESampler

 I use TPESampler from Optuna to search for the best hyperparameters.

 I define an objective function and let Optuna run multiple trials.

 After training, I select the best parameters based on validation accuracy.

⸻

 5. Use best parameters for CNN + ANN + compile and create final model

 Using the best parameters from Optuna, I rebuild the CNN + ANN model.

 I adjust the architecture accordingly.

 Then I re-compile the model using the optimized settings.

⸻

 6. Fit data with final model

 I train the final model on the training dataset.

 During training, I monitor the loss and accuracy.

 I also save the training history so I can visualize the performance over epochs.

⸻

 7. Use images for deployment and check if model predictions are correct

 I load individual images for prediction.

 I use the trained model to predict the class of each image.

 Finally, I display the predictions and verify if they are correct.

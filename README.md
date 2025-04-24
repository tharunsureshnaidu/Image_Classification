# Image_Classification
Image Classification whether a person is Happy or Sad

Here I have Web scraped and collected the Images of Happy people and Sad ones in Seperate Folder 

Data Collection:
Web Scraping: Collected images of happy and sad individuals using automated scripts.

Dataset Structuring: Organized into separate folders for each class.

 Data Preprocessing:
Image Resizing to (256x256) pixels.

Normalization of pixel values to the range [0, 1].

Augmentation (optional but recommended): Used techniques like rotation, flipping, and zoom to increase dataset diversity and reduce overfitting.

Model Architecture:
Implemented a Convolutional Neural Network (CNN) using TensorFlow / Keras.

Architecture highlights:

Multiple Conv2D + BatchNormalization + MaxPooling2D layers.

Regularization using Dropout and L2 penalty.

Output layer with sigmoid activation for binary classification.

Compilation & Training:
Optimizer: Adam

Loss Function: Binary Crossentropy

Metrics: Accuracy, Precision, Recall

Epochs: 30 (can be tuned further)

Handled overfitting using dropout and batch normalization.

 Evaluation:
Validated model performance on the validation dataset.

Tracked training/validation accuracy and loss using Matplotlib.

Observed potential overfitting; considered further tuning or dataset balancing.

Model Saving & Deployment:
Saved trained model using model.save().

 Problem Faced: Overfitting
During training, the model achieved very high accuracy on the training set, but significantly lower accuracy on the validation set. This indicated overfitting, where the model was learning patterns specific to the training data and not generalizing well to unseen data.

solution :  Hyperparameter Tuning
To overcome overfitting, I experimented with and adjusted various hyperparameters:

Dropout Rates: Increased dropout in convolutional and dense layers to reduce co-adaptation of neurons.

Regularization: Applied L2 kernel regularization in convolutional layers.

 Model Depth & Filters: Tuned the number of convolutional layers and filter sizes.

Learning Rate: Adjusted the learning rate for better convergence.

Epochs: Monitored training and validation performance across different epoch counts.

Batch Size: Tweaked batch size for better gradient updates.

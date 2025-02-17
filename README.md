UMESH CHANDRA KURUVA
700759482
1. Tensor Creation, Reshaping, and Broadcasting
•  Tensor Creation : A random tensor of shape (4, 6) is generated using tf.random.uniform(). Rank and shape are printed using TensorFlow functions.
•  Reshaping : The tensor is reshaped from (4, 6) to (2, 3, 4) using the tf.reshape() method.
•  Transposing : The reshaped tensor is transposed to (3, 2, 4) using the tf.transpose() method.
•  Broadcasting and Addition : A smaller tensor of shape (1, 4) is broadcasted to match the larger tensor and added element-wise.
•  Broadcasting Explanation : TensorFlow's broadcasting allows tensors with different shapes to operate together by expanding dimensions as needed.

2. Loss Functions & Hyperparameter Tuning

•  Overview : Implementation and comparison of Mean Squared Error (MSE) and Categorical Cross-Entropy (CCE) loss functions using TensorFlow. Visualization of how loss values change with different model predictions.
•  Steps Performed :
  -  Define True and Predicted Values : True labels (y_true) are one-hot encoded, and initial predictions (y_pred) are created for comparison.
  -  Compute Loss Functions :
    - Used tf.keras.losses.MeanSquaredError() to compute MSE.
    - Used tf.keras.losses.CategoricalCrossentropy() to compute CCE.
  -  Modified Predictions : Adjusted predictions slightly to observe the effect on loss values.
  -  Plot Loss Values : Visualized the loss function values for initial and modified predictions using a bar chart.

3. Train a Model with Different Optimizers: MNIST Dataset

•  Overview : Training two models on the MNIST dataset using Adam and SGD optimizers to compare training and validation accuracy trends.
•  Steps Performed :
  -  Data Loading and Preprocessing : Loaded MNIST dataset and normalized the images to [0, 1] range.
  -  Model Definition :
    - Input layer: Flattened 28×28 images.
    - Hidden layer: 128 units, ReLU activation.
    - Output layer: 10 units, Softmax activation.
  -  Training with Optimizers :
    - One model trained with Adam optimizer.
    - One model trained with SGD optimizer.
  -  Comparison of Accuracy : Plotted training accuracy and validation accuracy trends for both optimizers.

4. Train a Neural Network and Log to TensorBoard

•  Overview : Train a simple neural network on the MNIST dataset and log training and validation metrics to TensorBoard for analysis.
•  Steps Performed :
  -  Data Loading and Preprocessing : Loaded and normalized MNIST dataset.
  -  Model Definition :
    - Input layer: Flattened 28×28 images.
    - Hidden layer: 128 units, ReLU activation.
    - Output layer: 10 units, Softmax activation.
  -  TensorBoard Setup : Configured TensorBoard to log metrics during training.
  -  Model Training : Trained the model for 5 epochs using Adam optimizer and logged metrics.
  -  
5. Patterns in the Training and Validation Accuracy Curves

•  Training Accuracy Curve :
  - Generally increases steadily during the epochs.
  - May plateau after a certain point, especially as the model learns the most basic patterns.
•  Validation Accuracy Curve :
  - Typically follows the training curve but stays at a lower value.
  - If it diverges or plateaus while the training accuracy increases, this signals overfitting.
Using TensorBoard to Detect Overfitting
•  Training vs. Validation Curves :
  - Overfitting occurs when training accuracy increases, but validation accuracy plateaus or declines.
•  Training vs. Validation Loss Curves :
  - Overfitting is also indicated when training loss decreases, but validation loss stops decreasing or even increases.
What Happens When You Increase the Number of Epochs?
•  Training Behavior :
  - Initially, more epochs improve both training and validation accuracy.
  - After a certain point, training accuracy keeps increasing, but validation accuracy may not improve and could decline.
•  Generalization :
  - Too many epochs may lead to overfitting, where the model becomes too specialized for the training data and struggles with unseen data.
•  Impact on Loss :
  - Training loss continues to decrease, but validation loss may level off or increase, signaling overfitting.
Summary of Key Insights
•  Training and Validation Accuracy Curves :
  - Ideally, both curves should increase. If validation accuracy starts to decline while training accuracy rises, overfitting is occurring.
•  Overfitting Detection in TensorBoard :
  - Monitor both accuracy and loss curves. Divergence between training and validation curves signals overfitting.
•  Effect of Increasing Epochs :
  - Training for too many epochs can lead to overfitting. Training should be stopped when validation performance stops improving or declines.

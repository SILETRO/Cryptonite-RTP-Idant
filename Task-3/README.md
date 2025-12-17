## Wine Quality Dataset
### Preprocessing
- I normalised the data and label encoded the y values so that thy can be categorised easily.
- Sparse cross-entropy loss function was used to compute the costs in order to enable multiclassification of the wine qualiy.
- I created a neural network with 3 layers with each having 100 neurons.
### Evaluation
- It was able to achieve 57% accuracy.
- Precision of 55%
- Recall of 57%

## Income Classification Dataset
### Preprocessing
- Created a pipeline to impute and normalize the numerical values.
- Created a pipeline to impute and onehot encode the categorical values in the dataset.
### Model
- Created a 3 layered neural network with 100 neurons each.
- ReLU activation function was used in the hidden layers with He initialisation.
- Used L2 regularised to avoid overfitting of the data.
- Adam optimizer was used to adjust the learning rate.
### Evaluation

- Achieved accuracy of over 86%.
- Precision of 69%
- Recall of 73%

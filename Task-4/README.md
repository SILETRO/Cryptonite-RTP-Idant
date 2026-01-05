## Fashion MNIST Classification

### Model Architecture

A CNN was developed with the following specifications:

- **Convolutional Layers**: 3 layers with 3×3 kernels and 64 filters each
- **Activation**: ReLU with He normal initialization
- **Pooling**: MaxPooling layers after each convolutional block
- **Fully Connected Layers**: Two dense layers with 128 and 64 neurons respectively
- **Regularization**: Dropout (0.5) applied between fully connected layers
- **Training Strategy**: Early stopping to prevent overfitting

The architecture was kept shallow due to the simple 28×28 grayscale images in the Fashion MNIST dataset.
A deeper architecture would have increased the risk of overfitting without improving performance.

### Hyperparameter Optimization

Keras Tuner was used to find optimal hyperparameters. The tuning founded the best parameters to be:

- 2 convolutional layers (rather than 3)
- Dropout rate of 0.3

### Performance Metrics

| Metric | Score |
|--------|-------|
| Test Accuracy | 91.29% |
| Precision | 92% |
| Recall | 92% |
| F1-Score | 92% |

---

## DeepWeeds Classification

### Model Architecture

This project uses the pre-trained **ResNet50** architecture due to the complexity of the DeepWeeds dataset, which contains images with varying exposure, zoom levels, and orientations.
The small visual differences between weed species makes it necessary to use a deep CNN architecture.

**Implementation Details**:

- **Base Model**: ResNet50 (pre-trained on ImageNet)
- **Initial Training**: All ResNet50 layers frozen
- **Custom Layers**: Fully connected layers with 1,024 and 512 neurons
- **Activation**: ReLU with He normal initialization
- **Data Augmentation**: Applied to improve generalization and prevent overfitting
- **Training Strategy**: Early stopping monitoring

### Transfer Learning

After initial training achieved 70% validation accuracy, fine-tuning was performed by unfreezing the last 30 layers of ResNet50.
This resulted in major performance improvements.

### Performance Metrics

| Metric | Score |
|--------|-------|
| Test Accuracy | 89.6% |
| Precision | 90% |
| Recall | 90% |
| F1-Score | 90% |

---

## Facial Expression Recognition

### Model Architecture

The **EfficientNet-B0** architecture was selected for this task. This was because of the small image dimensions (48×48 pixels) in the FER dataset.
Deeper architectures like ResNet would have been likely to overfit and would have required extensive regularization.

**Implementation Details**:

- **Base Model**: EfficientNet-B0 (pre-trained on ImageNet)
- **Initial Training**: All EfficientNet-B0 layers frozen
- **Custom Layers**: Fully connected layers with 512 and 256 neurons
- **Activation**: ReLU with He normal initialization
- **Data Augmentation**: Applied to enhance model generalization
- **Training Strategy**: Early stopping monitoring

### Transfer Learning

Fine-tuning was performed by unfreezing the last 50 layers of EfficientNet-B0, which improved the test accuracy to 61%.

### Performance Metrics

| Metric | Score |
|--------|-------|
| Test Accuracy | 61% |
| Precision | 62% |
| Recall | 61% |
| F1-Score | 59% |

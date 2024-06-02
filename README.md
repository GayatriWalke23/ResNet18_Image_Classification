# ResNet Architecture Implementation
This project implements the ResNet-18 architecture for image classification using PyTorch. ResNet, short for Residual Network, introduced residual blocks to address the degradation problem in deep networks, where adding more layers led to higher training error.

## ResNet Architecture
The ResNet-18 architecture consists of the following key components:

- Input Layer: Accepts input images of size 224x224x3 (RGB images).
- Convolutional Layer 1: Uses a 7x7 kernel with a stride of 2 to reduce the spatial dimensions. The output is passed through batch normalization and a ReLU activation function.
- Max Pooling Layer: Applies max pooling with a 3x3 kernel and a stride of 2 to reduce the spatial dimensions further.
- Residual Blocks: Consist of multiple layers of basic blocks. Each basic block consists of two convolutional layers with batch normalization and ReLU activation. The first convolutional layer has a kernel size of 3x3, and the second convolutional layer has the same kernel size. Shortcut connections are used to skip one or more layers, helping to address the vanishing gradient problem.
- Global Average Pooling Layer: Reduces the spatial dimensions to 1x1, effectively converting each feature map into a single value.
- Fully Connected Layer: A linear layer that maps the features to the number of output classes. The output size is equal to the number of classes in the dataset.
- Output Layer: Uses a softmax activation function to produce class probabilities.

## Techniques Used
- Regularization: L2 regularization with a weight decay of 0.0001.
- Dropout: Dropout with a probability of 0.5.
- Early Stopping: Early stopping based on validation loss.
- Image Augmentation: Random horizontal flip and random crop.

### Results
- Without Optimization:
  - Validation Accuracy: 81.44%
  - Validation Loss: 0.4898
- With Optimization:
  - Validation Accuracy: 86.76%
  - Validation Loss: 0.3355
The optimized model shows significant improvements in validation accuracy and loss compared to the non-optimized model.

Conclusion
The implementation of the ResNet-18 architecture with optimization techniques has led to improved performance in image classification tasks. The model demonstrates better generalization and higher accuracy on unseen data, showcasing the effectiveness of ResNet architectures in deep learning applications.


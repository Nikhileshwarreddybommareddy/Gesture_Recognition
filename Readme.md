# Gesture Recognition Analysis by Nikhileshwar B

## Overview:

This project delves into the realm of gesture recognition, employing various models and techniques to achieve accurate classification. The primary focus was on optimizing accuracy and minimizing trainable parameters. The journey involved experimentation with different models and strategies to discern the most effective approach for gesture recognition.

## Project Highlights:

1. **Generator Function:** A dynamic generator function was developed, streamlining the entire image classification process and enabling seamless transitions between images.

2. **Library Initialization:** The project began by initializing essential libraries. However, a challenge arose with SciPy, limiting image reading capabilities to SciPy version 1.1.0.

3. **Image Reshaping:** Within the generator function, images were reshaped to a standardized size of (100,100) with RGB channels, ensuring consistency in input data.

4. **CSV Data Processing:** The generator function was bifurcated based on CSV column values, facilitating efficient handling of data with binary classifications (0 or 1).

5. **Model Iterations:**
    - **Base Model:** Utilized normal Conv 3D layers with Adam optimizer and ReLU activation function. Achieved a training accuracy of 0.78 and a validation accuracy of 0.28 within 3 epochs.
    - **Parameter Optimization:** Attempted to reduce parameters by adjusting dense layer input to 64. Although training accuracy improved, there was no impact on validation accuracy.
    - **Complexity Increase:** Added more Conv 3D layers, anticipating an improvement in validation accuracy. However, this led to increased trainable parameters and complexity without a significant validation accuracy change.
    - **Overfitting Mitigation:** Tried to reduce trainable parameters by setting dense layer neurons to 128. While this decreased parameters, overfitting became a concern, with no improvement in validation accuracy.
    - **Conv 2D with LSTM:** Implemented a model combining Conv 2D with LSTM, drastically reducing trainable parameters. This approach resulted in a steep increase in validation accuracy.
    - **Transfer Learning:** Employed transfer learning, leading to a substantial increase in validation accuracy, nearly tripling the performance. Training accuracy also demonstrated commendable results.

## Conclusion:

The project's evolution showcased the significance of model architecture and parameter optimization. Transfer learning emerged as the most effective approach, significantly enhancing validation accuracy. This journey provides valuable insights into gesture recognition methodologies and their nuances.

*Note: This README provides an overview of the project's process and outcomes. For detailed code and results, please refer to the complete project documentation.*
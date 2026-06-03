# Digit Recognizer

A convolutional neural network for classifying handwritten digits from the MNIST dataset.

## Kaggle Score: 0.99350

## Approach
- Exploratory data analysis — class distribution and image visualization
- Data augmentation — rotation, shifting, and zoom to improve robustness
- Three-layer CNN with feature extraction and classifier head
- Early stopping to prevent overfitting

## Key Findings
- Data augmentation causes validation accuracy to exceed training accuracy — expected behavior since training sees harder augmented images
- Three conv layers (32→64→128 filters) with two max pooling layers
- Converges well before the 50 epoch limit

## Architecture
- Conv2D(32) → MaxPool → Conv2D(64) → MaxPool → Conv2D(128) → Flatten → Dense(128) → Dropout(0.5) → Dense(10, softmax)

## Libraries
- TensorFlow/Keras, NumPy, pandas, matplotlib, scikit-learn

# PRODIGY_ML_04
# Hand Gesture Recognition with CNNs

This project builds a Convolutional Neural Network (CNN) model to classify hand gestures from the **Leap Gestural Recognition Dataset**. The model processes grayscale images of gestures, trains on a CNN to recognize the gesture type, and provides predictions.

## Data Preprocessing

1. **Image Loading**: The dataset is loaded from the specified directory structure, where each subfolder corresponds to a unique gesture class.
2. **Preprocessing**: Images are resized to 64x64 pixels, converted to grayscale, and normalized to a range of [0, 1]. The processed images are then stored in arrays for efficient access.
3. **Label Encoding**: Each gesture label is encoded into a numerical index, which helps the model to process class labels more efficiently.

## Model Architecture

The CNN model consists of the following layers:
- **Convolutional Layers**: These layers are used to capture spatial features from gesture images.
- **Pooling Layers**: Max-pooling layers are employed to reduce spatial dimensions, making the model less sensitive to image shifts and reducing computational load.
- **Dropout Layers**: Dropout is applied to prevent overfitting by randomly dropping neurons during training.
- **Fully Connected Layers**: These dense layers allow the model to learn complex relationships and finalize gesture classification.

## Training

The model is compiled with the **Adam optimizer** and trained using **sparse categorical cross-entropy loss**. The model is trained over a set number of epochs with validation data, and both training and validation accuracy/loss are tracked to monitor progress. 

## Evaluation

After training, the model is evaluated on the test set. Key metrics such as accuracy and loss are printed, and performance over time is visualized in accuracy and loss plots.

## Random Prediction Display

For visual inspection, random test images are selected, and the model’s predictions are compared to true labels. This provides insight into the model's performance in real-world scenarios.

## Usage

Running the script performs the following steps:
1. Loads and preprocesses the data.
2. Builds and trains the CNN model.
3. Evaluates the model and plots accuracy/loss metrics.
4. Displays random test images with predicted and true labels for performance validation.




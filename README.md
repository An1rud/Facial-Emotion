# Facial Emotion Recognition

This project implements a Convolutional Neural Network (CNN) for emotion recognition using the FER2013 dataset. The model is built using Keras and trained to recognize emotions such as Angry, Disgust, Fear, Happy, Neutral, Sad, and Surprise.

## Dataset
The FER2013 dataset consists of 48x48 pixel grayscale images of faces annotated with one of seven emotions.

### Data Preprocessing
- Images are preprocessed using Keras' `ImageDataGenerator` with the following augmentations:
  - Rescaled to a range of [0, 1]
  - Random rotation (30 degrees)
  - Shear range of 0.3
  - Zoom range of 0.3
  - Horizontal flipping
  - Nearest fill mode
- Training and validation data are loaded using `flow_from_directory` from directories `data/train/` and `data/test/`.

## Model Architecture
The CNN model architecture consists of several Conv2D layers followed by MaxPooling, Dropout for regularization, and Dense layers.
- Input shape: (48, 48, 1)
- Output classes: 7 (corresponding to the 7 emotions)

## Training
The model is compiled using 'categorical_crossentropy' loss and 'adam' optimizer.
- Batch size: 32
- Number of epochs: 30

## Results
- The model achieves an accuracy of 79% on the validation set.



# How to Use

## Clone this repository:
```bash
git clone https://github.com/your-username/emotion-recognition-cnn.git
```
## Install the required dependencies:
```bash
pip install -r requirements.txt
```


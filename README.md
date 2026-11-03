# Waste Classification Using CNN and Transfer Learning

## Project Overview
This project uses deep learning to classify waste images into six categories. It uses MobileNetV2 with transfer learning to recognize different types of waste.

## Waste Categories
- Cardboard
- Glass
- Metal
- Paper
- Plastic
- Trash

## Technologies Used
- Python
- TensorFlow / Keras
- MobileNetV2
- CNN
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Model Architecture
The project uses MobileNetV2 pretrained on ImageNet as a feature extractor. A custom classification head is added with:
- Global Average Pooling
- Dropout
- Dense output layer with six classes and Softmax activation

The model is initially trained with the pretrained layers frozen, followed by fine-tuning selected layers.

## Dataset
The dataset contains images belonging to six waste categories. Images are resized to 224 × 224 pixels for model training.

## Model Performance
Initial validation accuracy: 70.86%

Fine-tuned validation accuracy: 76.47%

Test accuracy: 76.04% (from model.evaluate)

Classification report accuracy: 78% (prediction pass; verify against the same test examples before treating this as the final result).

## Project Structure
```text
Waste_Classification_Project/
├── notebooks/
│   └── main.ipynb
├── models/
│   └── waste_classifier_mobilenetv2.keras
├── results/
│   ├── confusion_matrix.png
│   └── training_history.png
└── README.md
```

## How to Use
1. Open the notebook in Google Colab.
2. Mount Google Drive.
3. Set the project directory.
4. Load the saved Keras model.
5. Upload a waste image.
6. Run the prediction cells to obtain the predicted category.

## Limitations
- Performance varies between waste categories.
- The trash category has lower recall than the other categories.
- Predictions depend on image quality and similarity to the training dataset.

## Future Improvements
- Add more diverse images, especially for the trash category.
- Improve class balance.
- Experiment with data augmentation.
- Evaluate performance on a larger independent dataset.

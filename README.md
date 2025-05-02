# Technical Task for Machine Learning Intern Position – Accelx

A technical task (Dog vs Cat Classification) for "Machine Learning Intern" position. Here, I have build a custom CNN classification model on the Dogs vs. Cats dataset. 

## Dataset

The dataset used for training and evaluation is "Cats-vs-Dogs Datasett" available on Kaggle. You can find the dataset <a href="https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset">here</a>.

## Proposed Methodology
Here, I have used 4 convolutional block. In each block, there are 2 Conv2D layer, 2 BatchNormalization layer, 2 MaxPooling2D Layer and one Dropout layer. After using Flatten layer to converts the multidimensional feature maps into a 1D vector to make it suitable for dense layers, there are 2 Dense, BatchNormalization, and Dropout layers each. Lastly, a dense layer used to activate softmax activation function which assigns probabilities and classifies the input data into 2 classes.

## Experimental Setups
    
### Anaconda with VSCode
- **Environment:**
  - Python Version: 3.6.13 
  - Tensforflow Version: 2.6.2
  - Keras Version: 2.6.0
  - Processor: Intel i5 13400F
  - GPU: NVIDIA GeForce RTX 3060 (12 GB)
  - RAM: 16 GB
  - Storage: 512 GB NVMe SSD + 1 TB HDD
    

## Results
### Performance Evaluation of CNN Classification Model for Brain MRI Dataset

| Model | Accuracy | Precision | Recall  | F1 Score |
|-------|----------|-----------|---------|----------|
| CNN   | 0.95718  |  0.95711  | 0.95721 | 0.95715  |

## Model Performance Analization and Solution
- Based on the Training and Validation Loss and Accuracy Curves, this model is likely have some overfitting issues. Because,
  - There is a clear gap between training and validation performance (both in accuracy and loss).
  - Training performance keeps improving while validation stops improving after a certain point.

- Proposed Solutions to Reduce Overfitting:
  - Hyperparameter Tuning
  - Modification of the CNN Architecture
  - Early Stopping, to stop training by monitoring validation Loss and when it stops improving to prevent over-training
  - Data Augmentation Techniques
  - K-fold cross-validation to ensure model is not overfitting to a specific split

The model was trained using the Adam optimizer with an initial learning rate of 0.001. A dynamic learning rate scheduler (ReduceLROnPlateau) was applied, reducing the rate by a factor of 0.5 upon stagnation of validation accuracy for 2 epochs, with a lower bound of 1e-5.
This is a solution to optimize convergence and avoid some overfitting while dynamically adjusting learning rate.

## Contact Information

- **Shamim Rahim Refat**
  - Email: [n.a.refat2000@gmail.com](mailto:n.a.refat2000@gmail.com)

# Fashion-MNIST Image Classification

A deep learning project that implements a Convolutional Neural Network (CNN) to classify Fashion-MNIST images into 10 different clothing categories.

## Dataset

The Fashion-MNIST dataset consists of 70,000 grayscale images of clothing items:
- **Training Set**: 60,000 images
- **Test Set**: 10,000 images
- **Image Size**: 28x28 pixels
- **Classes**: 10 clothing categories

### Classes
1. T-shirt/top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle boot

## Model Architecture

The CNN classifier consists of:
- **2 Convolutional Blocks**
  - Conv2D → ReLU → Conv2D → ReLU → MaxPool2D
- **Fully Connected Classifier**
  - Flatten → Linear layer

**Total Parameters**: ~7,850



## Project Structure

```
fashion-mnist-classifier/
│
├── Fashion-MNIST_Complete.ipynb    
│
├── models/                          
│   ├── fashion_mnist_best_model.pth
│   └── fashion_mnist_final_model.pth
│
├── outputs/                        
│   ├── visualizations/             
│   │   ├── class_distribution.png
│   │   ├── sample_images.png
│   │   ├── training_history.png
│   │   ├── confusion_matrix.png
│   │   ├── sample_predictions.png
│   │   └── per_class_accuracy.png
│   └── classification_report.txt   
│
├── data/                           
│   └── FashionMNIST/
│
├── README.md                    
├── requirements.txt              
└── .gitignore                      
```

## Usage

### Training the Model

Open and run the Jupyter notebook:

```bash
jupyter notebook Fashion-MNIST_Complete.ipynb
```

Run all cells sequentially to:
1. Load and explore the dataset
2. Create data loaders
3. Define and initialize the model
4. Train the model (10 epochs by default)
5. Generate visualizations and evaluation metrics

### Model Performance

- **Training Accuracy**: ~95-96%
- **Test Accuracy**: ~90-91%
- **Best Model**: Automatically saved during training


## Results

### Training Progress
The model shows steady improvement over 10 epochs with minimal overfitting.

### Confusion Matrix
Shows strong classification performance across all categories with some confusion between similar items (e.g., T-shirt vs Shirt, Pullover vs Coat).

### Per-Class Accuracy
- Best performing: Trousers, Bags, Ankle boots (>90%)
- Most challenging: Shirts, T-shirts, Pullovers (80-85%)

## Key Features

- ✅ Complete data exploration and visualization
- ✅ CNN architecture with multiple convolutional layers
- ✅ Training with progress tracking
- ✅ Automatic best model checkpointing
- ✅ Comprehensive evaluation metrics
- ✅ Confusion matrix analysis
- ✅ Per-class accuracy breakdown
- ✅ Sample prediction visualization
- ✅ Organized output structure

## Customization

### Adjusting Hyperparameters

```python
# In the notebook, modify these values:
BATCH_SIZE = 32          # Batch size for training
epochs = 10              # Number of training epochs
learning_rate = 0.001    # Adam optimizer learning rate
hidden_units = 10        # Number of hidden units in conv layers
```

### Training for More Epochs

Simply change the `epochs` variable in the training loop cell.

## Visualizations

All visualizations are automatically saved to `outputs/visualizations/`:

1. **Class Distribution** - Bar chart showing data balance
2. **Sample Images** - Grid of random training samples
3. **Training History** - Loss and accuracy curves
4. **Confusion Matrix** - Heatmap of predictions vs true labels
5. **Sample Predictions** - 16 test predictions with confidence scores
6. **Per-Class Accuracy** - Color-coded accuracy by category


### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/fashion-mnist-classifier.git
cd fashion-mnist-classifier
```

2. Install required packages
```bash
pip install -r requirements.txt
```

# car_detection
Cardetection is a comprehensive car classification system built using PyTorch that can identify various car makes and models from images**(including Iranian cars)**.
Reaching over 90% accuracy.
# Description
Cardetection is a comprehensive car classification system built using PyTorch that can identify various car makes and models from images. The project integrates two distinct datasets:
- **Stanford Car Dataset** - A widely-used academic dataset with diverse car makes and models
- **Iran Used Cars Dataset** - A regional dataset providing additional diversity

### Key features of this project:
- Custom dataset integration with unified class mapping
- Pre-trained ResNet18-based model fine-tuned for car classification
- Extensive data augmentation pipeline
- Comprehensive evaluation metrics
- Interactive prediction functionality


## Technical Details
- **Architecture**: ResNet18 with modified classification head
- **Input Size**: 400x400 RGB images
- **Optimization**: SGD with momentum and learning rate scheduling
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score
- **Early Stopping**: Implemented to prevent overfitting

## Performance metrics

![output](https://github.com/user-attachments/assets/9c719b98-ce05-42f3-8fc3-9401f9202be7)

## Installation
# Clone the repository
```
git clone https://github.com/Amirreza-al/car_detection.git
cd car_detection
```

# Install dependencies
```
pip install torch torchvision matplotlib numpy tqdm scikit-learn kagglehub torchsummary
```

## Usage
### Dataset Preparation
The project expects data to be organized in the following structure:
```
dataset1_dir/
├── train/
│   ├── class1/
│   │   └── images...
│   ├── class2/
│   │   └── images...
└── test/
    ├── class1/
    │   └── images...
    ├── class2/
    │   └── images...

dataset2_dir/
├── train/
│   ├── class1/
│   │   └── images...
│   ├── class2/
│   │   └── images...
└── test/
    ├── class1/
    │   └── images...
    ├── class2/
    │   └── images...
```
### Running the Notebook
1- Open the Jupyter notebook:
 ```
jupyter lab car-detection.ipynb
```
2- Execute the cells in order to:
    - Load and prepare the datasets
    - Initialize and train the model
    - Evaluate model performance
    - Make predictions on test images

## Making Predictions
To classify a car image, use the ```pred_car``` function:
```
pred_car(model, dataset=1, image_path='path/to/car/image.jpg')
```
## Features
- Dataset Integration: Seamlessly combines multiple datasets with different class structures
- Data Augmentation: Implements resize, random horizontal flip, and rotation transformations
- Transfer Learning: Builds on ResNet18 pre-trained on ImageNet
- Performance Monitoring: Tracks accuracy, precision, recall, and F1-score for both training and validation
- Early Stopping: Prevents overfitting by monitoring validation loss
- Learning Rate Scheduling: Adjusts learning rate based on model performance
- Visualization Tools: Provides functions to visualize sample images and training metrics

# Contributing
Contributions to improve Cardetection are welcome! Here’s how you can contribute:
1-Fork the repository
2-Create your feature branch ```(git checkout -b feature/amazing-feature)```
3-Commit your changes ```(git commit -m 'Add some amazing feature')```
4-Push to the branch ```(git push origin feature/amazing-feature)```
5-Open a Pull Request

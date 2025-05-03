# car_detection
Cardetection is a comprehensive car classification system built using PyTorch that can identify various car makes and models from images(including Iranian cars).
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

## Performance metrics

![output](https://github.com/user-attachments/assets/9c719b98-ce05-42f3-8fc3-9401f9202be7)

## Installation
# Clone the repository
git clone https://github.com/Amirreza-al/car_detection.git
cd car_detection

# Install dependencies
pip install torch torchvision matplotlib numpy tqdm scikit-learn kagglehub torchsummary

## Usage
### Dataset Preparation
The project expects data to be organized in the following structure:

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

### Training the Model
# Set up paths to your datasets
dataset1_dir = 'path/to/stanford_car_dataset'
dataset2_dir = 'path/to/iran_used_cars_dataset'

run the training code

## Making Predictions
Once your model is trained, you can use the pred_car function to make predictions on new images:

pred_car(model, dataset=1, image_path='path/to/car/image.jpg')

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
  2-Create a new branch (git checkout -b feature-branch)
  3-Make your changes
  4-Commit your changes (git commit -m 'Add some feature')
  5-Push to the branch (git push origin feature-branch)
  6-Open a Pull Request

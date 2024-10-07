# Pre-trained-CNN-Models-Evaluation-for-Dog-Breeds-Classification
This project evaluates the performance of three pre-trained Convolutional Neural Network (CNN) architectures (VGG, AlexNet, and ResNet) for classifying dog breeds. Using transfer learning, the models were fine-tuned to identify whether the pet image is of a dog and, if so, classify the dog's breed. The goal was to determine which architecture performs best in both tasks: distinguishing dogs from non-dogs and accurately classifying dog breeds. The models' performances are compared through metrics such as the percentage of correctly classified dogs and dog breeds.

The task not only demonstrates skills in model selection but also in applying evaluation metrics to assess classification quality. This project is part of an AI programming course and uses Python for evaluating these models. Batch processing options are also available for users who want to compare the performance of all models in one go.

# Project Overview
This project is part of an AI programming course and aims to evaluate a classifier that can:

1. Identify which pet images are dogs and which are not dogs.
2. Classify the breed of the dog for images that are of dogs.
   
The classifier is trained using transfer learning with the three CNN architectures, and their performance is compared based on two primary objectives:

- Correct identification of dogs and non-dogs.
- Correct classification of dog breeds.

## Model Architectures
Three CNN architectures are used in this project:

**ResNet:** Known for its ability to deal with very deep networks without vanishing gradients.

**AlexNet:** One of the pioneering deep learning models for image classification.

**VGG:** A deep network that is computationally more expensive but often yields higher accuracy for specific tasks.

## How to Use
### Prerequisites
Python 3.x

You can run the classification script using any of the three pre-trained models. The output includes performance metrics, including the percentage of correctly classified dog images and breeds.

### Running the Classification
To run the classifier with any of the available models, use the following command:
```
python check_images.py --dir <path-to-image-folder> --arch <model-architecture> --dogfile dognames.txt
```
**< path-to-image-folder >:** The directory containing the images you want to classify.

**< model-architecture >:** The CNN architecture to use (resnet, alexnet, or vgg).

**dognames.txt:** The file containing a list of valid dog breeds.

### Example Usage
```
python check_images.py --dir pet_images/ --arch resnet --dogfile dognames.txt
```

### Batch Processing
If you'd like to compare the performance of all three models at once, you can run the provided batch script:

**Unix/Linux/OSX**
```
./run_models_batch.sh
```
**Windows**
```
run_models_batch.bat
```

## Results
For each model, the following metrics were calculated:

- Percentage of Correctly Classified Dogs (pct_correct_dogs)
- Percentage of Correctly Classified Breeds (pct_correct_breed)
- Overall Match Percentage (pct_match)

| Model Architecture | % Correct Dogs | % Correct Breeds | % Match |
|--------------------|----------------|------------------|---------|
| ResNet             | 100.0%         | 90.0%            | 82.5%   |
| AlexNet            | 100.0%         | 80.0%            | 75.0%   |
| VGG                | 100.0%         | 93.3%            | 87.5%   |

The best performing model is VGG, which correctly classified both dogs and dog breeds with the highest accuracy.


## Files and Folders
**check_images.py:** Runs the classification on the provided dataset using one of the three CNN architectures.

**run_models_batch.sh:** Runs the classification for all three models in batch.

**print_results.py:** Provides the results summary and printouts for misclassified dogs and breeds.

**pet_images** Directory containing the pet images to be classified.

**dognames.txt:** File containing a list of dog breed names for classification.

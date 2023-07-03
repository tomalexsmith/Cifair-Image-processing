# Cifair Image processing

### Conducting Comparative Analysis of CNN Architectures Trained on the CiFair10 Dataset

This GitHub repository presents a study that focuses on comparing the performance and results obtained from various popular Convolutional Neural Network (CNN) architectures, including AlexNet, LeNet, and VGGNet. Through training these architectures on the CiFair10 dataset, this project aims to provide insights into their respective strengths and weaknesses. 

By leveraging the results obtained from evaluating and comparing existing architectures, this project introduces a custom CNN model that strives to outperform the initial architectures. With the goal of achieving superior results, this research-driven development enhances the capabilities of CNNs for specific tasks.

Github Repository: https://github.com/tomalexsmith/Cifair-Image-processing

## Description of the algorithm 

This project begins by importing the cifair10 dataset, which is then split into training, testing, and validation data. Both the images and their corresponding classification labels are divided using an 80-10-10 split ratio. The code further ensures the accuracy of data import by displaying a set of 10 random images from each of the 10 classes. This visualisation step offers a valuable opportunity to observe the dataset's content and structure prior to initiating the training process, with the displayed images dynamically changing each time the code is executed.

### Preprocessing

To ensure successful training of the CNN models on the dataset, a crucial step involved data pre-processing. In this particular case, functions were developed that streamlined the necessary operations. These functions enabled essential pre-processing steps such as one-hot encoding of the image labels, as well as pixel normalisation, batching, and shuffling on the ciFair dataset. By implementing these pre-processing techniques, the data was appropriately formatted and optimised to enhance the training process, improving the overall performance and accuracy of the CNN models.

### Defining CNN Architectures

The initial CNN architecture chosen for implementation using Keras was AlexNet. This popular architecture was trained utilising the output data from the pre-processing functions, including training and testing datasets. Once AlexNet was successfully implemented and trained, the project progressed by defining a custom CNN architecture. This custom model was built upon the foundation of AlexNet, incorporating modifications to hyperparameters and introducing additional layers. These enhancements aimed to optimise and improve the performance of the model, fine-tuning it to better suit the specific requirements of the project at hand.

The improvements made include:
- Reducing the kernel size and stride of the first convolution layer, allows for smaller details
and patterns to be captured from the 32x32 images.
- Decreased number of filters in the convolution layers increases computational efficiency and
reduces the chance of overfitting, with a negligible model performance penalty due to the
small input size.
- Batch normalisation layers after each convolution and dense layer improves the stability and
performance of the CNN.
Thomas Smith – Student ID: 200359423
Body word count (Excluding figures and references): 1096
Maximum word count: 1000 +/- 10% (1100)
- Decreased batch size, whilst making the training process slower due to being
computationally expensive, improves model’s generalisation capability.
- Adding a sixth convolution and subsampling layer improves the model’s ability to identify
features and patterns in the training data.
- Increasing the number of epochs increases the number of times the model is trained on the
training data, increasing performance.
- The loss function was changed to ‘sparse_categorical_crossentropy’, as eliminating the need
for one-hot encoding is more computationally efficient.
- Plateau-based learning rate decay increases the performance of the model in the case of the
loss plateauing.

Following the initial implementation of AlexNet, two additional standard CNN architectures, namely LeNet and VGGNet, were implemented using Keras. These architectures served as benchmarks for comparing their performance against the custom CNN architecture developed earlier. To assess the performance of all four models (AlexNet, VGGNet, LeNet, and the custom CNN), dedicated functions were created.

The first function generated two comprehensive graphs, visualizing the training and testing accuracy, as well as the training and testing loss, across different epochs for a given CNN model. This aided in monitoring and analysing the model's training progress. A second function was designed to provide predictions for individual images. By inputting a single image and a CNN model, the function displayed the image along with the model's predicted label, accompanied by an indication of correctness.

### Architecture comparison

To facilitate a thorough comparison, three additional functions were developed. These functions produced informative graphs, including a bar chart, line chart, and confusion matrix, which effectively illustrated and compared the performance of my custom CNN architecture to that of AlexNet, LeNet, and VGGNet. By leveraging these functions, this project aimed to comprehensively evaluate and compare the performance of various CNN architectures, enabling a deeper understanding of their strengths, weaknesses, and overall effectiveness in image classification tasks.

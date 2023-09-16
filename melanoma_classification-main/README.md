# Melanoma Detection Assignment

## Problem statement

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion
 
Please download the Ipython notebook from [here](https://github.com/ContentUpgrad/Convolutional-Neural-Networks/blob/main/Melanoma%20Detection%20Assignment/Starter_code_Assignment_CNN_Skin_Cancer%20(1).ipynb).


## Importing neccessary libraries


**pathlib:** Imported for managing file paths and directories.

**tensorflow (tf):** TensorFlow library, used for deep learning tasks.

**matplotlib.pyplot (plt):**Matplotlib's pyplot module, utilized for creating visualizations.

**numpy (np):** Numpy library, employed for numerical operations and array handling.

**pandas (pd):** Pandas library, used for data manipulation and analysis.

**os:** Python's os module, employed for interacting with the operating system.

**PIL:** Python Imaging Library, used for image processing.

**keras:** Keras, an API provided by TensorFlow for building and training 
neural networks.

**layers:** Keras' layers module, used for building layers in a neural network.

**Sequential:** Sequential class from Keras' models module, used for creating sequential models.

# Initial Situation:

To rectify the problem of imbalanced classes, you can employ a Python package called Augmentor (https://augmentor.readthedocs.io/en/master/). This approach entails generating additional samples across all classes to ensure that no class is underrepresented.

# Identify the Least Sampled Class:

The class "Seborrheic keratosis" has the fewest number of samples, and it is closely followed by "Actinic Keratosis."

# Identify Dominant Classes:

The class "Pigmented benign keratosis" takes the lead in terms of the number of samples in the training set, surpassing a count of 100.

Here's how you can implement these steps using the Augmentor package:

# Resolve Class Imbalance:

To rectify the issue of imbalanced classes, you can leverage the Augmentor package. Its purpose is to increase the number of samples in all classes uniformly, ensuring that each class has a sufficient representation.

# Identify Classes with Few Samples:

Through examination, it is evident that the class "Seborrheic keratosis" has the lowest number of samples, and "Actinic Keratosis" follows closely behind.

# Spot Dominant Classes:

In terms of the proportionate number of samples, the class "Pigmented benign keratosis" emerges as the dominant one. It possesses a count exceeding 100 instances in the training dataset.

# Effect on Overfitting/Underfitting:

- With 50 epochs, you observed that validation accuracy improved, and the gap between training and validation accuracy reduced. This indicates that the rebalanced dataset helped mitigate overfitting and underfitting issues.

- In conclusion, rebalancing the dataset through augmentation improved the validation accuracy, and various epoch and dropout combinations were experimented with to achieve better results.

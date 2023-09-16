# Gesture Recognition Using TensorFlow

## Problem Statement

Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote. Let's have professor Raghavan introduce you to the problem statement:

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

- Thumbs up:  Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards 10 seconds
- Right swipe: 'Jump' forward 10 seconds  
- Stop: Pause the movie


## Generator
This is a crucial section of the code where we focus on the generator's functionality. In this generator, we have a few essential tasks:

**Image Preprocessing**:

 Since we're dealing with images of two different dimensions, we need to implement image preprocessing. This means adjusting parameters like img_idx, y, and z to ensure that our images are prepared correctly before feeding them into the model. The exact values of these parameters will likely require experimentation to optimize for the best results.

**Batch Creation**:

 The generator also needs to create batches of video frames. This involves selecting the appropriate batch size and organizing the frames in a way that the model can process effectively.

**Normalization**:

 Normalization of the data is a key step in preparing it for training. Experimentation may be needed to determine the best method and values for normalizing the input data to achieve high accuracy.

In summary, this part of the code is about fine-tuning the generator's settings, including image preprocessing, batch creation, and data normalization, to optimize the model's accuracy. It involves a process of trial and error to find the most effective configurations for your specific dataset and model architecture.



## Model


In this part of the code, we're tasked with building the model using various functionalities that Keras offers, with a particular focus on designing it for memory-efficient operation. Here are the key instructions:

**3D Convolutional Model** (Conv3D and MaxPooling3D): We're required to use 3D convolution layers (Conv3D) and 3D max-pooling layers (MaxPooling3D) for our model. These layers are essential for processing spatial and temporal information in three-dimensional data, such as video frames.

**Conv2D+**  RNN Model with TimeDistributed: Alternatively, we may need to build a model that combines 2D convolution (Conv2D) layers with Recurrent Neural Network (RNN) layers, possibly using the TimeDistributed wrapper. This design can be effective for sequence data like videos, where spatial features are processed by Conv2D layers, and temporal dependencies are captured by RNN layers.

**Final Layer as Softmax:** The last layer of the model should be a softmax activation layer. This is typically used for classification tasks to produce probability distributions over the different classes.

**Memory-Efficient Design**: The critical challenge is to design the model in a way that it achieves good accuracy while using the fewest parameters possible. The goal is to make the model compact enough to fit within the memory constraints of the webcam.

Achieving this balance between model performance and memory usage often requires experimentation and optimization. You might need to adjust the number of layers, the size of convolutional kernels, the number of filters, and other architectural aspects. Techniques like model pruning, quantization, and knowledge distillation can also be considered to reduce the model size.

Overall, this section of the code involves careful architectural choices and experimentation to create a model that provides good accuracy while remaining memory-efficient enough to operate within the constraints of the webcam's memory.

In this update from the training process, we can observe the following:

- During the 30th epoch of training, a learning rate adjustment took place. The learning rate was reduced to a very small value, approximately 4.096e-12. This adjustment is often triggered by a learning rate scheduling strategy, like ReduceLROnPlateau, which dynamically adjusts the learning rate during training to help the model converge more effectively.

- The training process involved 11 batches or steps. Each step took around 29 seconds to complete.

- The training loss at this point was 0.0147, indicating how well the model is fitting the training data. Lower values are generally better.

- The categorical accuracy on the training data was 99.47%, which signifies the percentage of correctly classified samples in the training set.

- The validation loss was 0.1376, which measures the model's performance on a separate validation dataset. It's important to monitor this value to check for overfitting, where the model performs well on the training data but not on unseen data.

- The validation categorical accuracy was 100%, indicating perfect accuracy on the validation dataset.

- The learning rate (lr) used in this epoch was 2.0480e-11.

These metrics provide insights into the training progress and the model's performance. The reduction in the learning rate suggests that the model might be converging slowly or encountering difficulties, and the training and validation metrics help assess its overall effectiveness.
# Happy-Sad-Face-Recognition-using-CNN
This a implementation of CNN for classification of happy or sad person. This model is mainly build on tensorflow and a very basic preprocessing has been done before implementing the Neural Network.

The Dataset contains two folder namely happy and sad containing images of happy and sad persons. This dataset has been created by myself by downloading stock images from Google and using the Chrome extensiion : https://chromewebstore.google.com/detail/download-all-images/ifipmflagepipjokmbdecpmjbibjnakm?hl=en 

Also a brief look for the loss and accuracy can be given as 
![ACC](https://github.com/vihaaaaan17/Happy-Sad-Face-Recognition-using-CNN/assets/138303144/616b9cc6-e2e0-477a-8b85-e8a392b71ead)
![LOSS](https://github.com/vihaaaaan17/Happy-Sad-Face-Recognition-using-CNN/assets/138303144/336eac75-97c5-466d-a388-109659a05a48)


Input Layer:
The input layer defines the shape of the input data. In this case, it expects images with a resolution of 256x256 pixels and 3 color channels (RGB), which is a common input size for image classification tasks.

Convolutional Layers:
Convolutional layers are responsible for detecting various features in the input images. Each convolutional layer applies a set of filters (also known as kernels) to the input image, performing convolution operations.
In this model, the first convolutional layer has 16 filters of size 3x3. These filters learn to detect low-level features like edges, textures, and patterns in the input images. The ReLU activation function is applied after the convolution operation to introduce non-linearity to the model.
The subsequent convolutional layers (e.g., the second convolutional layer with 32 filters and the third convolutional layer with 16 filters) typically learn higher-level features by combining lower-level features learned in previous layers.

MaxPooling Layers:
MaxPooling layers are used to reduce the spatial dimensions of the feature maps obtained from the convolutional layers, while retaining the most important information. This helps in reducing computational complexity and controlling overfitting.
In this model, MaxPooling layers with default settings (typically 2x2 pooling size with a stride of 2) are used after each convolutional layer to downsample the feature maps.

Flatten Layer:
The Flatten layer serves as a bridge between the convolutional layers and the fully connected (Dense) layers. It converts the 2D feature maps obtained from the last convolutional layer into a 1D vector, which can be fed into the dense layers for classification.

Dense Layers:
Dense layers (also known as fully connected layers) are used for classification based on the extracted features. Each neuron in a dense layer is connected to every neuron in the previous layer.
In this model, there is a dense layer with 256 neurons and ReLU activation function. This layer helps in learning complex patterns and relationships in the feature representations.
Output Layer:

The output layer produces the final predictions of the model. Since it's a binary classification task (happy or sad face recognition), a single neuron with a sigmoid activation function is used.
The sigmoid activation function squashes the output between 0 and 1, representing the probability of the input image belonging to the positive class (e.g., happy face).


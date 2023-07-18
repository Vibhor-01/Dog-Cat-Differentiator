# Dog-Cat-Differentiator
This is a Dog/Cat Differentiator Project using Tensorflow in Deep learning.

Link for DataSet: https://drive.google.com/drive/folders/1mWrX9nMewW0CJvMMli4OKAithfbzHPYl?usp=drive_link

The project is based on Convolutional neural networks, and uses Tensorflow for creating and training the Deep Learning Model. The Tensorflow used here is 2.12.0. The Project uses 2 dataset folder which has one folder containing the photos of a DOG and the second folder containing the Photos of a CAT.

The data is split into two folders containing Training and Test set, both of the folders contain the images of DOGs and CATs. The dataset are imported into the jupyter notebook using ImageDataGenerator and rescaled to 1./255, shear_range of 0.2 and zoom_range of 0.2, along with a horizontal flip. The training dataset on the other hand does not require any sort of Horizontal flip, or shear_range change, as our model should be able to tell whether it is a photo of a DOG or a CAT. It is however, recaled to 1./255.

The Deep learning model contains 6 layers, out of which 4 are Convolution layers and MaxPool layers, which performs MAXPooling. The MAXPool layers has a pool size of 2 and a stride of 2. While the Convolution layers has 32 filters, has a kernel_size of 3, and an activation function of 'relu'.

The 2 neuron layer has 128 and 1 unit of neuron respectively, and have activation function relu and sigmoid. The ANN is compiled using adam optimizer to perform stochastic gradient descent, and has binary_crossentropy as the loss fucntion estimation. The model is trained on 25 epochs.

To predict whether the image is of a dog or a cat, the image is first loaded into jupyter notebook and is then converted to an array. The results, are then predicted using predict() function and are distinguished using if/else statement.

if the prediction's probability value is greater than 0.5 then the prediction is a DOG and if it isn't then it is a CAT.

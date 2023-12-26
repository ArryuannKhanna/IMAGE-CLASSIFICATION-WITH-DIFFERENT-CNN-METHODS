## IMAGE CLASSIFICATION WITH DIFFERENT CNN METHODS

Image classification is a fundamental task in computer vision that involves the categorization of images into predefined classes or labels. The goal is to develop algorithms and models capable of recognizing and assigning appropriate labels to images based on their visual content. This process is crucial for a wide range of applications, including object recognition, medical imaging, autonomous vehicles, and more. In image classification, machine learning models, particularly convolutional neural networks (CNNs), have proven to be highly effective. These models learn hierarchical features from the input images, enabling them to distinguish patterns and characteristics essential for accurate classification. The training process involves providing the model with labeled images, allowing it to adjust its internal parameters to make predictions. Image classification plays a pivotal role in enhancing automation, enabling systems to interpret and respond to visual information, ultimately contributing to advancements in various fields.

We could leverage the use of following three methods to solve the issues-

### ARTIFICIAL NEURAL NETWORKS
Artificial Neural Networks (ANNs) are computational models inspired by the structure and functioning of the human brain. Comprising interconnected nodes, or neurons, organized into layers, ANNs process information through a series of weighted connections that allow them to learn and make predictions. The input layer receives data, which is then transmitted through hidden layers where computations occur, ultimately leading to an output layer that produces the network's prediction or classification. Training ANNs involves adjusting the weights of connections based on the error between predicted and actual outcomes, optimizing the network's performance. <br>
Herein if we think about the fundamental issue in our hands is how we are supposed to represent the image as data? An obvious answer is use of rgb channels of pixels i.e. each pixel of an image has 3 colour channels to give it a characteristic colour and they are represented by numbers in between 0 and 255. So we could use the matrix of height * width * 3 dimensions to characterise an image.We ofcourse need to do a matrix flattening as the ANN cant accept the input of this format. <br>
ANN has certain flaws i.e. it doesnt perform well when some augmentation is done to the picture (if an object is upside down or zoomed in).

### CONVULUTIONAL NEURAL NETWORKS
Convolutional Neural Networks (CNNs) represent a specialized class of artificial neural networks designed for processing and analyzing structured grid data, such as images. What distinguishes CNNs is their ability to automatically and adaptively learn hierarchical features through the application of convolutional operations. This architecture is particularly well-suited for tasks like image recognition, object detection, and computer vision. CNNs consist of layers like convolutional layers, pooling layers, and fully connected layers, enabling them to efficiently capture local patterns and spatial dependencies within the input data. 
Herein we use concepts of convolution,relu activation and pooling to leverage usage of the convulution layer.

We then use data augmentation for even better performance.

### TRNSFER LEARNING
Transfer learning is a machine learning technique that leverages knowledge gained from solving one task and applies it to a different but related task. Instead of training a model from scratch for a specific target task, transfer learning utilizes pre-trained models on a source task, allowing the model to transfer its learned features, representations, or knowledge to the new task. This approach is particularly beneficial when the labeled data for the target task is limited, expensive, or challenging to obtain.<br>
Here we use imagenet model from the tensorflow hub library(It is trained on millions of images for classifying 1001 objects.


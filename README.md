# Semantic Segmentation
In this project it will implement PSPNet architecture to implement Sementic Segmenatation. (ref: https://arxiv.org/pdf/1612.01105.pdf).
Semantic Segmentation is a computer vision task in which the goal is to categorize each pixel in an image into a class or object. 
## Scene Parsing
Scene Parsing which is based on Semantic Segmentation will assign each pixel in the image a category label to provide complete understanding of the scene. Unlike simple State-of-the-art scene parsing frameworks (fully convolutional network (FCN) and convolutional neural network (CNN)), it will understand the context of the scene. This will avoid mistake by predicting the data which out of context. Pyramid scene parsing network (PSPNet) is the algorithm that can achieve above goal.
## Pyramid scene parsing network (PSPNet)
In addition to traditional dilated FCN, it uses pyramid pooling to achieve pixel-level feature prediction.
### Pyramid pooling

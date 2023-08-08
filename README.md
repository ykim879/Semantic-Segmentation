# Semantic Segmentation
In this project it will implement PSPNet architecture to implement Sementic Segmenatation. (ref: https://arxiv.org/pdf/1612.01105.pdf).
Semantic Segmentation is a computer vision task in which the goal is to categorize each pixel in an image into a class or object. 
## Scene Parsing
Scene Parsing which is based on Semantic Segmentation will assign each pixel in the image a category label to provide complete understanding of the scene. Unlike simple State-of-the-art scene parsing frameworks (fully convolutional network (FCN) and convolutional neural network (CNN)), it will understand the context of the scene. This will avoid mistake by predicting the data which out of context. Pyramid scene parsing network (PSPNet) is the algorithm that can achieve above goal.
## Pyramid scene parsing network (PSPNet)
In addition to traditional dilated FCN, it uses pyramid pooling to achieve pixel-level feature prediction.
### Pyramid pooling
Pyramid pooling is beneficial since CNN is restricted to input size. CNN consists of some Convolutional (Conv) layers followed by some Fully-Connected (FC) layers where FC layers needs fixed input. Since not all images are fixed size, the cropping will be needed for the model. Cropping  may lose important feature that helps the machine to predict the data. To avoid this problem we add  Spatial Pyramid Pooling (SPP) layerbetween the last Conv layer and the first FC layer and removes the fixed-size constraint on CNN. 
SPP layer is to pool the variable-size features that come from the Conv layer and generate fixed-length outputs that will then be fed to the first FC layer of the network.The input of the SPP layer is a set of d feature maps of arbitrary size. Then, the SPP layer maintains spatial information of these feature maps in local spatial bins. The process is below: 
1. The first pooling layer (right in the image) consists of a single bin that outputs a d-dimensional feature since it applies max pooling in each input feature map.
2. The second pooling layer (middle in the image) consists of 4 bins that output a 4 \times d-dimensional feature.
3. The third pooling layer (left in the image) consists of 16 bins that output a 16 \times d-dimensional feature
All pooling layers apply max pooling. In total, the output feature has a fixed size that is equal to (16 + 4 + 1) \times d.

reference: https://www.baeldung.com/cs/spp-cnn

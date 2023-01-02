# Pandas object detection 

This is an implementation of [Mask R-CNN](https://arxiv.org/abs/1703.06870) on Python 3, Keras, and TensorFlow. The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.

The repository includes:
* Source code of Mask R-CNN built on FPN and ResNet101.
* Training code for MS COCO
* Pre-trained weights for MS COCO
* Jupyter notebooks to visualize the detection pipeline at every step
* ParallelModel class for multi-GPU training
* Evaluation on MS COCO metrics (AP)
* Example of training on your own dataset

![téléchargement (1)](https://user-images.githubusercontent.com/119355403/210189235-1a2007ee-b5b5-4cf0-adca-3d171af8f415.png)
![téléchargement (2)](https://user-images.githubusercontent.com/119355403/210189236-06a2f340-1fc4-45ba-93f7-d23a4e05a742.png)
![téléchargement (3)](https://user-images.githubusercontent.com/119355403/210189237-d12dbf67-e158-4fd5-b646-4b78f450ddf5.png)
![téléchargement (4)](https://user-images.githubusercontent.com/119355403/210189238-64d902a3-b0ae-44dd-81f3-9d98e01cb8d0.png)
![téléchargement](https://user-images.githubusercontent.com/119355403/210189239-175495e0-480a-4b5b-9de0-629afddd843b.png)

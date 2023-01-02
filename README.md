# Pandas object detection 

This is an implementation of [Mask R-CNN](https://arxiv.org/abs/1703.06870) on Python 3, Keras, and TensorFlow. The model generates bounding boxes and segmentation masks for each instance of an object in the image. It's based on Feature Pyramid Network (FPN) and a ResNet101 backbone.



![téléchargement (1)](https://user-images.githubusercontent.com/119355403/210189263-84b81094-0d1e-4d6e-aa65-38436cfbd152.png)
![téléchargement](https://user-images.githubusercontent.com/119355403/210189269-401b995b-5b4a-453e-959d-bcf3fb6f1c1a.png)

The repository includes:
* Source code of Mask R-CNN built on FPN and ResNet101.
* Training code for MS COCO
* Pre-trained weights for MS COCO
* Jupyter notebooks to visualize the detection pipeline at every step
* ParallelModel class for multi-GPU training
* Evaluation on MS COCO metrics (AP)
* Example of training on your own dataset


![téléchargement (3)](https://user-images.githubusercontent.com/119355403/210189275-7f77b623-035b-4d01-a7bc-13b57ff3aa39.png)
![téléchargement (4)](https://user-images.githubusercontent.com/119355403/210189280-3a022e9a-95ad-4180-9781-800f11af3b1d.png)

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

1 Collect the images e prepare the dataset with the images
In this case, I decided to identify pandas as a model.
The first step is to shoot many in different positions, with different lighting, in the middle of other objects, and with different backgrounds. In practice, the more images you can recover and the more different they will be, the more effective your model will be. To create even more variety I recommend using Image Augmentation (Improve your Dataset) | with Imgaug.

When you have collected enough images we need to move on to annotations, i.e. manually define the position of the object and assign a label. There are several annotation software but I recommend this open-source project https://www.makesense.ai.

2 How to train the dataset
First of all, we need to enable the GPU because we need the graphics card to do the training. Then go to Edit -> Notebook Settings and when the window opens select GPU from the drop-down menu then save.
Now we can start, I divided the notebook into 4 big steps:

Installation Mask R-CNN
Image Dataset
Training
Detection (test your model on a random image)

1. Installation Mask R-CNN
In this first step, Mask R-CNN will be installed on Google Colab in a totally automatic way, you just need to start it. Tensorflow and all necessary libraries will also be installed by the script
2. Image Dataset
First of all, we have to put our images folder in a .zip archive and we will have a dataset.zip file. We just have to upload the files to the notebook, the easiest way is to click on the folder design on the right and drop the file one at a time: annotations.json
dataset.zip
If the procedure is successful without problems you will have your files uploaded and by clicking on the Play of the second step you will get the total number of images uploaded.
To see if everything is correct load image samples. This function loads random images to verify that the annotations are correct.
3. Training
In the third step there are two cells, the first checks how many images there are and performs various preparatory processing for the training of Mask R-CNN. You don’t see it but there is a lot of code underneath that processes everything in seconds. In the next step, you can start with the training.
After a few seconds, we can already check if there is a first template ready mask_rcnn_object_0001.h5. This is the path Mask_RCNN -> logs -> object20210802T1353, your name may vary slightly but surely you will be able to find it.

4. Detection with Mask R-CNN (test your model on a random image)
Also in the fourth step, there are 2 blocks, the first is used to load the last model created. The latter is supposed to be the most accurate. Finally, we can test the resulting model of the training Mask R-CNN.

It will not be necessary to load anything because it will take random images and execute Mask R-CNN.

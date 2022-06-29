# Pothole Classification

This project aims to train a neutal network model that can alert drivers, cyclists, and pedestrians of road irregularities. We are focusing specifically on potholes for this model because one third of all traffic fatalities in America are caused by poor road conditions and potholes are the most costly/deadly obstacle. Even when potholes are not fatal, drivers can expect to pay an average of $377 for hitting a pothole and damaging their vehicle. 

The goal of the project is to build a model that can be integrated with a camera and mounted on a car, bike, or walker to alert the user while they are approaching a dangerous pothole to avoid the area.

![alt text](https://github.com/kwonkh0424/road_object_classification/blob/main/Walker.png)

We start this project by using a data set of around 750 images, balancing between images of well paved roads and potholes. Then we trained a number of baseline models including a vanilla CNN and variations on the VGG16 pretrained images classification model (partially frozen, finetuned, and from scratch). These models were able to achieve an accuracy around 50% on the training and test sets, so our goal was to beat that score.

Pothole            |  Negative Sample
:-------------------------:|:-------------------------:
![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/1.jpg)  | ![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/3.jpg)
![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/2%20(1).jpg)  | ![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/4.jpg)
![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/3._106177564_pothole.jpg)  | ![](https://github.com/kwonkh0424/road_object_classification/blob/main/img/7.13802057035_4e6ab91b98_b.jpg)

To improve upon our baseline, we added an additional data set to increase our training set to around 1300 total images. We also noticed we only had 16 images in the test set and some were not potholes, so we increased the test set size and removed incorrect images to improve data quality.

After researching some papers, we also found that image augmentations helped researchers increase model performance and increase data set size. Rotations, horizontal flip, brightness, and contrast were randomly applied to images during processing to increase model performance when the camera has a poor angle or during different weather/lighting conditions.

Finally, we tested a few different models and hyperparameter tuning to find the best combination of model, learning rate, and optimizer. The models tested included vanilla CNN, CNN with dropout, VGG, AlexNet, and ResNet...

# References

1. Kaggle Pothole Dataset: https://www.kaggle.com/datasets/sachinpatel21/pothole-image-dataset
2. Kaggle Pothole Dataset: https://www.kaggle.com/datasets/sachinpatel21/pothole-image-dataset
3. Pothole Facts: https://www.pothole.info/the-facts/
# Airbus Ship Detection
A [Kaggle challenge](https://www.kaggle.com/c/airbus-ship-detection) to detect all ships in satellite images and locate them in every single image.

## Description
Our project mainly consists of `Web` repo and `Model` repo. 
* In the `Web` repo, you will see how we build our webpage and web server.   
* In the `Model` repo, you will see how we build and train our model, thus detecting ships in testing set.

## Datasets
* Training set includes `231,724` satellite images.   
  * For images in the training set, the ground truth `EncodedPixels` are provided in the `train_ship_segmentations.csv` file.
  * `EncodedPixels` is blank if there are no ships in the image.
* Testing set includes `15,606` satellite images   
  * For images in the testing set, our goal is to predict the `EncodedPixels`.

## Model
For this task, we compared several models and chose [U-Net model](https://www.kaggle.com/hmendonca/u-net-model-with-submission). 
* **U-Net** is highly suitable for binary segmentation of images, which is exactly our task: binary segmentation for is or is not a ship.

## Webpage

## Usage
### 1. Use our webpage
Here to visit our ship detection [webpage](https://www.shipdetection.ml/).
* Notice that the webpage is still a prototype. For now, the function including uploading images and outputing images can be done. Futher development are to be built. 

### 2. Run at local
* To directly run the ship detector at local, you will need to setup your environment. Please refer to `Model/tools/ENG_Grid/` in the `Model` repo.
After that, you can use our ship detector by:
```
command
```

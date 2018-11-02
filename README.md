# Airbus Ship Detection

Project derived from [the Kaggle challenge "Airbus Ship Detection"](https://www.kaggle.com/c/airbus-ship-detection) to detect all ships in satellite images and locate them in every single image.

If you have more questions, feel free to contact <shipdetection@phy25.com> or emails [listed here](https://drive.google.com/open?id=11rLsOUhRSbCihl513VZVUK5XEWhZHEkf73p-rwu8QX4) *(Section A1, 09: Airbus Ship Detection)*.

## Resources

Our project mainly consists of [Model repo](https://github.com/BUGenerator/Model) and [Web repo](https://github.com/BUGenerator/Web). Issues and pull requests for these repos are welcome.

* In the Model repo, you will see how we build and train our model, thus detecting ships in testing set. (https://github.com/BUGenerator/Model)
* In the Web repo, you will see how we build our webpage and web server. (https://github.com/BUGenerator/Web)

Other resources are listed below (some need BU Kerbose account):

- Agile board: https://github.com/orgs/BUGenerator/projects
- Sprint 1 Slides: https://drive.google.com/open?id=1nW0XfrfmcUOdIXQVQkb_QdVCRu0mEHe2
- Sprint 2 Slides: https://drive.google.com/open?id=1hg6p04cKZ-N-WCua3hLS_kNUqgNbzFMCdizPbBcJbNw

## Datasets

* Training set includes 231,724 satellite images.   
  * For images in the training set, the ground truth `EncodedPixels` are provided in the `train_ship_segmentations.csv` file.
  * `EncodedPixels` is blank if there are no ships in the image.
* Testing set includes 15,606 satellite images   
  * For images in the testing set, our goal is to predict the `EncodedPixels`.

## Model

For this task, we compared several models and chose [U-Net model](https://www.kaggle.com/hmendonca/u-net-model-with-submission) for now.

***U-Net** is highly suitable for binary segmentation of images, which is exactly our task: binary segmentation for is or is not a ship.*

## Webpage

* For frontend, we build it with Bootstrap. For backend, we build it with Flask in Python.
* The web server is deployed on [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/). Thanks to [Semaphore CI](https://semaphoreci.com), we are able to auto deploy the program onto Beanstalk when new commits are pushed onto https://github.com/BUGenerator/Web/tree/master.

## Usage

### 1. Check out the webpage

Visit our ship detection webpage at https://www.shipdetection.ml/.

*Notice that the webpage is still a prototype. For now, the function including uploading images and outputing images can be done. Futher development are to be built.*

### 2. Run locally

To directly train and run the ship detector locally, you will need to setup your environment. Please refer to https://github.com/BUGenerator/Model/tree/master/tools/ENG_Grid for a development environment. We will have instructions on simpler detection-only environment setup later.

After that, you can go through the .ipynb file by:

```shell
$ jupyter notebook
```

*We will upload the model we have trained and the standalone detection module later. Sorry about this.*

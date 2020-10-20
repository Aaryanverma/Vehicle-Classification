# Vehicle Classification

Transfer Learning is a technique in which we can train a model using a pre-trained model in case of small dataset because deep learning model needs huge amount of data for training from scratch.

In case of Computer Vision, There are various pretrained models available like VGGNet, ResNet, MobileNet etc.

To choose best model for your usecase, check whether the pretrained model you want to select is already trained on the class on which you want to work or not.

If it is already trained on similar usecase then choose that model only because it will converge faster and give better accuracy in lesser time.

In provided notebook, dataset chosen is a vehicle dataset consisting of 9 classes of vehicles namely: bike, boat, bus, car, cycle, helicopter, plane, scooty, truck

Dataset Credits: https://www.kaggle.com/rishabkoul1/vechicle-dataset


Train Images containes 468 images and Test Images contains 72 images which makes this a perfect case for transfer learning

I used MobileNet V2 pretrained model for transfer learning here because it is lightweight and still accurate.

Applied GlobalAveragePooling2D for extracting the average of best features from images.

Since, dataset is too small, Image Augmentation is done for the dataset to generate more images on the fly while training to get better accuracy while testing with unseen images.

Three types of Augmentation is done
- Rescale: normalize the image
- Shear: Distorts the image like a parallelogram
- zoom: enlarge the image

Each image is augmented three times for each iteration, therfore generating more data for training.


Model is trained and got Training accuracy of 97.22% while Validation accuracy is 83.33%.

**THIS SHOWS HOW TRANSFER LEARNING CAN BE USED IN DEEP LEARNING FOR SMALL DATASETS AND STILL GETTING GOOD ACCURACY.

- Author: Aaryan Verma
- References:
  - https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html
  - https://towardsdatascience.com/step-by-step-guide-to-using-pretrained-models-in-keras-c9097b647b29

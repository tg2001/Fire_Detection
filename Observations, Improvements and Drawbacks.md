# Observations:

- There are a number of image transformations applied like translating, rotating, zooming in/out, flipping, blurring and adding noises to the images. These are applied both to increase the number of images, and to make the model more robust to changes.
- The model architecture can be seen in the code itself, which shows the number of convolution, pooling and dense layers used and also the way they are used. The commented layers show the different combination of models used. The accuracy is quite good (99%).
- Normally, using black and white images is preferred over coloured, because it requires much less calculations as compared to the colored ones. But in case of fire detection, we had to use colored images as color is the only determining factor if it is a fire or not. If black and white image is used, then probably, the only way for the model to know whether it's a fire or not is by noticing a sudden increase in brightness in the image.
- If the model is successful in identifying that smoke mostly accompanies fire, then that's great, because in that case, it can identify fire from smoke, if the fire is not within the camera's range. But in this case, the model may confuse between smoke and fog.
- The graph at the end shows confidence of the images in the test set, because just the accuracy isn't enough. Accuracy gives a count of the number of images identified correctly, whereas confidence suggests the surity with which the model can label the images.

# Improvements and Drawbacks:

- As already mentioned in the 'Dataset.txt' file about the drawbacks of the dataset on which the model is trained, a way to improve the model is to mitigate those drawbacks by providing more images, providing images with the fire occupying a small portion of the image and providing non-fire images with yellow object in them.
- Another possible imrovement can be to use a different architecture, may be with custom layers, to get better results.
- A drawback of the model is that it identified my image wearing a yellow t-shirt as fire with 90% accuracy. So again, the way to remove this error is to train the model with images containing yellow objects which is not fire.

# Height Detection 


## Method Summary

In order to estimate height, we first started by determining the coordinate locations of corn labels in our given training data.

We used the images generated from the video data for the given labels and ran these through our Batch Object Detection Notebook ([ObjectDetection_Batch.ipynb](https://github.com/trentspi/corn_connection_detection/blob/master/height-detection-submission/ObjectDetection_Batch.ipynb)). The Object Detection notebook is a batch process that takes our existing Tensforflow Object Decetion Model and labelmap in order to generate coordinates from an image of the detection boxes. These coordinates were used as our training coordinates since we already had the heights for these samples.

From there, we did the same thing for testing images (samples that we did not have height labels for). We also ran these images through our Batch Object Detection Notebook ([ObjectDetection_Batch.ipynb](https://github.com/trentspi/corn_connection_detection/blob/master/height-detection-submission/ObjectDetection_Batch.ipynb)) in order to generate coordinates of the detection boxes.

After this, we fed our training and test coordinates to our Height Prediction model ([HeightPredictions.ipynb](https://github.com/trentspi/corn_connection_detection/blob/master/height-detection-submission/HeightPredictions.ipynb)). This is a linear regression model that predicts the average height based on multiple images that were extracted from the same video sample. We also tried models such as a Random Forest Regressor or a Gradient Boosting Regressor, however our best R^2 score was on the linear regression model.

We were also able to get metrics based on predictions of our given data and labels such as mean absolute error and mean squared error.

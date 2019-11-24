# Corn Connection Detection

## Running the model

1. Open the `object_detection_image.ipynb` notebook

2. In the second cell, the following code will be found:
   ```
   # Name of the directory containing the object detection module we're using
   MODEL_NAME = 'inference'
   
   # The filename of the image to be used for object detection
   # Change this filename in order to run an image through the detector
   IMAGE_NAME = 'image.jpg'
   ```
   Change the `IMAGE_NAME` to be the filename of the image to be ran through the object detector
   
 3. Run all of the notebook cells
 
 4. The last cell will execute the Open CV window for the object detection of the image itself
 ![](https://i.imgur.com/2hfsyR9.jpg)
 5. Press any key to exit the detection window

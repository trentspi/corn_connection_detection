
# Corn Connection Detection


### Pre-processing
Using tensorflow Object detection API to detect the corn connections off from a video files.
We extracted the images off from video capturing frames once every second using following
example as reference: https://www.geeksforgeeks.org/extract-images-from-video-in-python/.

After extracting the images, we tried labelling images for few of the videos. And after that used
the Object Detection model provided by tensorflow to start the training. In the meantime we came across
a very useful similar project, so referenced few things off from there. Here is the link of the project
we used a reference: 
https://github.com/EdjeElectronics/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10

### Training
We trained using the same deep learning architecture used in the refernce project, the faster resnet network.
It takes a long time to train the network, it took us quite long amount of time to train however much we have trained.
And as a result we have a model that is good at detecting overall corn regions in the crop.


### Testing
When we started testing, we realized that it didn't do good on the images for whose camera angles were weird. So if there
are images which looks like it is taken by camera that is held completely vertical, then only it will be able to detect
the corn connections otherwise it is not able to do so. So we need to re-train the model with more labelled images whose
images are taken from weird camera angles. For example, if you look at video from GOPR0165 you can see that the video is
taken from different angle than in videos from GOPR0388-GOPR0491.


### Running the model
Just clone this repository locally and add the images or video into the cloned repo destination for which you would want
to test our model.


For running this model, run the following scripts with minor modifications:
* Run this script to test against a image (only one image can be tested at a time):
    * https://github.com/trentspi/corn_connection_detection/blob/master/Object_detection_image.py
    * Edit line 22 in this script and replace it with image filename (including extenstion) that needs to be tested


* Run this script to test againsts a video (only one video at a time) :
    * https://github.com/trentspi/corn_connection_detection/blob/master/Object_detection_video.py
    * Edit line 22 in this script and replace it with video filename (including extenstion) that needs to be tested



To execute the code go into the directory where you cloned the repo. And from command-promt/console/shell execute following
commands:
* `python Object_detection_image.py`
* `pyton Object_detection_video.py`
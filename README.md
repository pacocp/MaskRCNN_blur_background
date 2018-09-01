# Blur the background of an image

This project uses the Mask R-CNN algorithm to blur the background of an image leaving the object focused. The aim was to
simulate the effect of the iPhone X or other phones camera when you are taking
a selfie and it blurs the background leaving you as prettiest as you are (it doesn't
do magic, I am sorry).

The Mask R-CNN was published March 2017, by the [Facebook AI Research (FAIR)](https://research.fb.com/category/facebook-ai-research/).

This paper claims state of the art performance for detecting instance segmentation masks. If you want
to know more, you can check the original [paper](https://arxiv.org/abs/1703.06870).

## Mask R-CNN implementation

This project uses the Mask R-CNN implementation from [Matterport, Inc](https://matterport.com) in Tensorflow and
Keras, you can check it and please leave them a star in their [repository](https://github.com/matterport/Mask_RCNN).

A few changes have been made:

	- A new function to take the mask and save in a new matrix the pixels where the objects are present.

	- Perform the blurring and assign the original image values to the blurred pixels where the objects are present.

A Gaussian filter is applied in order to blur the image.

## Requirements

Python 3.4, TensorFlow 1.3, Keras 2.0.8 and other common packages listed in requirements.txt.

To install requirements:

```
pip install -r requirements.txt
```
## How to use

The main script is **detect_and_blur.py**. An example of execution would be as follows:

```
python3 detect_and_blur.py --input_name input_image.png --output_name blurred.png
```

It would save the new image in the location given.

## Example

![Example of blurred image](https://github.com/pacocp/MaskRCNN_blur_background/blob/master/samples/guiness-paco_blur.png)

	
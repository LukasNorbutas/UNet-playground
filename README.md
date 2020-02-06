# Steel fracture detection

#### ***Problem***
Image segmentation problem - there are 4 classes of different fractures, each of which contain very irregular shapes. The task is to locate them.

#### ***Solution***
UNet model that takes image as the input and 4-channel mask as the label. Each mask has the same dimensions as the image, but only 1 channel (e.g. 256x2000x1) that represents fracture of a specific class. This way we can simultaneously model segmentations of all classes in the same label.

#### ***Models***
- UNet with ResNet50 base (4-channel mask), Dice loss
- UNet with ResNet50 base (1-channel mask), Dice loss

#### ***Results and learnings***
Sorry, no metrics yet! 
- It seems pretty easy to get an ok solution (visually) with out-of-the-box models.
- The models are really slow and it was pretty difficult to find a working architecture-loss combo.
- Pre-processing was nasty.


## **Teaser**
![alt text](https://i.imgur.com/xCVtZwk.png)

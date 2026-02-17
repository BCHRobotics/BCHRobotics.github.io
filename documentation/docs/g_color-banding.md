# Object Detection With Color Banding

This is the simpler of the two common approaches to object detection.
 
The idea is to take a source image and pick out regions that have a similar color - the color of the game piece we want to look for.

{raw image of a game piece}

{processed image of a game piece}

## Setup

Photonvision has an entire framework for color banding built into it, so it's incredibly easy to set up. 

{image showing the panel}
 
![alt text](img/od_1.png?)
*This is what the camera sees.*
![alt text](img/od_2.png?)
*By looking for yellow circles in the image, we can detect the ball (the red square is its bounding box).*
 
## Flaws

Since we are only looking for color and no other characteristics like shape, this approach struggles to differentiate between items of the same color - yellow balls vs. yellow cones, for example.
 
![alt text](img/od_3.png?)
*This time, the camera can see two yellow objects: a ball and a cone.*
![alt text](img/od_4.png?)
*As you can see, the result is a lot messier. Keep in mind that we're only trying to detect the ball.*
 
Worse is when you accidentally detect field elements or other things in the background that have a similar color to the one you want - or just happen to look that way because of the lighting. It gets much worse when the game piece you're looking for is either red or blue (the balls from 2022 is one example) because many field elements are either red or blue. In short, if you're looking for a red or blue game piece you can abandon all hope of using color banding to find it.
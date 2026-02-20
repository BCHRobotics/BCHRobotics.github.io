# More Advanced Object Detection Strategies
`in progress`
 
*Note that all of these approaches rely on having an accurate way of identifying objects. I would not recommend trying any of them unless you have a good neural network - you will not be able to get very far with color banding.*

## 3D Pose Estimation For Spherical Objects
 
Object detection tends to leave you with a bounding box, and that's all. While this isn't a lot of information, it is enough to estimate the 2D field position of an object - with one condition. The object has to appear identical from all directions - which pretty much limits you to spheres (thankfully a lot of FRC games have balls as their main game piece).
 
The idea here is to first estimate the distance to the ball, and then use that information along with the direction that the camera is facing to estimate the 3D position of the ball. 

# List of Known Problems and Their Solutions

Hopefully this helps with troubleshooting any random issues that come up. Please add to this if you find any more problems/solutions!

## Robot suddenly drives full-speed in a direction?
(CAREFULLY disable and enable again to see if it keeps driving, it should head in the same direction it was going in.)

This is caused by a value of NaN or Infinity being sent to the drivetrain. The easiest way to get NaN is using a divide by zero, so check for any divides in the code and make sure you're not allowing zeros to get through.

## One of the swerve wheels is dragging or spinning in the wrong direction?

Possible fixes:
 
* reset the swerve turning encoders (see [LINK])
 
* check for any unplugged encoder or power cables (and plug them back in)
 

If the above don't work, make sure nobody has edited the swerve-handling part of the robot code, especially the following:


*in Constants.java*
 
 
`public static final double kFrontLeftChassisAngularOffset = -Math.PI / 2;`
 
`public static final double kFrontRightChassisAngularOffset = 0;`
 
`public static final double kBackLeftChassisAngularOffset = Math.PI;`
 
`public static final double kBackRightChassisAngularOffset = Math.PI / 2;`

You may want to test the problematic motors on their own to make sure they work.

## 
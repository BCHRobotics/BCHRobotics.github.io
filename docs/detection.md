# The Rationale Behind: Gamepiece Detection

by 10tothe6

Something we need for a long-term software solution is a way of seeing game pieces on the field. 

There are two ways to do this: 
* you process the image and use thresholds to look for groups of color (from now on referred to as `thresholding`)
* you use a neural network (from now on referred to as `machine learning`)

For 2024 Crescendo we used `thresholding`, and it was difficult to adjust the thresholds to different lighting settings. It was also very possible that the camera might pick up on things that aren’t game pieces. 
This wasn’t that bad with the very-orange notes, but gets worse when the game piece is a neutral color (e.g. white), like coral in 2025 Reefscape. It’s even worse when the game pieces are red and blue, like in 2022 Rapid React, because so many other game elements are the same colors. Overall this approach is sketchy at best, and for some game pieces is practically impossible. Not a good long term solution.

`Machine learning` is much better. It allows for reliable detection of practically any game piece, if you train the neural network well enough. It is much less affected by neural-colored pieces, and red-and-blue pieces. Is it harder to get going? Yes. But from my experience programmers on our team often have little to do, and the process of training a model can be done by less-experienced students.


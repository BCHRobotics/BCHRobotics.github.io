# The Rationale Behind: Our FRC Dashboard

by `10tothe6`

There are a lot of programs that run on driverstations that can display information from the robot to anyone who happens to be driving it. We all know them as `dashboards`. Here are the most popular ones, from what I've seen:

* `WPILib Shuffleboard`
* `WPILib SmartDashboard`
* `LabVIEW`
* `Glass`
* `AdvantageScope`
* `Elastic`

As you can see, there are a few to choose from (to be fair, not all of these are the kinds of dashboards you would use *during a match*, some are more suited for testing in-house). Which one did we pick? Well, we didn't.

The dashboard that our team uses is called `Drivetools`, and it's developed by `FAR Robotics` (that's a fancy way of saying that it's developed by me, `10tothe6`). So add that one to the list, I guess.

Alright so why did I decide to make my own dashboard? First let's look at what I dislike about the existing dashboards.
*(I admit that I'm not the most well-informed, feel free to let me know that I'm wrong about some of these)*

* `LabView`: It's... old. And not very easy to work with, from what I've seen.
* `Shuffleboard`: It's just not as customizable as I'd like.
* `SmartDashboard`: I've never seen it *not* glitch out, and display the text weirdly. Also old.
* `Glass`: Actually I can't think of anything, I guess it's a little busy.
* `AdvantageScope`: Never tried it, but I know it doesn't work that well for competition scenarios.
* `Elastic`: Best one that I've seen, I don't have any gripes about it.

Obviously that's not enough, I mean why not just use `Elastic`? The big reason is that as a part of `FAR Robotics` I want to do a lot of more advanced things that involve communication from the computer to the robot. It's really useful to have a custom solution for that, which is why we didn't use some *other* teams custom dashboard.

In the end, it comes down to features. There are a few *really* specific features that none of the other dashboards have, that `Drivetools` does. And hey, it's a good opportunity to try and improve on things, right?

*(I encourage you to try `Drivetools` by the way, I think its cool)*


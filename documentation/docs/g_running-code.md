# Deploying and Running FRC Robot Code
`in progress`
 
Thankfully, WPILib makes the process of uploading (aka. deploying) and running robot code incredibly easy. Here's a quick run-down:
 
* Press ctrl+shift+p on your laptop to open the commands menu.
 
* Type 'Deploy Robot Code', and click on the command from WPILib.
 
{image of the deploy robot code thing}
*The command that you need to run.*
 
* Wait until on, FRC Driverstation, you see the 'Communications' light turn green. That's it! You can now enable.

## Some Details
'building' code and 'deploying' code are two different things, and thus have two different commands.
 
{image of the two}
 
The 'Deploy Robot Code' command actually runs a build first, before deploying, so there's no need to always run the build command before the deploy command. It'll do that for you. However, sometimes the 'Build Robot Code' command will try and download vendor libraries from the internet (if you don't have a local copy) - and of course you can't do that while connected to the robot network. So if you get this error or a similar one:
 
{image of the error}
 
Then connect to a proper wi-fi network, run a build by itself, then connect back to the robot and deploy. Once it's downloaded the vendor libraries once, it'll have them saved to your computer and you won't need to download them again unless you change them.
 
Also, by default, deploying code will NOT delete old files on the RoboRIO. You do want to delete old files, so that any autos you delete on the laptop side don't stick around on the RIO side, for example - and saving disk space never hurt anyone. Make sure that old files get deleted by setting [] to true:
 
{image of the variable in question}
 

![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Welcome to the repository for integrating ArduPilot master onto the 3DR Solo! This is the central location for information, instructions, and files. 

Quick Background
----------------
A stock Solo uses a heavily customized branch of ArduCopter 3.3 circa 2015.  Since that time, the ArduCopter project has made significant strides to version 3.5.  With 3DR no longer in the consumer UAS industry, the Solo has fallen far behind.  There many operational stability, reliability, and safety enhancements to ArduCopter master that the Solo is now lacking.  There are many many new features in ArduCopter master that the Solo is also now lacking, such as "boat mode".  The ArduPilot Solo project aims to bring Solo up to the current ArduCopter master level, and keep it there.  This will allow the Solo to make use all of current ArduCopter features and functions.  And it will keep it on the leading edge as ArduCopter continues to grow.  Many people are contributing time, skills, materials, and testing effort to this project.


The Firmware
------------
The files listed above will get your Solo onto ArduCopter master. There is a zip file that contains everything for one easy download, which you can easily right-click above to download.  You can also go through individual files to see what they are and a history of the changes. The directories are as follows:
* `Firmware` contains the ArduCopter firmware files. There may be more than one firmware file if there are more than one currently stable file for general use.
* `IMX` contains files that should be uploaded to the Solo's companion computer.  These are usually python (*.py) files, and usually go in the /usr/bin/ directory.
* `Parameters` contains ArduCopter parameter files applicable to the firmware. This is baked into the firmware as defaults now! So this is only for reference.
* The Solo Beta full branch [repository can be found here.](https://github.com/Pedals2Paddles/ardupilot/tree/solomod-master)

Releases
---------
Tracking of the "official" Solo Beta releases can be found here in the GitHub releases list in the nav bar above or [here](https://github.com/Pedals2Paddles/SoloBeta/releases).  This is how the latest changes, additions, & subtractions will be documented in an organized manner. These "releases" document the files in the directories above (and the zip file).  


The Hardware
------------
**The Green Cube (or a traditional Cube 2.1 with the internal jumper set for 5 volts) are required for safe and reliable use of ArduCopter master on a 3DR Solo!** [You can purchase the Green Cube from ProfiCNC](http://www.proficnc.com/3dr-solo-accessories/79-the-cube.html).  The old stock firmware has a software patch to _mostly_ mitigate an electrical flaw in the motor pods. This is what you may hear referred to as "slew rate protection".  ArduCopter master does not have this slew rate protection.  It is severely handicapping and difficult to manage. It worked OK at the time, but is not practical to keep working. You can't/shouldn't fix a hardware problem with software.  The hardware solution to this hardware problem is replacing the stock Pixhawk 2.0 with the new Green Cube. That will allow you to safely run ArduCopter master without the slew rate protection.  You _can_ install ArduCopter master on the stock Pixhawk 2.0, but it is highly discouraged.  It will install, and it will fly.  But you are at fairly high risk for motors shutting down in flight, leading to a serious crash. 

**You cannot use the old stock 3DR Solo firmware on the Green Cube or Cube 2.1. It is entirely incompatible.*** The Cube will get stuck in bootloader if you try. This also means you cannot do a factory reset on the Solo with the Green Cube still in the Solo. The factory reset tries to reload the old Solo version of ArduCopter, which doesn't work.  If you need to Factory Reset, you will need to put the old stock Pixhawk 2.0 back in, run the full factory reset and update, then put the Green Cube back in. Yes, this is annoying, but there is no way around it now or in the foreseeable future. In short, do not need to factory reset!

Useful Links
------------
* [ProfiCNC](http://www.proficnc.com/3dr-solo-accessories/79-the-cube.html) for the Green Cube and other cool gear
* [Solo Beta Test](https://www.facebook.com/groups/617648671719759/) group on Facebook
* [Solex Users](https://www.facebook.com/groups/176789056089526/) group on Facebook
* [Solex App](http://www.solexapp.com/) official website. This app is truely the future of Solo's user interface!
* [Solo Mod Club](https://www.facebook.com/groups/3DRSOLOModClub/) group on Facebook
* [ArduPilot](http://ardupilot.org/) homepage
* [ArduCopter Full Parameter List](http://ardupilot.org/copter/docs/parameters.html) details all 700 something parameters in ArduCopter.
* [ArduCopter introduction](http://ardupilot.org/copter/docs/introduction.html): Learn what you're getting yourself into :)
* [Mission Planner](http://ardupilot.org/planner/docs/common-install-mission-planner.html) ground station app for Windows
* [Filezilla](https://filezilla-project.org/download.php?type=client) for moving files to/from the companion computer
* [WinSCP](https://winscp.net/eng/download.php) for moving files to/from the companion computer


Initial First Time Install Using the Solex App on Android
----------------------------------------------------------
This is by far the easist and most highly recommended way to install the Green Cube and install ArduCopter. No need for Mission Planner, WinSCP, Filezilla, SSH, or a complicated passwords.
[Solex initial install instructions](../master/Initial_Install_Solex.md)


Initial First Time Install _without_ Solex
-----------------------------------------------
These instructions currently assume you already know how to use things like Mission Planner and WinSCP or Filezilla. Multiple applications and processes are required. I cannot provide detailed step by training on how to use these applications.
[SCP & Mission Planner method intial install instructions](../master/Initial_Install_Other.md)
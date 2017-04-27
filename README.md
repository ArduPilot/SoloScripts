![Logo](https://github.com/Pedals2Paddles/SoloBeta/blob/master/Misc/APsolo.jpg)

Welcome to the repository for integrating ArduPilot master onto the 3DR Solo! This is the central location for information, instructions, and files. 

Quick Background
----------------
A stock Solo uses a heavily customized branch of ArduCopter 3.3 circa 2015.  Since that time, the ArduCopter project has made significant strides to version 3.5.  With 3DR no longer in the consumer UAS industry, the Solo has fallen far behind.  There many operational stability, reliability, and safety enhancements to ArduCopter master that the Solo is now lacking.  There are many many new features in ArduCopter master that the Solo is also now lacking, such as "boat mode".  The ArduPilot Solo project aims to bring Solo up to the current ArduCopter master level, and keep it there.  This will allow the Solo to make use all of current ArduCopter features and functions.  And it will keep it on the leading edge as ArduCopter continues to grow.  Many people are contributing time, skills, materials, and testing effort to this project.


The Firmware
------------
The files listed above will get your Solo onto ArduCopter master. There is a zip file that contains everything for one easy download, which you can easily right-click here to download.  You can also go through individual files to see what they are and a history of the changes. The directories are as follows:
* `Firmware` contains the ArduCopter firmware files. There may be more than one firmware file if there are more than one currently stable file for general use.
* `IMX` contains files that should be uploaded to the Solo's companion computer.  These are usually python (*.py) files, and usually go in the /usr/bin/ directory.
* `Parameters` contains ArduCopter parameter files applicable to the firmware. This is baked into the firmware as defaults now! So this is only for reference.
* `Testing` is for storing files being tested for easy access. It is not part of any actual release.
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
* [Mission Planner](http://ardupilot.org/planner/docs/common-install-mission-planner.html) ground station app for Windows
* [Filezilla](https://filezilla-project.org/download.php?type=client) for moving files to/from the companion computer
* [WinSCP](https://winscp.net/eng/download.php) for moving files to/from the companion computer
* [ArduPilot](http://ardupilot.org/) homepage
* [Solo Mod Club](https://www.facebook.com/groups/3DRSOLOModClub/) group on Facebook
* [Solex Users](https://www.facebook.com/groups/176789056089526/) group on Facebook
* [Solex App](http://www.solexapp.com/) official website. This app is truely the future of Solo's user interface!
* [ArduCopter Full Parameter List](http://ardupilot.org/copter/docs/parameters.html) details all 700 something parameters in ArduCopter.
* [ArduCopter introduction](http://ardupilot.org/copter/docs/introduction.html): Learn what you're getting yourself into :)


Instructions
------------
Remember, this is experimental and constantly developing. This is not a final product or final procedure (is it ever?). This is not currently an easy flash-and-fly procedure like you may be used with the 3DR Solo app.  Please read carefully.  These instructions currently assume you already know how to use things like Mission Planner and WinSCP or Filezilla. More detailed step by step instructions are in the works.  The ultimate goal is to Automate this process through the Solex App!

**Your solo should be in safe working order before you start**. It should not be malfunctioning or unreliable before you even begin. It must be up to date with the latest 3DR firmware. You cannot do this with a straight out of the box Solo. You must go through the full pre-flight update first on a new Solo.  Once your Solo is up to date and working well, you're ready to begin.


1. Load the py files onto the Solo's companion computer first.  The four python files at this time are are `rcManager.py`, `shotManger.py`, `buttonManager.py`, & `px_uploader.py`. Use WinSCP, Filezilla, or other SCP/SSH application to put all 4 python files in the /usr/bin/ directory of the companion computer, overwriting the ones that are there now. Once you've copied them in, you will need to reboot the Solo for them to take effect.


2. Load the ArduCopter firmware file.  This is the .px4 file in the firmware directory. Connect with WinSCP / Filezilla / SSH and drop this file into the /Firmware/ directory on the companion computer. Then reboot the Solo. It will detect the new file on boot, and go into bootloader. Give it time as it does its thing. This process takes approximately 5 minutes. There will be lots of colorful lights and beeping. Once it is done, it will play some musical tones and be ready for your input.  If you've ever loaded the old 1.5.3 firmware on the Solo as described in the forms, this is the same procedure.  After a short while, the controller will reconnect to the Solo.  Occassionally it gets lazy and both need to be power cycled to wake them up, which is nothing to worry about.


3. After you've loaded the firmware, you must do a full parameter reset. Reconnect with Mission Planner. In Mission Planner's full parameter list, click the reset to defaults button on the right. The Pixhawk will reboot on it's own, with all the defaults taking over. After a short while, the controller will reconnect to the Solo.  Occassionally it gets lazy and both need to be power cycled to wake them up, which is nothing to worry about.


4. With everything on, connect with the 3DR Solo app. Run the turtle/rabbit sliders for speed and pan through their full range from slow to fast. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be.


5. Go through all the settings in the 3DR Solo app (And Solex if you use it).  Touch every thing to set and verify everything. Do not assume these settings stuck from before.

6. Once all of this done, you will need to do a level calibration and a compass calibration using the 3DR Solo app as normal.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before click through to the next one.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. The Solo app uses the "onboard compass calibration" method, just like Mission Planner does.


7. Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

8. Enjoy!
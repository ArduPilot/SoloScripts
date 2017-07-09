![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Instructions
------------
These instructions currently assume you already know how to use things like Mission Planner and WinSCP or Filezilla. This method is somewhat complicated compared to using Solex. But this does work. Please read carefully and follow all steps in order.

Download the zip file for the version you wish to install from back on the [main page] (https://github.com/ArduPilot/SoloScripts). As of this writing, that is `ArduCopter_35-RC10.zip`. Save this zip file somewhere convenient and unzip it. In the zip, there are several files that will be used throughout this process.
* A parameters file (*.parm). As of this writing, the file is `AC35-RC10_Solo_Parameters.parm` but may be updated in the future.
* A directory of python files (*.py)
* A wipe firmware file called `Wipe_Pixhawk_Firmware.px4`
* An ArduCopter firmware file. As of this writing, the file is `AC35-RC10_Firmware.px4` but may be updated in the future.

These instructions use [WinSCP](https://winscp.net/eng/download.php) for moving files to/from the companion computer for Windows for file transfers. But the settings and process are basically the same for [Filezilla](https://filezilla-project.org/download.php?type=client) and other SFTP applications.  The settings and what the directory structures look like are pictured below:
  ![WinSCP Settings](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/winscp_settings.jpg)
  ![WinSCP Directories](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/winscp_directories.jpg)

These instructions require the use of the [Mission Planner](http://ardupilot.org/planner/docs/common-install-mission-planner.html) ground station application for Windows. The necessary settings for Mission Planner are pictured below. They are in the Config/Tuning > Planner sexction. You need the layout drop down set for advanced and the connection drop down set for UDP. To connect to the Solo, your PC must be connected to the Solo's WiFi. Press the connect button. Mission Planner will connect to the Solo's Pixhawk and download all it's parameters. Once connected, you will get many more options in config/tuning.
![MP Settings](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/mission_planner_settings.jpg)
JPG

1. **Your solo should be in safe working order before you start**. It should not be malfunctioning or unreliable before you even begin. It must be up to date with the latest 3DR firmware. You cannot do this with a straight out of the box Solo. You must go through the full pre-flight update first on a new Solo.  Once your Solo is up to date and working well, you're ready to begin.

2. **Update python files before installing Pixhawk!** Before doing anything else, you must load the new python files onto the Solo's companion computer. Use WinSCP, Filezilla, or other SFTP application as described in the beginning.  Put all the python files (`*.py`) in the **/usr/bin/** directory on the Solo, overwriting the ones that are already there. After copying the files, power cycle the solo. It will reconnect to the controller upon rebooting.

3. **Remove the battery tray:** Remove the battery and pop off the GPS cover.  Then unscrew all the small black screws around the battery tray. The battery tray can now be lifted up.  Unplug the GPS from the carrier board.  Set the battery tray aside. We highly recommend you do not lose the screws.
   ![Battery Tray Screws](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/battery_tray_screws.jpg)

4. **Lift up the carrier board:** Locate the comparatively large silver screw on the right side toward the front. Unscrew that and set it aside with all the other screws that you're not going to lose.  The carrier board can not be lifted up very carefully.  You will need to fidget with the wires from the motor pods a bit.  The board will need to go up a bit, then shift back, then shift up the rest of the way. The left side can go up higher than the right, which is convenient.  It's kind of tight and generally annoying.  Be careful not to break the small wires.  Don't break any of the other wires either.  You will need to get the board high enough up to expose the Pixhawk mounted underneath it.  It's the black cube looking device.
   ![carrier screw](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/carrier_retainer_screw.jpg)
   ![wires](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/carrier_board_wires.jpg)

5. **Unscrew the stock Pixhawk:** There are 4 very small screws on the top of the carrier board. Unscrew them and set them aside. The stock Pixhawk can now be removed. It will pull down off the carrier board. Set the stock Pixhawk aside somewhere safe. You will want to keep it.
   ![Pixhawk screws](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/pixhawk_screws.jpg)

6. **Install the green cube:** The green cube installs the same way the old one came off.  Plug it into the carrier board from the bottom.  Then put in the four screws.
  ![cube installed](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/cube_installed.jpg)
  
7. **Do not reassemble yet:** It is best to do the initial firmware install with the Solo still opened up. If anything goes wrong, it avoids having to disassemble it again. 

7. **Do not reassemble yet:** It is best to do the initial firmware install with the Solo still opened up. If anything goes wrong, it avoids having to disassemble it again. 

8. **Power up the Solo and reconnect to controller:** Put the battery onto the solo. It will just sit atop the carrier board. Obviously you should avoid manhandling the Solo while like this since the battery can just fall off. So get everything situated first.  Turn on the battery.  The solo will power up as usual. After a short while, the Solo will reconnect with the controller as usual. It will probably give you all kinds of warnings about calibration. This is normal and expected.

9. **Wipe Firmware:** Use WinSCP, Filezilla, or other SFTP application as described in the beginning.  Put the `Wipe_Pixhawk_Firmware.px4` file in the **/firmware/** directory on the Solo. If there are any other px4 files in this directory, delete them now, but there really shouldn't be. Power cycle the solo. It will reboot, then switch into bootloader mode. Normally you will see disco lights while it's doing this. But if the LED driver isn't enabled, you may not. Don't worry. It's working. Give it 3-5 minutes to process. You may hear some clicks as the Pixhawk reboots. After 3-5 minutes, you will hear some tones signalling completion. It will come back to life, reconnecting with the controller

10. **Install ArduCopter Firmware:** Use WinSCP, Filezilla, or other SFTP application as described in the beginning.  Put the _ArduCopter firmware px4 file_ in the **/firmware/** directory on the Solo. If there are any other px4 files in this directory, delete them now, but there really shouldn't be. Power cycle the solo. It will reboot, then switch into bootloader mode. Normally you will see disco lights while it's doing this. But if the LED driver isn't enabled, you may not. Don't worry. It's working. Give it 3-5 minutes to process. You may hear some clicks as the Pixhawk reboots. After 3-5 minutes, you will hear some tones signalling completion. It will come back to life, reconnecting with the controller.

    _If the Solo doesn't seem to complete the installation after about 5 minutes, power off the Solo and power it back on.  A few people have experienced this. It took a few power cycles to get it go through. It is unknown why this happens.  But in those cases, power cycling 1-4 times got it to go._
    

11. **Reset parameters:** Connect with Mission Planner. Go to Config/Tuning > Full Parameter List. Press the _Reset To Defaults_ button and acknowledge any prompts.  The Pixhawk will reboot.  Shortly after, the controller will reconnect. You may need to reconnect Mission Planner if it does not reconnect on it's own.
  ![MP Parameters](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/mission_planner_parameters.jpg)

12. **Load Solo Parameters:** Connect with Mission Planner. Go to Config/Tuning > Full Parameter List. Click the _load from file_ button.  Select and load the Solo parameters file (*.param) from the zip you downloaded earlier. Once the file loads, you'll probably see a lot parameter boxes in Mission Planner turn green, which is normal.  Next, press the _Write Params_ button.  Mission Planner will write all the new parameters to the Pixhawk. Once it is complete, you can disconnect and close Mission Planner.  Power cycle the Solo. It will reboot and reconnect to the controller.

13. **Install Complete!**  You have completed all the hard work.  The controller will probably be nagging about compass and level calibrations which is normal.  The lights should be in the aviation theme, red and white up front and yellow or white in the back depending on GPS status.

14. **Reassemble the Solo:** Once the installation has completed successfully, you can reassemble the Solo. Make sure you don't have any screws left over.  Make sure all the wires, including the HDMI, GPS, and motor pods are plugged back in. Again, be careful with the small green/white battery data wires.

15. **Connect and Check:** Turn the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. Run the turtle/rabbit sliders for speed and pan all the way to rabbit, then back down all the way to turtle. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be. Finally, set the sliders where you prefer to have them for flight. Go through all the settings. Touch every thing to set and verify everything. Do not assume these settings stuck from before.

16. **Calibrations:** Once all of this done, you will need to do a level calibration and a compass calibration. As of today, only the 3DR Solo app can do these functions. This is not yet in Solex.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before clicking through to the next one. Once complete, reboot the Solo.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once complete, reboot the Solo.

17. **FLY!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)
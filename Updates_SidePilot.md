![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Installing Updates Using SidePilot
-----------------------------------------------
These instructions are for installing subsequent updates to the Solo. _This is NOT for first time installs of the Green Cube and ArduCopter master_. These instructions use the SidePilot application on iOS.  No need for Mission Planner, WinSCP, Filezilla, SSH, or a complicated passwords.

1. Launch SidePilot & connect to Solo.

2. With your device connected to the internet: In the SidePilot menu all the way at the bottom, select `Help & Settings`.

3. Scroll to the bottom of the Help & Settings page and select '3DR Solo Firmware Upgrade'

4. If connected to Solo, your current firmware version will display, as well as the latest version available. You must have an internet connection.

5. Select 'Download Firmware Update'. The package will be downloaded to your device. Once downloaded the 'First Time Bootloader' and 'Intall Update' buttons will become available.
    * If this step fails, check your internet connection and try again.

6. Select 'Install Update'. All the files will be copied to the Solo in all the right places.

7. When prompted, turn Solo off and back on to reboot manually.
    * During boot the firmware files will be installed, this may take a while. Dont worry. It's working.
    * You will probably not see the multi-color disco lights usually associate with firmware updates on the solo. Don't worry. It's working.
    * Give it up to 5 minutes to process this awesomeness. You may hear some clicks as the Pixhawk reboots.
    
8. **Installation complete!** After 3-5 minutes, it will come back to life, reconnecting with the controller and applications. 

9. If a parameter reset has been recommended: With the SidePilot app reconnected to the Solo, navigate to the Parameters menu, and tap 'Load Params'. Once all parameters are loaded, go back to the Firmware Update menu and click the `Reset Parameters` button. When prompted, power off the Solo and power it back on. Calibrations will need to be redone in step 11.

10. **Connect and Check:** Tun the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. 

11. **Calibrations:** Once all of this done, you will need to do a level calibration and a compass calibration. You can do this in the SidePilot app by navigating to the Calibration menu and performing an Accelerometer and then a Compass calibration.
    * Do the accelerometer calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before tapping next. Once complete, turn Solo off and on.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once complete, turn Solo off and on.

12. **FLY!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)

![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Installing Updates Using Solex
-----------------------------------------------
These instructions are for installing subsequent updates to the Solo. _This is NOT for first time installs of the Green Cube and ArduCopter master_. These instructions use the Solex application on Android.  No need for Mission Planner, WinSCP, Filezilla, SSH, or a complicated passwords.

1. With your device connected to the internet: In the Solex menu all the way at the bottom, select `Firmware Updates`.

2. If the available packages are not shown, click refresh. But they should load automaically as long as you have an internet connection.

3. Click the package you wish to download.  The _available_ status will change to _downloaded_.

4. Connect you Android devices to the Solo if you aren't already. Make sure Solex shows _connected to vehicle_.

5. In the Firmware Updates menu, click the package you previously downloaded.

6. Read the notice and select `install`. All the files will be copied to the Solo in all the right places.

7. When prompted, click `reboot vehicle`.
    * The solo will disconnect from the controller and app. Don't worry. It's working.
    * It will probably do the radio connection lost blinking LEDs since the companion computer is not connected to the pixhawk anymore. Don't worry. It's working.
    * You will probably not see the multi-color disco lights usually associate with firmware updates on the solo. Don't worry. It's working.
    * Give it up to 5 minutes to process this awesomeness. You may hear some clicks as the Pixhawk reboots.
    
8. **Installation complete!** After 3-5 minutes, it will come back to life, reconnecting with the controller and applications. 

9. If a parameter reset has been recommended: With the Solex app reconnected to the Solo, click the `Reset Params` button on the Firmware Update screen of Solex.  When prompted, power off the Solo and power it back on. Calibrations will need to be redone in step 11.

10. **Connect and Check:** Tun the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. Run the turtle/rabbit sliders for speed and pan all the way to rabbit and back down all the way to turtle. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be.  Go through all the settings. Touch every thing to set and verify everything. Do not assume these settings stuck from before. 

11. **Calibrations:** If you reset the parameters, you will need to redo the calibrations. If anything seems unstable in flight, you should redo the calibrations. As of today, only the 3DR Solo app can do these functions. This is not yet in Solex.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before clicking through to the next one. Once complete, reboot the Solo.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once complete, reboot the Solo.

12. **FLY!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)
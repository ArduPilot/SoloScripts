![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Initial First Time Install Using the SidePilot App
-----------------------------------------------
These instructions are for first time installs of the Green Cube and ArduCopter master.  This is only for the initial install. These instructions use the SidePilot application on iOS.  No need for Mission Planner, WinSCP, Filezilla, SSH, or a complicated passwords.

1. **Your solo should be in safe working order before you start**. It should not be malfunctioning or unreliable before you even begin. It must be up to date with the latest 3DR firmware. You cannot do this with a straight out of the box Solo. You must go through the full pre-flight update first on a new Solo.  Once your Solo is up to date and working well, you're ready to begin.

2. Launch SidePilot & connect to Solo.

3. With your device connected to the internet: In the SidePilot menu all the way at the bottom, select `Help & Settings`.

4. Scroll to the bottom of the Help & Settings page and select '3DR Solo Firmware Upgrade'

5. If connected to Solo, your current firmware version will display, as well as the latest version available. You must have an internet connection.

6. Select 'Download Firmware Update'. The package will be downloaded to your device. Once downloaded the 'First Time Bootloader' and 'Intall Update' buttons will become available.
    * This may fail once or twice, simply select 'Download Firmware Update' again.

2. **Update px_uploader:** Before doing anything else, you must load the new `px_uploader.py` file onto the Solo's companion computer. This can be loaded with the SidePilot app's firmware update function really easily with a few clicks! Select 'First Time Bootloader'. This will copy over the correct files to the correct locations. Once complete, it will prompt you to reboot Solo. Simply turn Solo off and on. It will then reconnect to the controller and application after booting

   ![SidePilotScreenshot](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/SidePilot_Screenshot.jpg)

3. **Remove the battery tray:** Remove the battery and pop off the GPS cover.  Then unscrew all the small black screws around the battery tray. The battery tray can now be lifted up.  Unplug the GPS from the carrier board.  Set the battery tray aside. We highly recommend you do not lose the screws.

4. **Lift up the carrier board:** Locate the comparatively large silver screw on the right side toward the front. Unscrew that and set it aside with all the other screws that you're not going to lose.  The carrier board can not be lifted up very carefully.  You will need to fidget with the wires from the motor pods a bit.  The board will need to go up a bit, then shift back, then shift up the rest of the way. The left side can go up higher than the right, which is convenient.  It's kind of tight and generally annoying.  Be careful not to break the small wires.  Don't break any of the other wires either.  You will need to get the board high enough up to expose the pixhawk mounted underneath it.  It's the black cube looking device.

5. **Unscrew the stock pixhawk:** There are 4 very small screws on the top of the carrier board. Unscrew them and set them aside. The stock pixhawk can now be removed. It will pull down off the carrier board. Set the stock pixhawk aside somewhere safe. You will want to keep it.

6. **Install the green cube:** The green cube installs the same way the old one came off.  Plug it into the carrier board from the bottom.  Then put in the four screws.
  ![Guts](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/guts.jpg)
  
7. **Do not reassemble yet:** It is best to do the initial firmware install with the Solo still opened up. If anything goes wrong, it avoids having to disassemble it again. 

8. **Power up the Solo and connect to controller:** Put the battery onto the solo. It will just sit atop the carrier board. Obviously you should avoid manhandling the Solo while like this since the battery can just fall off. So get everything situated first.  Turn on the battery.  The solo will power up as usual. After a short while, the Solo will reconnect with the controller as usual. It will probably give you all kinds of warnings about calibration. This is normal and expected.

9. **Load the firmware and files using SidePilot**
 * In SidePilot, connect to Solo and navigate to the Firmware Updates screen. Download the updated package once more.
 * Select `Install Update`. You will be warned about performing the First Time Bootloader step. This is normal, just tap 'Continue'. All the files will be copied to the Solo in all the right places.
 * When prompted, reboot Solo. This will install the firmware file.
 * It will probably do the radio connection lost blinking LEDs since the companion computer is not connected to the pixhawk anymore. Don't worry, this is normal.
 * You will probably not see the multi-color disco lights usually associate with firmware updates on the solo. Don't worry. It's working.
 * Give it up to 5 minutes to process this awesomeness. You may hear some clicks as the Pixhawk reboots.
 * After 3-5 minutes, it will come back to life, reconnecting with the controller and applications. You will notice the lights now look like an aircraft rather than a car.
 * With the SidePilot app reconnected to the Solo, click the `Reset Parameters` button on the firmware update screen of SidePilot.  When prompted, power off the Solo and power it back on.
 * Installation complete!
 
    _If the Solo doesn't seem to complete the installation after about 5 minutes, power off the Solo and power it back on.  A few people have experienced this. It took a few power cycles to get it go through. It is unknown why this happens.  But in those cases, power cycling 1-4 times got it to go._

10. **Reassemble the Solo** once the installation has completed successfully. Make sure you don't have any screws left over.  Make sure all the wires, including the GPS, are plugged back in.

11. **Connect and Check:** Tun the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. Run the turtle/rabbit sliders for speed and pan all the way to rabbit and back down all the way to turtle. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be.  Go through all the settings. Touch every thing to set and verify everything. Do not assume these settings stuck from before. 

12. **Calibrations:** Once all of this done, you will need to do a level calibration and a compass calibration. As of today, only the 3DR Solo app can do these functions. This is not yet in Solex.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before clicking through to the next one. Once complete, reboot the Solo.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once complete, reboot the Solo.

13. **FLY!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)

![Logo](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/APsolo.jpg)

Initial First Time Install Using the Solex App
-----------------------------------------------
These instructions are for _first time installs of the Green Cube and ArduCopter master_.  This is only for the initial install. These instructions use the Solex application on Android.  No need for Mission Planner, WinSCP, Filezilla, SSH, or complicated passwords.

1. **Your solo should be in safe working order before you start**. It should not be malfunctioning or unreliable before you even begin. It must be up to date with the latest 3DR firmware. You cannot do this with a straight out of the box Solo. You must go through the full pre-flight update first on a new Solo.  Once your Solo is up to date and working well, you're ready to begin.

2. **Update python files:** Before doing anything else, you must load the new python files onto the Solo's companion computer. This can be loaded with the Solex app's firmware update function really easily with a few clicks! Select the `IMX Python Files` package. If it it says "available", Solex will download it. Once it says "downloaded, click the file and select install. When prompted, power cycle the solo.  The files are compiled on reboot. It is critical that this step take places _before you install the Green Cube in your solo!_
   ![Solex Packages](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/Solex_Packages.png)

3. **Remove the battery tray:** Remove the battery and pop off the GPS cover.  Then unscrew all the small black screws around the battery tray. The battery tray can now be lifted up.  Unplug the GPS from the carrier board.  Set the battery tray aside. We highly recommend you do not lose the screws.
   ![Battery Tray Screws](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/battery_tray_screws.jpg)

4. **Lift up the carrier board:** Locate the comparatively large silver screw on the right side toward the front. Unscrew that and set it aside with all the other screws that you're not going to lose.  The carrier board can not be lifted up very carefully.  You will need to fidget with the wires from the motor pods a bit.  The board will need to go up a bit, then shift back, then shift up the rest of the way. The left side can go up higher than the right, which is convenient.  It's kind of tight and generally annoying.  Be careful not to break the small wires.  Don't break any of the other wires either.  You will need to get the board high enough up to expose the Pxhawk mounted underneath it.  It's the black cube looking device.
   ![carrier screw](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/carrier_retainer_screw.jpg)
   ![wires](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/carrier_board_wires.jpg)

5. **Unscrew the stock pixhawk:** There are 4 very small screws on the top of the carrier board. Unscrew them and set them aside. The stock Pixhawk can now be removed. It will pull down off the carrier board. Set the stock Pixhawk aside somewhere safe. You will want to keep it.
   ![Pixhawk screws](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/pixhawk_screws.jpg)

6. **Install the green cube:** The green cube installs the same way the old one came off.  Plug it into the carrier board from the bottom.  Then put in the four screws.
  ![cube installed](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/cube_installed.jpg)
  
7. **Do not reassemble yet:** It is best to do the initial firmware install with the Solo still opened up. If anything goes wrong, it avoids having to disassemble it again. 

8. **Power up the Solo and reconnect to controller:** Put the battery onto the solo. It will just sit atop the carrier board. Obviously you should avoid manhandling the Solo while like this since the battery can just fall off. So get everything situated first.  Turn on the battery.  The solo will power up as usual. After a short while, the Solo will reconnect with the controller as usual. It will probably give you all kinds of warnings about calibration. This is normal and expected.

9. **Load the firmware and parameters using Solex**
 * In the Solex menu all the way at the bottom, select `Firmware Updates`.
 * While your device has an internet connection, hit the refresh button to pull down the latest from the server.
 * While your device has an Internet connection, click the required packages to download them. They are `Wipe_New_Pixhawk_Firmware.zip`, `ArduCopter_x_Firmware.zip`, and `ArduCopter_x_parameters.zip`. The available status will change to downloaded for each one.
 * If not already, reconnect to the Solo's WiFi and make sure Solex says it's connected to vehicle.
 * **Wipe The Pixhawk:** In the Solex firmware updates menu, tap the `Wipe_New_Pixhawk_Firmware` package. Read the notice and select `install`. All the files will be copied to the Solo in all the right places. When prompted, power cycle the Solo. It will reboot, then switch into bootloader mode. Normally you will see disco lights while it's doing this. But if the LED driver isn't enabled, you may not. Don't worry. It's working. Give it 3-5 minutes to process. You may hear some clicks as the Pixhawk reboots. After 3-5 minutes, you will hear some tones signalling completion. It will come back to life, reconnecting with the controller and Solex. 
 * **Install ArduCopter:** In the Solex firmware updates menu, tap the `ArduCopter_x_Firmware` package. Read the notice and select `install`. All the files will be copied to the Solo in all the right places. When prompted, power cycle the Solo. It will reboot, then switch into bootloader mode. Normally you will see disco lights while it's doing this. But if the LED driver isn't enabled, you may not. Don't worry. It's working. Give it 3-5 minutes to process. You may hear some clicks as the Pixhawk reboots. After 3-5 minutes, you will hear some tones signalling completion. It will come back to life, reconnecting with the controller and Solex. 
 * **Reset Parameters:** With the Solex app reconnected to the Solo, click the `Reset Params` button on the firmware update screen of Solex.  When prompted, power cycle the solo.
 * **Load Parameters:** With the Solex app reconnected to the Solo, click the `ArduCopter_x_parameters` package. Read the notice and select `install`.  When prompted, power cycle the Solo.
 * **Complete:** The solo will reboot and reconnect to the controller and apps.  You will notice the LEDs now look like an aircraft rather than a car. Installation complete!
 
    _If the Solo doesn't seem to complete the firmware installations after about 5 minutes, power off the Solo and power it back on.  A few people have experienced this. It took a few power cycles to get it go through. It is unknown why this happens.  But in those cases, power cycling 1-4 times got it to go._

10. **Reassemble the Solo** once the installation has completed successfully. Make sure you don't have any screws left over.  Make sure all the wires, including the GPS and motor pods, are plugged back in.

11. **Connect and Check:** Tun the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. Run the turtle/rabbit sliders for speed and pan all the way to rabbit and back down all the way to turtle. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be.  Go through all the settings. Touch every thing to set and verify everything. Do not assume these settings stuck from before. 

12. **Calibrations:** Once all of this done, you will need to do a level calibration and a compass calibration. Solex v1.4.9 and higher now has these calibrations, making the 3DR Solo app no longer required for this step. In Solex, the "level calibration" is called IMU Calibration.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before clicking through to the next one. It must remain perfectly still when you push the button. Once calibration is complete, you must reboot the Solo.
    * The compass calibration must be done outdoors in an open area, away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once calibration is complete, you must reboot the Solo.
    ![Calibrations](https://github.com/ArduPilot/SoloScripts/blob/master/Misc/solex_cals.jpg)

13. **FLY!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)
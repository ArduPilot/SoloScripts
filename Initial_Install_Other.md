![Logo](https://github.com/Pedals2Paddles/SoloBeta/blob/master/Misc/APsolo.jpg)

Instructions
------------
These instructions currently assume you already know how to use things like Mission Planner and WinSCP or Filezilla. This method is somewhat complicated compared to using Solex. But this does work. Please read carefully and follow all steps in order.

1. **Your solo should be in safe working order before you start**. It should not be malfunctioning or unreliable before you even begin. It must be up to date with the latest 3DR firmware. You cannot do this with a straight out of the box Solo. You must go through the full pre-flight update first on a new Solo.  Once your Solo is up to date and working well, you're ready to begin.

2. **Update px_uploader:** Before doing anything else, you must load the new `px_uploader.py` file onto the Solo's companion computer. We're going to load all the python files while we're at it though. Use WinSCP, Filezilla, or other SCP/SSH application to put all the python files (`*.py`) in the /usr/bin/ directory of the companion computer, overwriting the ones that are there now.  Once you've copied them in, you will need to reboot the Solo for them to take effect. You don't need to keep redoing this every time you reset parameters or install new ArduCopter px4 files. These file will never change or revert unless you do a complete factory reset.

3. **Remove the battery tray:** Remove the battery and pop off the GPS cover.  Then unscrew all the small black screws around the battery tray. The battery tray can now be lifted up.  Unplug the GPS from the carrier board.  Set the battery tray aside. We highly recommend you do not lose the screws.

4. **Lift up the carrier board:** Locate the comparatively large silver screw on the right side toward the front. Unscrew that and set it aside with all the other screws that you're not going to lose.  The carrier board can not be lifted up very carefully.  You will need to fidget with the wires from the motor pods a bit.  The board will need to go up a bit, then shift back, then shift up the rest of the way. The left side can go up higher than the right, which is convenient.  It's kind of tight and generally annoying.  Be careful not to break the small wires.  Don't break any of the other wires either.  You will need to get the board high enough up to expose the pixhawk mounted underneath it.  It's the black cube looking device.

5. **Unscrew the stock pixhawk:** There are 4 very small screws on the top of the carrier board. Unscrew them and set them aside. The stock pixhawk can now be removed. It will pull down off the carrier board. Set the stock pixhawk aside somewhere safe. You will want to keep it.

6. **Install the green cube:** The green cube installs the same way the old one came off.  Plug it into the carrier board from the bottom.  Then put in the four screws.
   ![Guts](https://github.com/Pedals2Paddles/SoloBeta/blob/master/Misc/guts.jpg)

7. **Do not reassemble yet:** It is best to do the initial firmware install with the Solo still opened up. If anything goes wrong, it avoids having to disassemble it again. 

8. **Power up the Solo and connect to controller:** Put the battery onto the solo. It will just sit atop the carrier board. Obviously you should avoid manhandling the Solo while like this since the battery can just fall off. So get everything situated first.  Turn on the battery.  The solo will power up as usual. After a short while, the Solo will reconnect with the controller as usual. It will probably give you all kinds of warnings about calibration. This is normal and expected.

9. **Load the firmware**
 * Use an app such WinSCP or Filezilla connected to the Solo.
 * Copy the `.px4` file into the Solo's `/firmware/` directory.
 * Disconnect from the file transfer app.
 * Power off the Solo and power it back on.
 * It will detect the new file on boot, and go into bootloader. Give it time as it does its thing. This process takes approximately 5 minutes. There will be lots of colorful lights and beeping. Once it is done, it will play some musical tones and be ready for your input. If you've ever loaded the old 1.5.3 firmware on the Solo as described in the forms, this is the same procedure.
 * After a short while, the controller will reconnect to the Solo.  Occassionally it gets lazy and both need to be power cycled to wake them up, which is nothing to worry about.
 * After you've loaded the firmware, you must do a full parameter reset. Reconnect with Mission Planner. In Mission Planner's full parameter list, click the reset to defaults button on the right. The Pixhawk will reboot on it's own, with all the defaults taking over. After a short while, the controller will reconnect to the Solo.  Occassionally it gets lazy and both need to be power cycled to wake them up, which is nothing to worry about. If "Full Parameter List" is not visible on the "Config/Tuning" screen, select "Planner" and set Layout to "Advanced". Restart Mission Planner. 
 * Installation complete!
 
    _If the Solo doesn't seem to complete the installation after about 5 minutes, power off the Solo and power it back on.  A few people have experienced this. It took a few power cycles to get it go through. It is unknown why this happens.  But in those cases, power cycling 1-4 times got it to go._

10. **Reassemble the Solo** once the installation has completed successfully. Make sure you don't have any screws left over.  Make sure all the wires, including the GPS, are plugged back in.

11. **Connect and Check:** Tun the Solo back on. Connect with any and all apps you plan to use (3DR, Solex, Side Pilot, etc) and test functionality. Run the turtle/rabbit sliders for speed and pan all the way to rabbit and back down all the way to turtle. These sliders make changes to the parameters. Running the sliders up and down ensure those parameters are set the way they should be.  Go through all the settings. Touch every thing to set and verify everything. Do not assume these settings stuck from before. 

12. **Calibrations:** Once all of this done, you will need to do a level calibration and a compass calibration. As of today, only the 3DR Solo app can do these functions. This is not yet in Solex.
    * Do the level calibration first on a decently level surface, such as a table. For each orientation, place Solo down gently, and let it settle for about 5 seconds before clicking through to the next one. Once complete, reboot the Solo.
    * The compass calibration must be done outdoors and away from structures, vehicles, and other metal objects. This applies to any vehicle running any firmware, not just a Solo, and not just ArduCopter master. Once complete, reboot the Solo.

13. **FLY!!** Once all of the above is complete, you are ready to fly! You should make your first few flights in a safe, open, and clear area. Start off low and slow. Run through the basics to function test everything.  Make sure the Solo is operating smoothly, reliably, safely, and as intended.

[Back To Main](../master/README.md)
EXPERIMENTAL
------------

This will do a full file system update to the Solo.  This includes the latest 3DR 2.4.2, the required updated python files, and ArduCopter 3.5.0.  This will also update the Factory Reset (golden image) partition to match. So if you factory reset, you go back to a useful and flyable baseline rather than a circa 2015 unflyable thing.  No need for an internet update or 3DR servers ever again.

**If you already have a Green Cube installed:** You should install this now.  It will not hurt and can only help.

**If you are doing a new Green Cube install:** This replaces all those complicated steps.  The new procedure will go something like this:
1. Remove stock cube
2. Install Green Cube
3. Power up, connect, install this upgrade package
4. Done

I have not put this up for public consumption on Solex yet. We need some people to test it out. To test this out on Solex manually:

1. Update Solex to the latest from the play store (v1.5.3 as of today)
2. Copy the above zip (`Green Cube Full Upgrade.zip`) into the `/Solex/download/packages/` directory on your device. The actual location of this directory structure varies by device and whether it has a real removable SD card or not.  I have faith you can find it.
3. Connect to Solo with Solex. The initial parameter refresh when Solex opens must finish before you can go into FW Updates.
4. Run the Green Cube Full Update in Solex FW Updates.
5. Files will copy to Solo.  Then the script will execute.  Once the script is done, the Solo will reboot and continue with the install. Let it go. The disco lights may or may not happen. The gimabl will come on and off a few times.  The pixhawk will reboot at least once.

When it's done, the lights will come on as usual, the gimbal will level, and the controller will reconnect.  Power cycle the controller if it doesn't reconnect automatically.

**Note:** This package is 74MB so all aspects will take longer.  When you click the buttons, it may seem like nothing is happening. Just be patient. It will go.
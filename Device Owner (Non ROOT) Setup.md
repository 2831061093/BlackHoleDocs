### Device Owner (Non ROOT) Mode Setup

1. Make sure your phone running Android  5.0+ and you know how to use [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) clearly.
2. Go to "Settings > Accounts", remove **all accounts** including your Google account.
3. If multi-user or guest mode has been set on your device, also need to be closed or deleted
4. Run ```adb shell dpm set-device-owner com.hld.apurikakusu/.receiver.DPMReceiver``` on your computer.
5. If you see the words Success, you can open the BlackHole to use (may need to restart your phone) , then you can add your accounts and guest mode back.

### FAQ

- **Q: It shows "no devices/emulators found"**
- A: USB debugging is not turned on, or the USB is not connected properly..

- **Q: It shows "Not allowed to ... already several users on the device"**
- A: Please follow step 2 and remove the guest mode.

- **Q: It shows "Trying to set the device owner, but device owner is already set"**
- A: You have set up other app using Device Owner mode, please cancel the settings of other app.
</br>**Added: You can use the command ```adb shell pm list users``` view the accounts, use the command ```adb shell pm remove-user user id``` to delete the account.**

- **Q: There is "Device is managed by your organization" on my notification center after setting up. Why?**
- A: That is how BlackHole works.

- **Q: How to uninstall BlackHole?**
- A: Just select "Uninstall" in the settings of BlackHole.



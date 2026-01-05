# Onyx Boox Palma 2 Pro tips & tricks

## Enabling app to run in background

Sometimes when you have a computer in your pocket, running pretty complex operating system you want to enable multitasking on it.  
This is used for apps like music player, podcasts, messaging apps, smartwatch app, and many more!  
Fortunately it is possible in these days! And as you will see - also easy.

### Chapter 1 - eInk Wise

You need to enable option `Stay active in the background` in eInk Wise center.

There are two possible ways how to get to required settings menu

#### Option 1
- Longpress on app icon  
![Long press](screenshots/pwr01_app.png "Long press")

- Select `Optimize` from menu  
![Optimize](screenshots/pwr02_app_menu.png "Long press")

#### Option 2
- Open the app you want to configure

- Display `eInk Wise` overlay

- Tap small cogwheel next to selected eInkWise profile  
![eInkWise](screenshots/pwr03_einkwise.png "eInkWise")


Both these options brings you to app profile in eInk Wise.

>[!WARNING]  
>Remember this setting is tied to specific profile for that app. If you change profile from `Customize` to `Recommended` or `Fast` settings including background running will be different (probably default => running in background disabled).  
>You have to customize settings for all profiles, or be sure that profile for that app never changes.  
>You can of course take advantage of this feature. Creating profile with and without background running enabled. Then switch app to run in background mode only when you want to (for example when you are going to listen audiobook or something)

- In eInk Wise profile tap on `Others`  
![eInkWise settings](screenshots/pwr04_einkwise_settings.png "eInkWise settings")

- On `Others` tab enable `Stay active in the background` option
![eInkWise others](screenshots/pwr05_einkwise_runinbgr.png "eInkWise others")

### Chapter 2 - Onyx Settings

Now let's disable `App freezing` and enable `Autostart` for our app.

- From Boox launcher or top tray select `Settings`  
![Boox Settings](screenshots/pwr06_boox_settings.png "Boox Settings")

- In `Settings` menu select `Apps & Notifications`  
![Boox Settings menu](screenshots/pwr07_boox_settings_menu.png "Boox Settings menu")

- Then select `Freeze Settings`  
![Boox Settings freeze](screenshots/pwr08_boox_apps_settings.png "Boox Settings freeze")

- Disable `Freezing` for selected app  
![Disable freeze](screenshots/pwr09_boox_freezemenu.png "Disable freeze")

- Now return back to `Apps & Notifications` and select `App Startup`  
![Boox Settings startup](screenshots/pwr10_boox_apps_settings2.png "Boox Settings startup")

- And enable `Autostart` for selected app  
![Enable startup](screenshots/pwr11_boox_autostart.png "Enable startup")

### Chapter 3 - Android Settings

Now for the more tricky part. You need to access standard `Android setting`. But those are unaccessible from Boox launcher.  
But since everyone played Dark Souls these days, this cannot stop anyone.  
Just install any other launcher of your choice (do not set it as default - it has a reason you will soon find out if you do).  
I will use `Nova Launcher` for example.

- Start launcher of your choice  
![Launcher](screenshots/pwr12_launcher.png "Launcher")

- Start `Settings` app from launcher (not from top tray!)  
![Android settings](screenshots/pwr13_real_settings.png "Android settings")

- This will bring you to `Android Settings` where you need to select `Apps`
![Android settings - apps](screenshots/pwr14_android_settings.png "Android settings - apps")

- Select app you need to allow to run in background
![Select app](screenshots/pwr15_android_appsettings.png "Select app")

- On app settings page (I changed app name on purpose) scroll down  
![App settings](screenshots/pwr16_android_settings_app.png "App settings")

- Disable `Manage app if unused`
![App - disable manage](screenshots/pwr17_android_app_disableunused.png "App - disable manage")

- Now scroll back up and enter `App battery usage` submenu
![App - battery settings](screenshots/pwr18_android_settings_app2.png "App - battery settings")

- Inside `App battery usage` submenu tap on `Allow background usage` text (box next to it should say enabled - this is done by eInkWise)  
![App - battery settings hidden](screenshots/pwr19_app_batteryusage.png "battery settings hidden")

- Clicking on text opens another menu where you need to set `Unrestricted` option  
![App - unrestricted on background](screenshots/pwr20_app_battery_unresticted.png "unrestricted on background")

- Now return back to `App info` screen and select `Permissions`  
![App - permissions](screenshots/pwr21_android_settings_app3.png "App - permissions")

- Disable `Pause app activity if unused`
![App - diable pause](screenshots/pwr22_app_disablepause.png "App - diable pause")

### Epilogue

:confetti_ball: :fireworks:  
If you reached this point, then congrats! You just enabled single app to run on background and not be killed by power management!

As you just witnessed, it is just easy and intuitive.  
Who needs some toggle button, when you have this beautiful UI designed by mad genius?!

## Enabling notifications for all apps

Since on Android some apps needs `Google Services` to show local notifications (why?) on the device and Palma 2 Pro does not have them, you must use another solution. Some info for example is [here](https://github.com/krille-chan/fluffychat/wiki/Push-Notifications-without-Google-Services)

For these purposes you can use [SunUp](https://unifiedpush.org/users/distributors/sunup/), [ntfy](https://unifiedpush.org/users/distributors/ntfy/), or some other implementation.  
I choosed SunUp because my favorite messaging app has some [weird bug](https://github.com/krille-chan/fluffychat/issues/1314#issuecomment-2336777629) with ntfy.

> [!NOTE]  
> You will need to enable notification app to [run in background](#enabling-app-to-run-in-background)

## Phone calls and SMS on Palma 2 Pro

Since system update `2025-12-27_14-24_4.1.1-rel_12272` (there are [some reports about earlier](https://www.reddit.com/r/eink/comments/1ptmhz7/phone_calls_available_on_palma2_pro/) ) device is capable of calling and SMS messages without any modifications.  
While SMS reception and sending is reliable as I tested so far. This is not same for receiving calls. So it is still not enough to be used as reliable phone!

You only have to install some dialer app and SMS app. And set them as default dialer/sms app.  
Dialer examples: [Amadz](https://f-droid.org/packages/com.talsk.amadz/), [Fossify Phone](https://f-droid.org/packages/org.fossify.phone/), [Google Dialer](https://play.google.com/store/apps/details?id=com.google.android.dialer)  
SMS app examples: [Fossify Messages](https://f-droid.org/packages/org.fossify.messages/), [QUIK](https://f-droid.org/packages/dev.octoshrimpy.quik.fdroid/), [Google Messages](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging).

> [!NOTE]  
> You will need to enable dialer and messaging app to [run in background](#enabling-app-to-run-in-background)

Known problems:

- When device goes to sleep/lockscreen, is is unable to receive calls. If you call number on Palma 2 Pro, you will get `LINE BUSY` signal. But SMS bessages are somehow received in sleep mode.
- There are no settings in Onyx Power Settings that will allow `Stay Connnected` to mobile network in sleep state (as it does for Wifi or Bluetooth)
- Device does calling (incoming or outgoing) over GSM network. There is no VoLTE or VoWifi support so far. When you are in area where is no GSM network, you will be not able to use calling. (Which is not rare in my country) 

## How to restore Palma 2 Pro if not booting to Android

If you somehow bricked your Palma and have backup there is still hope!  
You are probably stuck with unresponsive device with BOOX logo on the screen.

- first connect device to computer and check if it is in fastboot mode with `fastboot getvar all`

- If you are able to get some output, get [edl](https://github.com/bkerler/edl) utility (which you probably already have)

- Leave device connected to computer and issue some `edl` command using correct loader. Example: `edl --loader=palma2pro.bin printgpt`

- Now pres and hold `Power button` on your Palma until device reboots - screen will flash

- Immediately release power button and press and hold VolUp + VolDown until you see device is recognized by computer. Then release buttons.

- Now you will be able to flash backup and restore device functionality

>[!WARNING]  
>For some reason I encountered behavior that even after restore Palma refused to boot. Setting active boot partition to secondary and then back was needed.  
>Can be done this way:
>```
>edl --loader=palma2pro.bin setactiveslot a
>edl --loader=palma2pro.bin reset
>edl --loader=palma2pro.bin setactiveslot b
>edl --loader=palma2pro.bin reset
>```

## Rooting Palma 2 Pro

Used sources: [Palma2Root guide issue](https://github.com/jdkruzr/BooxPalma2RootGuide/issues/9), [eOS documentation - Install on FP4](https://doc.e.foundation/devices/FP4/install), [MobileRead thread](https://www.mobileread.com/forums/showthread.php?t=371138)

>[!WARNING]  
>This procedure will wipe your data on device! Be prepared.  
>Rooting and modifying device is dangerous. Do this on your risk. You can cause device will be unable to boot.  
>It is probably good idea to buy some pre-made EDL cable to be prepared when things goes wrong!

### Preparing tools

Get [edl](https://github.com/bkerler/edl) utility

Get Palma loader file for EDL utility: `wget -O palma2pro.bin 'https://github.com/bkerler/Loaders/raw/refs/heads/main/lenovo_motorola/0000000000000000_bdaf51b59ba21d8a_fhprg.bin'`

Get latest available eOS build for Fairphone 4 Android 15 from [eOS site](https://images.ecloud.global/community/FP4/). I used [this](https://images.ecloud.global/community/FP4/IMG-e-3.3-a15-20251213556761-community-FP4.zip) specifically.

From that Fairphone 4 image, extract `abl.img` somewhere. I will reference it as `abl-fp4.img` in the process.

Reboot phone into bootloader with `adb reboot bootloader`, then issue `fastboot getvar current-slot`. And note down that letter. For me it was and rest of the guide I will be using slot `a`. Do adjust those commands for your active slot.

### Backing up data

Put the device into EDL mode with `adb reboot edl`

Now do the backup of the device. Best way how to do that is backing up all partitions. (except userdata - will be wiped anyway)  
It takes about 15 minutes and takes ~9GB disk space. Can be done with command (folder `stock_partitions_backup` must exists):  
`edl --loader=palma2pro.bin --memory=ufs rl stock_partitions_backup/ --skip=userdata`  
If you do this you can skip next step with backing all partitions again and adjust partitipn paths to this whole backup.

Now let's backup the important stuff only. This cannot be skipped:  
```
mkdir stock_backup
edl --loader=palma2pro.bin --memory=ufs r devinfo stock_backup/devinfo.img
edl --loader=palma2pro.bin --memory=ufs r boot_a stock_backup/boot_a.img
edl --loader=palma2pro.bin --memory=ufs r boot_b stock_backup/boot_b.img
edl --loader=palma2pro.bin --memory=ufs r vbmeta_a stock_backup/vbmeta_a.img
edl --loader=palma2pro.bin --memory=ufs r vbmeta_b stock_backup/vbmeta_b.img
edl --loader=palma2pro.bin --memory=ufs r vbmeta_system_a stock_backup/vbmeta_system_a.img
edl --loader=palma2pro.bin --memory=ufs r vbmeta_system_b stock_backup/vbmeta_system_b.img
edl --loader=palma2pro.bin --memory=ufs r recovery_a stock_backup/recovery_a.img
edl --loader=palma2pro.bin --memory=ufs r recovery_b stock_backup/recovery_b.img
edl --loader=palma2pro.bin --memory=ufs r abl_a stock_backup/abl_a.img
edl --loader=palma2pro.bin --memory=ufs r abl_b stock_backup/abl_b.img
```

### Unlocking bootloader

Unfortunately Boox firmware does not allow unlocking device. But since hardware is similar to Fairphone 4 we will take Fairphone image to help.

Get into edl mode again with `adb reboot edl`. Then issue those commands to write FP4 ABL into Palma (not sure why, but for me it was needed to write into both slots):  
```
edl --loader=palma2pro.bin --memory=ufs w abl_a abl-fp4.img
edl --loader=palma2pro.bin --memory=ufs w abl_b abl-fp4.img
```

Now use your activeslot you noted before (my palma was not booting without this) and reboot device:  
```
edl --loader=palma2pro.bin setactiveslot a
edl --loader=palma2pro.bin reset
```

Go into android settings. You can use command `adb shell am start -a android.settings.SETTINGS` to do that. Or use method described in [run in background guide](#chapter-3---android-settings).  
Select `System` submenu.  
![System settings](screenshots/rooting1_system_settings.png "System settings")  
Then select `Developer options`.  
![Developer settings](screenshots/rooting2_developer_settings.png "Developer settings")  
In those go to Developer options enable `OEM unlocking`.  
![Enable unlocking](screenshots/rooting3_enable_unlocking.png "Enable unlocking")

Reboot the device.

Now we will proceed to unlocking bootloader. Your data will be WIPED from the device. There is no going back! Ready?

Reboot into bootloader with `adb reboot bootloader`.

You should get BOOX logo on screen and command `fastboot devices` should see the device.

Issue `fastboot flashing unlock` to begin unlocking.  
On screen there will still bee BOOX logo, nothing visible.  
Press `Vol Up` once, and then `Power button`.  
Now device will automatically reboot few times and wipes all your data.

Now you are with clear device in defaults. Enable ADB in settings again. And issue `adb reboot bootloader`.

Issue `fastboot flashing unlock_critical`.  
AGAIN: On screen there will still bee BOOX logo, nothing visible.  
Press `Vol Up` once, and then `Power button`.  
Device will automatically reboot few times and wipes all your data once again.

Now you have unlocked device. `fastboot oem device-info` should say something like:  
```
(bootloader) Verity mode: true
(bootloader) Device unlocked: true
(bootloader) Device critical unlocked: true
(bootloader) Charger screen enabled: true
```

### Rooting with Magisk

From now the rooting procedure can be done as on [Palma 2](https://github.com/jdkruzr/BooxPalma2RootGuide).

Install [Magisk](https://github.com/topjohnwu/Magisk/releases/) to your Palma

Push your backed up boot image for your activeslot onto Palma `adb push stock_backup/boot_a.img /sdcard/`

Patch the boot image using Magisk in your phone. Note the filename and use it in next command.

Then download it back to your computer: `adb pull /sdcard/Download/magisk_patched-30600_x1Hl9.img boot_a_patched.img`

Reboot Palma into EDL mode: `adb reboot edl`

Write modified image into Palma and reboot it:  
```
edl --loader=palma2pro.bin --memory=ufs w boot_a boot_a_patched.img
edl --loader=palma2pro.bin reset
```

Congrats! Your Palma is rooted now!

If you want, you can now flash back the stock ABL images back into Palma.  
I do recommend it, because without it, device was kinda unstable and for example launching Onyx settings from top-tray did not worked (after flashing original ABL it did worked)
```
edl --loader=palma2pro.bin --memory=ufs w abl_a stock_backup/abl_a.img
edl --loader=palma2pro.bin --memory=ufs w abl_b stock_backup/abl_b.img
```

## How to get into recovery menu

Source: [Boox support](https://help.boox.com/hc/en-us/community/posts/39889271676948-Palma-2-Factory-Reset) [video](https://drive.google.com/file/d/1Mu-mD0hE7L09MH52Oq13iGLPQM-NFXbB/view?pli=1)

- When turned off, long-press power button until screen blinks

- Release the power button and then press it again for 5 sec

- Release the power button and short-press 6 times

- If you end up with white screen, pres `Vol Down` once


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

## Rooting Palma 2 Pro - In progress

Any help appreciated. Let's discuss that on [MobileRead](https://www.mobileread.com/forums/showthread.php?t=371138)

## How to get into recovery menu

[source](https://drive.google.com/file/d/1Mu-mD0hE7L09MH52Oq13iGLPQM-NFXbB/view?pli=1)

- When turned off, long-press power button until screen blinks

- Release the power button and then press it again for 5 sec

- Release the power button and short-press 6 times

- If you end up with white screen, pres `Vol Down` once


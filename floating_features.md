# Floating Feature Tweaks 🍀
Add these lines in system/etc/floating_feature.xml (One UI 4.x +)  or vendor/etc/floating_feature.xml (One UI <= 4.1).

# Some Useful stuffs :

### 01. Enable Flagship Launcher Animations
> [!NOTE]  
> - Search for the following line in floating_feature.xml ```<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>``` And change value from "LowEnd" or "Mass" to "HighEnd" (Mass is used widely on the mid-rangers)
```
<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>HighEnd</SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>
```

### 02. Enable Processing Speed
> [!NOTE]  
> - Could cause the device to heat and may have bigger battery consuption.
```
<SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_ENHANCED_PROCESSING>TRUE</SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_ENHANCED_PROCESSING>
```

### 03. Nuke system logging stuffs.
> [!NOTE]  
> - Search for the following line in floating_feature.xml ```<SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_MESSAGE_LOGS>``` And change value from "TRUE" to "FALSE" and it should look like the one in the below.
```
<SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_MESSAGE_LOGS>FALSE</SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_MESSAGE_LOGS>
```

> [!NOTE]  
> - Besure to add or change the value of the below mentioned flag too.
```
<SEC_FLOATING_FEATURE_SYSTEM_CONFIG_SYSINT_DQA_LOGLEVEL>0</SEC_FLOATING_FEATURE_SYSTEM_CONFIG_SYSINT_DQA_LOGLEVEL>
```

### 04. Enable Performance Profile
> [!NOTE]  
> - Could cause the device to heat and may have bigger battery consuption.
```
<SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_LOW_HEAT_MODE>TRUE</SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_LOW_HEAT_MODE>
```

### 05. Enable High Performance Mode
> [!NOTE]  
> - Could cause the device to heat and may have bigger battery consuption.
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_HIGH_PERFORMANCE_MODE>TRUE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_HIGH_PERFORMANCE_MODE>
<SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_ENHANCED_CPU_RESPONSIVENESS>TRUE</SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_ENHANCED_CPU_RESPONSIVENESS>
```

### 06. Enable Extra Screen Modes (Might break the original amoled colors)
> [!NOTE]  
> Step 1 - Search for this line ```<SEC_FLOATING_FEATURE_LCD_SUPPORT_MDNIE_HW>``` and make it's value from "TRUE" to "FALSE"
> Step 2 - Search for this line ```<SEC_FLOATING_FEATURE_LCD_SUPPORT_WIDE_COLOR_GAMUT>``` and make it's value from "TRUE" to "FALSE"

### 07. Enable Smooth Scroll of Surface Flinger
```
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SMOOTH_SCROLL>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SMOOTH_SCROLL>
```

# Display :

### 01. Enable Flagship Edge Lighting+ Animations (Needs OneUI 2.x)
> [!NOTE]  
> - Search for the following line in floating_feature.xml ```<SEC_FLOATING_FEATURE_COMMON_CONFIG_EDGE>``` And remove  "-basic_lighting" line, then it should look like the one below.
```
<SEC_FLOATING_FEATURE_COMMON_CONFIG_EDGE>people,task,circle,panel,-edgefeeds,edgelighting_v2,debug,cornerR:6.2,search,phonecolor,dot_bottom</SEC_FLOATING_FEATURE_COMMON_CONFIG_EDGE>
```

### 02. Enable Flagship Edge Lighting+ Animations (Needs OneUI 3.x)
```
<SEC_FLOATING_FEATURE_SYSTEMUI_CONFIG_EDGELIGHTING_FRAME_EFFECT>frame_effect</SEC_FLOATING_FEATURE_SYSTEMUI_CONFIG_EDGELIGHTING_FRAME_EFFECT>
```

### 03. Enable AOD Clock Transition Animation
> [!NOTE]  
> - Search for the following line in floating_feature.xml ```<SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>``` And add "clocktransition" and "activeclock=4" in the following line, then it should look like the one below.
```
<SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>aodversion=7,clearcoveroff,clocktransition,activeclock=4</SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>
```

### 04. Enable Multiwindow tray
```
<SEC_FLOATING_FEATURE_COMMON_CONFIG_MULTIWINDOW_TRAY>TRUE</SEC_FLOATING_FEATURE_COMMON_CONFIG_MULTIWINDOW_TRAY>
```

### 05. Make 60Hz as the default refresh rate.
```
<SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_DEFAULT_REFRESH_RATE>60</SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_DEFAULT_REFRESH_RATE>
<SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_MODE>0</SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_MODE>
<SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_SUPPORTED_REFRESH_RATE>60</SEC_FLOATING_FEATURE_LCD_CONFIG_HFR_SUPPORTED_REFRESH_RATE>
<SEC_FLOATING_FEATURE_LCD_CONFIG_SELFMASK_VERSION>0</SEC_FLOATING_FEATURE_LCD_CONFIG_SELFMASK_VERSION>
<SEC_FLOATING_FEATURE_LCD_SUPPORT_SELFMASK>TRUE</SEC_FLOATING_FEATURE_LCD_SUPPORT_SELFMASK>
```

### 06. Enable Advanced Screen Capture (Screen Recorder)
```
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_CAPTURE_ADVANCED_EDIT_VI>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_CAPTURE_ADVANCED_EDIT_VI>
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_RECORDER>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_RECORDER>
<SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_SCREEN_RECORDER_ITEM>-pip</SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_SCREEN_RECORDER_ITEM>
```

### 07. Enable Partial Blur (Needs OneUI 3.x)
```
<SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_PARTIAL_BLUR>TRUE</SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_PARTIAL_BLUR>
```

### 08. Enable Semi Native Blur (Needs OneUI 3.x)
```
<SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_CAPTURED_BLUR>TRUE</SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_CAPTURED_BLUR>
```

### 09. Enable 3 Resolution options in Settings
> [!NOTE]  
> - this only works on the older revisions of the oneui (to be exact, it works fine on oneui 2.1 or lesser)
```
<SEC_FLOATING_FEATURE_COMMON_CONFIG_DYN_RESOLUTION_CONTROL>WQHD,FHD,HD</SEC_FLOATING_FEATURE_COMMON_CONFIG_DYN_RESOLUTION_CONTROL>
```

### 10. Enable darker Dark Mode (Needs OneUI 2.5)
> [!NOTE]  
> - Remember this code won't works after OneUI2.5+ (After OneUI2.5 it's shifted to Bixby routines)
```
<SEC_FLOATING_FEATURE_LCD_CONFIG_REPLACE_COLOR_FOR_DARKMODE>#FF171717</SEC_FLOATING_FEATURE_LCD_CONFIG_REPLACE_COLOR_FOR_DARKMODE>
```

# Miscellaneous :

### 01. Enable Side Key Function
```
<SEC_FLOATING_FEATURE_SETTINGS_SUPPORT_FUNCTION_KEY_MENU>TRUE</SEC_FLOATING_FEATURE_SETTINGS_SUPPORT_FUNCTION_KEY_MENU>
```

### 02. The Device Model Name, commonly used that to show the ROM'S name.
> [!NOTE]  
> - Search for the following line in floating_feature.xml ```<SEC_FLOATING_FEATURE_SETTINGS_CONFIG_BRAND_NAME>``` and edit the " Galaxy A/M/F x x  " to something like the one below.
```
<SEC_FLOATING_FEATURE_SETTINGS_CONFIG_BRAND_NAME>equinoX - Alpha Centauri</SEC_FLOATING_FEATURE_SETTINGS_CONFIG_BRAND_NAME>
```

### 03. Enable Wireless PowerShare
> [!NOTE]  
> - it won't work without proper hardware support.
```
<SEC_FLOATING_FEATURE_BATTERY_SUPPORT_HV>TRUE</SEC_FLOATING_FEATURE_BATTERY_SUPPORT_HV>
<SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_HV>TRUE</SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_HV>
<SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_NIGHT_MODE>TRUE</SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_NIGHT_MODE>
<SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_TX>TRUE</SEC_FLOATING_FEATURE_BATTERY_SUPPORT_WIRELESS_TX>
<SEC_FLOATING_FEATURE_COMMON_CONFIG_DEX_MODE>dual,wireless,dexforpc</SEC_FLOATING_FEATURE_COMMON_CONFIG_DEX_MODE>
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_WIRELESS>TRUE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_WIRELESS>
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_MULTI_RATIO>TRUE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_MULTI_RATIO>
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_ON_PC>TRUE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_DEX_ON_PC>
```

### 04. Enable Ultra Power Saving
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_ULTRA_POWER_SAVING>TRUE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_ULTRA_POWER_SAVING>
```

### 05. Enable Secure Wifi
```
<SEC_FLOATING_FEATURE_WLAN_SUPPORT_SECURE_WIFI>TRUE</SEC_FLOATING_FEATURE_WLAN_SUPPORT_SECURE_WIFI>
```

### 06. Disable Index Scroll
Search for the following line in floating_feature.xml:
```
<SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_INDEX_SCROLL>
```
And change value from "TRUE" to "FALSE.
```
<SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_INDEX_SCROLL>FALSE</SEC_FLOATING_FEATURE_CONTACTS_SUPPORT_INDEX_SCROLL>
```

### 07. Disable Smart Switch
Search for the following line in floating_feature.xml:
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_SMART_SWITCH>
```
And change value from "TRUE" to "FALSE.
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_SMART_SWITCH>FALSE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_SMART_SWITCH>
```

### 08. Enable Drawer Clearer Contrast/Live Blur
> [!NOTE]  
> - Live Blur requires it's proper libs and bins to make it working.
> - Hop into our chats if you want the proper libs and bins.
```
<SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_3D_SURFACE_TRANSITION_FLAG>TRUE</SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_3D_SURFACE_TRANSITION_FLAG>
```

### 09. Disable Samsung Ads
Search for the following line in floating_feature.xml:
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_SAMSUNG_MARKETING_INFO>
```
And change value from "TRUE" to "FALSE.
```
<SEC_FLOATING_FEATURE_COMMON_SUPPORT_SAMSUNG_MARKETING_INFO>FALSE</SEC_FLOATING_FEATURE_COMMON_SUPPORT_SAMSUNG_MARKETING_INFO>
```

### 10. Enable Haptic Feedback in settings (Needs OneUI 2.5)
```
<SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DC_MOTOR_HAPTIC_FEEDBACK>TRUE</SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DC_MOTOR_HAPTIC_FEEDBACK>
```

### 12. Enable Live Clock in Launcher
```
<SEC_FLOATING_FEATURE_LAUNCHER_SUPPORT_CLOCK_LIVE_ICON>TRUE</SEC_FLOATING_FEATURE_LAUNCHER_SUPPORT_CLOCK_LIVE_ICON>
```

### 13. Change battery capacity
Change values from 0000 to your needs.
```
<SEC_FLOATING_FEATURE_SETTINGS_CONFIG_BATTERY_CAPACITY>0000 mAh</SEC_FLOATING_FEATURE_SETTINGS_CONFIG_BATTERY_CAPACITY>
```

### 14. Disable Game Launcher in Drawer
> [!NOTE]  
> - Change the value from "FALSE" to "TRUE" if you want to enable it.
```
<SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_DEFAULT_GAMELAUNCHER_ENABLE>FALSE</SEC_FLOATING_FEATURE_GRAPHICS_SUPPORT_DEFAULT_GAMELAUNCHER_ENABLE>
```

### 15. Enable Google Discover in Drawer (Needs OneUI version 3 or more)
```
<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ZERO_PAGE_PACKAGE_NAMES>com.google.android.googlequicksearchbox</SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ZERO_PAGE_PACKAGE_NAMES>
```

### 16. Disable Drawer (Needs OneUI version 3 or more)
```
<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ZERO_PAGE_PACKAGE_NAMES>null</SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ZERO_PAGE_PACKAGE_NAMES>
```

### 17. Bring Spotify into the alarm sounds.
```
<SEC_FLOATING_FEATURE_CLOCK_CONFIG_ALARM_SOUND>spotify</SEC_FLOATING_FEATURE_CLOCK_CONFIG_ALARM_SOUND>
```

### 18. Enable Lock screen wallpaper as AOD screen (OneUI 6.0+)
> [!NOTE]  
> - Requires device resource support.
```
<SEC_FLOATING_FEATURE_LCD_CONFIG_AOD_FULLSCREEN>1</SEC_FLOATING_FEATURE_LCD_CONFIG_AOD_FULLSCREEN>
```

### 19. Enable Dolby Atmos without Headsets
> [!NOTE]  
> - For devices with One UI 4.1 or Higher, you will need to download this version of SoundAlive and Place it in your ```/system/priv-app/SoundAlive*/``` (Backup and Delete your original apk first)
> - Link for the file: <a href="https://cloud.ravindu-deshan.workers.dev/0:/SoundAlive_80.apk">Click here</a> & <a href="https://www.dropbox.com/scl/fi/rnhxcgxgk949g26wl1rop/SoundAlive_80.apk?rlkey=ro9se1gecckrh2yotzpge2j22&dl=0">Click here for the mirror</a>
```
<SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DUAL_SPEAKER>TRUE</SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DUAL_SPEAKER>
```
Search for the following line in floating_feature.xml:
```
<SEC_FLOATING_FEATURE_AUDIO_CONFIG_SOUNDALIVE_VERSION>
```
And replace which these lines:
```
eq_knob,eq_custom,uhq_switch,uhq_level,adapt,spk_stereo,dvfs_860000,tube,concert
```

### 20. Enable Music Information in AOD
Search for the following line in floating_feature.xml:
```
<SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>
```
And remove "musicoff" line, then it should look like this:
```
<SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>aodversion=7,clearcoveroff</SEC_FLOATING_FEATURE_FRAMEWORK_CONFIG_AOD_ITEM>
```

### 21. Enable Dolby Atmos in Games
```
<SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DEFAULT_ON_DOLBY_IN_GAME>TRUE</SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DEFAULT_ON_DOLBY_IN_GAME>
```

### 22. Enable Dolby Atmos Game Profiles
```
<SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DOLBY_GAME_PROFILE>TRUE</SEC_FLOATING_FEATURE_AUDIO_SUPPORT_DOLBY_GAME_PROFILE>
```
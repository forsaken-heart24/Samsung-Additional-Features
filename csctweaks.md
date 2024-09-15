# CSC (Country Service Code) Feature Tweaks
- Add some of the lines that you wanna add it in the product/omc/(your region, ex ATT)/config or if you have an dynamic partition styled devices add these lines in the optics/configs/carriers/(your carrier, ex ATT)/conf.
- In Higher One UI versions, you need to decrypt > edit > encrypt the cscfeature.xml. So <a href="https://github.com/forsaken-heart24/OMCDecoder">use this tool to decode your csc file.</a>
## ‼️ Don't add anything unless you don't know what are you doing and what those added code(s) does, cuz it might crash some stuffs on the system.
<hr>

### ¬ Data Icon Style (4G+) 
```
<CscFeature_SystemUI_ConfigOverrideDataIcon>DCM</CscFeature_SystemUI_ConfigOverrideDataIcon>
```

### ¬ Camera Shutter Sound menu
```
<CscFeature_Camera_ShutterSoundMenu>TRUE</CscFeature_Camera_ShutterSoundMenu>
```

### ¬ image quality enhancer
```
<CscFeature_Common_EnhanceImageQuality>TRUE</CscFeature_Common_EnhanceImageQuality>
<CscFeature_Camera_DefaultQuality>superfine</CscFeature_Camera_DefaultQuality>
```

### ¬ bring mobile data toggle on the power menu context
```
<CscFeature_Framework_SupportDataModeSwitchGlobalAction>TRUE</CscFeature_Framework_SupportDataModeSwitchGlobalAction>
```

### ¬ Bring USIM info at the bottom of lock screen
```
<CscFeature_LockScreen_ConfigCarrierTextPolicy>DisplayUsimText;DisplayPlmnOnBottom</CscFeature_LockScreen_ConfigCarrierTextPolicy>
```

### ¬ bring useful cards menu in Samsung Messages
```
<CscFeature_Message_SupportUsefulcard>TRUE</CscFeature_Message_SupportUsefulcard>
```

### ¬ Bring NFC Card Mode
```
<CscFeature_NFC_ConfigDynamicFirmwareLoading>KOO</CscFeature_NFC_ConfigDynamicFirmwareLoading>
<CscFeature_NFC_ConfigReaderModeUI>KOREA</CscFeature_NFC_ConfigReaderModeUI>
```

### ¬ Make NFC icon always appear in the status bar
```
<CscFeature_SystemUI_ConfigDefIndicatorAdditionalSystemIcon>nfc</CscFeature_SystemUI_ConfigDefIndicatorAdditionalSystemIcon>
```

### ¬ Switches the 4G icon (value can be CHC, TGY, VZW, ATT, SPR, each one has different 4G icon)
```
<CscFeature_SystemUI_ConfigOpBrandingForIndicatorIcon>CHC</CscFeature_SystemUI_ConfigOpBrandingForIndicatorIcon>
```
<hr> - Special Thanks To : <a href="https://t.me/Hiruka_NU">Hiruka NU</a> | <a href="https://xdaforums.com/t/csc-feature-mods.4538389/"> This post on XDA </a> | <a href="https://t.me/samuel9611">Samuel</a><br><hr>

### ¬ Force the network icon to show 5 bars (Useless for some regions)
```
<CscFeature_SystemUI_ConfigMaxRssiLevel>5</CscFeature_SystemUI_ConfigMaxRssiLevel>
```

### ¬ Force the system to play song(s) while recording a video
```
<CscFeature_Camera_CamcorderDoNotPauseMusic>TRUE</CscFeature_Camera_CamcorderDoNotPauseMusic>
```

### ¬ Some Camera Tweaks
```
<CscFeature_Camera_CameraFlicker>60hz</CscFeature_Camera_CameraFlicker>
<CscFeature_Camera_DefaultQuality>superfine</CscFeature_Camera_DefaultQuality>
<CscFeature_Camera_ShutterSoundMenu>TRUE</CscFeature_Camera_ShutterSoundMenu>
<CscFeature_Camera_CameraFlicker>60hz</CscFeature_Camera_CameraFlicker>
<CscFeature_Camera_EnableCameraDuringCall>TRUE</CscFeature_Camera_EnableCameraDuringCall>
<CscFeature_Camera_EnableSmsNotiPopup>TRUE</CscFeature_Camera_EnableSmsNotiPopup>
<CscFeature_Camera_DefaultQuality>superfine</CscFeature_Camera_DefaultQuality>
<CscFeature_Camera_SecurityMdmService>TRUE</CscFeature_Camera_SecurityMdmService>
<CscFeature_Camera_CamcorderDoNotPauseMusic>TRUE</CscFeature_Camera_CamcorderDoNotPauseMusic>
<CscFeature_Camera_CamcoderForceShutterSoundDuringSnapShot>FALSE</CscFeature_Camera_CamcoderForceShutterSoundDuringSnapShot>
<CscFeature_Camera_CamcorderEnablePromptPopupToSelectRecMode>TRUE</CscFeature_Camera_CamcorderEnablePromptPopupToSelectRecMode>
<CscFeature_Camcorder_DoNotPauseMusic>TRUE</CscFeature_Camcorder_DoNotPauseMusic>
<CscFeature_Camcorder_DefaultQuality>superfine</CscFeature_Camcorder_DefaultQuality>
```

### ¬ Switches the Data icon style to the LTE icon.
```
<CscFeature_SystemUI_ConfigOverrideDataIcon>LTE</CscFeature_SystemUI_ConfigOverrideDataIcon>
```

### ¬ Data usage in quick panel (requires china smart manager)
```
<CscFeature_SystemUI_SupportDataUsageViewOnQuickPanel>TRUE</CscFeature_SystemUI_SupportDataUsageViewOnQuickPanel>
```

### ¬ Brings back network speed-o-meter on some regions.
```
<CscFeature_Setting_SupportRealTimeNetworkSpeed>TRUE</CscFeature_Setting_SupportRealTimeNetworkSpeed>
```
- For One UI 6 and up, you will need this line too:
```
<CscFeature_Common_SupportZProjectFunctionInGlobal>TRUE</CscFeature_Common_SupportZProjectFunctionInGlobal>
```

### ¬ Force the system to not close the camera during an important phone call
```
<CscFeature_Camera_EnableCameraDuringCall>TRUE</CscFeature_Camera_EnableCameraDuringCall>
```

### ¬ Enable VoLTE with 3G network(H/H+)
```
<CscFeature_Common_EnableHDVoiceDuring3GConnection>TRUE</CscFeature_Common_EnableHDVoiceDuring3GConnection>
```

### ¬ Brings back the mobile data icon in power menu
```
<CscFeature_Framework_SupportDataModeSwitchGlobalAction>TRUE</CscFeature_Framework_SupportDataModeSwitchGlobalAction>
```

### ¬ Enable Call Recording in the Samsung Dialer App
```
<CscFeature_VoiceCall_ConfigRecording>RecordingAllowedByMenu</CscFeature_VoiceCall_ConfigRecording>
```

### ¬ Smart Manager stuffs
```
<CscFeature_SmartManager_DisableAntiMalware>TRUE</CscFeature_SmartManager_DisableAntiMalware>
<CscFeature_SmartManager_ConfigDashboard>dual_dashboard</CscFeature_SmartManager_ConfigDashboard>
<CscFeature_SmartManager_ConfigSubFeatures>applock|appcleanner|autolaunch|autorestart|devicesecurity|storageclean|backgroundapp|chinadualpage|UDS|UDS2|applicationpermission|networkpowersaving|notificationmanager|trafficmanager|roguepopup|data_compression|cstyle</CscFeature_SmartManager_ConfigSubFeatures>
<CscFeature_SmartManager_ConfigUdsSubFeatures>videocompression|uploadcompression</CscFeature_SmartManager_ConfigUdsSubFeatures>
```

### ¬ Some SystemUI cherry picks
```
<CscFeature_SystemUI_ConfigOpBranding5GIcon>5GAvailable,RRCStateCheck,UseDisplayTimer</CscFeature_SystemUI_ConfigOpBranding5GIcon>
<CscFeature_SystemUI_ConfigDefQuickSettingItem>Wifi,SilentMode,SoundMode,WindowsLink,Bluetooth,NightMode,FocusMode,Intent,ColorInversion,Ebook,Routines,InstantSession,RotationLock,PowerShare,Flashlight,QRScanner,AirplaneMode,PowerSaving,MobileData,WifiCalling,Performance,BlueLightFilter,WifiHotspot,Hotspot,PersonalMode,SecureFolder,Location,Nfc,Aod,AllShareCast,ShareLive,DeviceVisibility,Dnd,Sync,UDS,BikeMode,PowerPlanning,EdgeLighting,FloatingMessage,RedPacket,DormantMode,NetworkBooster,QuickConnect,SmartStay,SmartPause,AirView,AirBrowse,Toolbox,CarMode,UltraPowerSaving,SFinder,ScreenCapture,ScreenRecorder,VoLte,Dolby,BatteryMode,DailyBoard,DesktopMode,SpenRemote,KidsHome,GrxScreenOnTime,GrxScreenRecord,GrxMultiAction,GrxRecovery</CscFeature_SystemUI_ConfigDefQuickSettingItem>
<CscFeature_SystemUI_ConfigQuickSettingPopup>SER</CscFeature_SystemUI_ConfigQuickSettingPopup>
<CscFeature_SystemUI_ConfigOverrideDataIcon>LTE</CscFeature_SystemUI_ConfigOverrideDataIcon>
<CscFeature_SystemUI_ConfigOpBrandingForIndicatorIcon>TTT</CscFeature_SystemUI_ConfigOpBrandingForIndicatorIcon>
<CscFeature_SystemUI_ConfigOpBrandingForDataIndicator>TTT</CscFeature_SystemUI_ConfigOpBrandingForDataIndicator>
<CscFeature_SystemUI_SupportRecentAppProtection>TRUE</CscFeature_SystemUI_SupportRecentAppProtection>
<CscFeature_SystemUI_SupportAssistanceAppChooser>TRUE</CscFeature_SystemUI_SupportAssistanceAppChooser>
<CscFeature_SystemUI_SupportDataUsageViewOnQuickPanel>TRUE</CscFeature_SystemUI_SupportDataUsageViewOnQuickPanel>
```

### ¬ Calendar
```
<CscFeature_Calendar_EnableWeatherInfo>TRUE</CscFeature_Calendar_EnableWeatherInfo>
<CscFeature_Calendar_SetColorOfDays>XXXXXBR</CscFeature_Calendar_SetColorOfDays>
<CscFeature_Calendar_EnableMsgReminder>TRUE</CscFeature_Calendar_EnableMsgReminder>
```

### ¬ Enable or Disable WifiCalling (change it from TRUE to FALSE to disable that option)
```
<CscFeature_Setting_SupportWifiCall>TRUE</CscFeature_Setting_SupportWifiCall>
<CscFeature_Setting_SupportWiFiCallingMenu>TRUE</CscFeature_Setting_SupportWiFiCallingMenu>
```

### ¬ Force skip some of the junks in the samsung setup wizard.
```
<CscFeature_Setting_SkipWifiActvDuringSetupWizard>FALSE</CscFeature_Setting_SkipWifiActvDuringSetupWizard>
<CscFeature_Setting_SkipStepsDuringSamsungSetupWizard>TRUE</CscFeature_Setting_SkipStepsDuringSamsungSetupWizard>
```

### ¬ Hide the software update option on the system settings app.
```
<CscFeature_Setting_InfinitySoftwareUpdate>TRUE</CscFeature_Setting_InfinitySoftwareUpdate>
<CscFeature_Setting_DisableMenuSoftwareUpdate>TRUE</CscFeature_Setting_DisableMenuSoftwareUpdate>
<CscFeature_Settings_FOTA>FALSE<CscFeature_Settings_FOTA>
<CscFeature_Settings_GOTA>TRUE</CscFeature_Settings_GOTA>
```

### ¬ Disable Find my device feature, use at your own risk!
```
<CscFeature_Setting_DisableMenuFindMyMobile>TRUE</CscFeature_Setting_DisableMenuFindMyMobile>
<CscFeature_Settings_FindMyMobile>FALSE</CscFeature_Settings_FindMyMobile>
```

### ¬ Clock app tweaks
```
<CscFeature_Clock_ConfigDefStatusWorldclockWeather>OFF</CscFeature_Clock_ConfigDefStatusWorldclockWeather>
<CscFeature_Clock_DisableGoogleLocationInfo>TRUE</CscFeature_Clock_DisableGoogleLocationInfo>
<CscFeature_Clock_EnableAutoPowerOnOffMenu>TRUE</CscFeature_Clock_EnableAutoPowerOnOffMenu>
<CscFeature_Clock_ExclusiveEnablingAutoPowerSetting>TRUE</CscFeature_Clock_ExclusiveEnablingAutoPowerSetting>
<CscFeature_Clock_SupportAlarmOptionMenuForWorkingDay>TRUE</CscFeature_Clock_SupportAlarmOptionMenuForWorkingDay>
```

### ¬ Nuke the KNOXGuard Services.
```
<CscFeature_Knox_SupportKnoxGuard>FALSE</CscFeature_Knox_SupportKnoxGuard>
```

### ¬ AOD
```
<CscFeature_AOD_ConfigAdditionalHomeDoubleKeyAction>;QuickCamera</CscFeature_AOD_ConfigAdditionalHomeDoubleKeyAction>
```

### ¬ Common
```
<CscFeature_Common_AutoConfigurationType>NO_DFLT_CSC, SIMBASED_OMC</CscFeature_Common_AutoConfigurationType>
<CscFeature_Common_ConfigEmergencyModePackages>com.ipsec.service,com.sec.android.providers.iwlansettings,com.sec.android.providers.mapcon</CscFeature_Common_ConfigEmergencyModePackages>
<CscFeature_Common_ConfigYuva>AIBokeh|powerplanning|reserve|zeroforward|mileage|dashboard|downloadable_spowerplanning|sprotect|downloadable_sprotect|downloadable_usbbackup</CscFeature_Common_ConfigYuva>
```

### ¬ Voice Recorder
```
<CscFeature_VoiceRecorder_SupportPrivacyPolicyPrompt>TRUE</CscFeature_VoiceRecorder_SupportPrivacyPolicyPrompt>
```

### ¬ Block Notification Sounds During an Video or an audio playback.
```
<CscFeature_Video_BlockNotiSoundDuringStreaming>TRUE</CscFeature_Video_BlockNotiSoundDuringStreaming>
```

### ¬ Let the Media Player to play a video during an call.
```
<CscFeature_Video_SupportPlayDuringCall>TRUE</CscFeature_Video_SupportPlayDuringCall>
```

### ¬ Enable Popup player on Samsung Video Player (useless cuz you won't use it probably)
```
<CscFeature_Video_EnablePopupPlayer>TRUE</CscFeature_Video_EnablePopupPlayer>
```

### ¬ NFC
```
<CscFeature_NFC_FollowTechnologyRouteToDefRoute>TRUE</CscFeature_NFC_FollowTechnologyRouteToDefRoute>
<CscFeature_NFC_DefStatus>OFF</CscFeature_NFC_DefStatus>
<CscFeature_NFC_StatusBarIconType>DEFAULT</CscFeature_NFC_StatusBarIconType>
```

### ¬ Launcher tweaks.
```
<CscFeature_Launcher_DisableFastScrollIndex>TRUE</CscFeature_Launcher_DisableFastScrollIndex>
<CscFeature_Launcher_AddAutoRotationIcon>TRUE</CscFeature_Launcher_AddAutoRotationIcon>
<CscFeature_Launcher_SupportBadgeClearGesture>TRUE</CscFeature_Launcher_SupportBadgeClearGesture>
<CscFeature_Launcher_ConfigMagazineHome>off</CscFeature_Launcher_ConfigMagazineHome>
<CscFeature_Launcher_PerformanceTunning>TRUE</CscFeature_Launcher_PerformanceTunning>
```

### ¬ Force the system to play an music during an call.
```
<CscFeature_Music_SupportPlaybackDuringCall>TRUE</CscFeature_Music_SupportPlaybackDuringCall>
```

### - Bring back the apk category on the Samsung MyFiles app.
```
<CscFeature_MyFiles_SupportApkCategory>TRUE</CscFeature_MyFiles_SupportApkCategory>
```

### - Disable Setup Wizard
```
<CscFeature_SetupWizard_DisablePrivacyPolicyAgreement>TRUE</CscFeature_SetupWizard_DisablePrivacyPolicyAgreement>
```			
# System Build Property Tweaks
Add these lines in Build.prop, which is located in system folder.

> - We have some good bootanimations here too, like the one from the <a href="https://github.com/forsaken-heart24/FLOSSIS/blob/main/tweak_configs/ROG_bootanimation.tar.gz">ROG devices</a> and one from the <a href="https://github.com/forsaken-heart24/FLOSSIS/blob/main/tweak_configs/Cyberpunk.tar.gz">OnePlus Cyberpunk Edition</a> (you have to extract and copy it over by yourself) and those bootanimation(s) is built for 2340x1080 resolution devices, use it if it works perfectly.

### ⁍ increase or decrease the bootanimation FPS (useful if you have an bootanimation with more frames like the one from above)
```
boot.fps=xx # should be an integer like 60 or smth lower than it.
shutdown.fps=xx # should be an integer like 60 or smth lower than it.
```

### ⁍ Use Dithering pattern for rendering and playbacks, better quality but it lowers the overall raw performance on those use cases.
```
persist.sys.use_dithering=1
```

### ⁍ Enable Hardware video acceleration (Will improve playback performance, but not all the cases)
```
debug.hwui.renderer=skiagl
video.accelerate.hw=1
debug.sf.hw=1
debug.performance.tuning=0
debug.egl.hw=1
debug.composition.type=gpu
```

### ⁍ Enable the newer google assistant.
```
ro.opa.eligible_device=true
```

### ⁍ Disable Knox
```
ro.securestorage.knox=false
```

### ⁍ RMM Fix
```
ro.security.vaultkeeper.native=0
```

### ⁍ Dalvik Virtual Machine Tweaks
```
dalvik.vm.checkjni=false
dalvik.vm.dexopt-data-only=1
dalvik.vm.verify-bytecode=false
dalvik.vm.execution-mode=int:jit
dalvik.vm.dexopt-flags=m=v,o=y
dalvik.vm.stack-trace-file=/data/anr/traces.txt
dalvik.vm.jmiopts=forcecopy
```

### ⁍ Force the UI elements to be rendered in Vulkun instead of OpenGL
```
ro.hwui.use_vulkan=1
```

### ⁍ Dalvik JIT for Dex
```
debug.usejit=true
```

### ⁍ RIL Wakelock Optimization
```
ro.ril.wake_lock_timeout=10000
```

### ⁍ Enable Webcam support for OneUI6.0+
> [!NOTE]  
> - This flag requires kernel support & some plugins.
```
ro.usb.uvc.enabled=true
```

### ⁍ Change the default USB Configuration.
> [!NOTE] 
> - Some of the mentioned flag values can be used to steal your information if you're pc is infected and you authorised your pc in ADB environment, do with pre-caution!

> This flag has many use cases but here's the list of the avaliable flag values :

> mtp : Sets the USB mode to Media Transfer Protocol, which allows the device to enable to copy , move and delete files inside the device's storage device(s)

> ptp : Sets the USB mode to Picture Transfer Protocol, which only allows the user to copy the DCIM and Pictures folder from the device.

> adb : Enables USB debugging mode, which is useful for developers.

> rndis : Enables the device to act as a network adapter, allowing it to be used as a USB Ethernet adapter.

```
persist.sys.usb.config=your_desired_flag_value_here # for example, mtp,adb or just the mtp alone
```

# Advanced System Build Property Tweaks
> [!NOTE] 
> - Disabling these might improve the performance
> - Some might trigger an unusual event which causes the system to behave weird, you're warned and we're not responsible for any damages.

### ⁍ Disables built in error reporting.
```
profiler.force_disable_err_rpt=1
profiler.force_disable_ulog=1
```

### ⁍ Disables logcat
> [!NOTE] 
> - The logcat daemon on Android devices serves a crucial purpose in the Android system's logging and debugging infrastructure.
```
logcat.live=disable
```

### ⁍ Disables Network Dropdump
```
sys.dropdump.on=Off
```

### ⁍ Disables google's atrace logger
> [!NOTE] 
> - The atrace command in Android is a powerful tool used for system-wide tracing and performance analysis. 
```
persist.debug.atrace.boottrace=0
```

### ⁍ Disables samsung's ewlog logger
> [!NOTE] 
> - According to a web source, The ewlogd service is an important component in Samsung's device monitoring and troubleshooting ecosystem. 
> - By collecting and managing emergency logs, it helps Samsung and service providers to quickly identify and address critical issues that users may encounter on their Samsung Android devices.
```
persist.log.ewlogd=0
```

### ⁍ Disables google's lpdumpd logger
> [!NOTE] 
> - According to some web sources, lpdumpd is a crucial service for gathering comprehensive system information and logs, which are essential for debugging, troubleshooting and improving the overall performance and stability of Android devices.
```
sys.lpdumpd=0
```

### ⁍ Disables google's perfetto logger, namely traced and traced_probes.
> [!NOTE] 
> - According to web sources, The purpose of these services is to provide a comprehensive tracing infrastructure for the Android platform. This allows developers, system engineers, and support teams to:
> - Analyze system performance and identify performance bottlenecks, Debug complex issues & Optimize the Android platform
```
persist.device_config.global_settings.sys_traced=0
persist.traced.enable=0
```

### ⁍ Change the Network logger(s) levels from DEBUG to SILENT
> [!NOTE]  
> - Improves performance and device stability, it's generic and it works on all oem devices
> - The below mentioned flags should've existed or not, but if that exists then change it's value from ' D ' , ' I ' or ' V ' (most of the time it's D) to ' S '
```
log.tag.ConnectivityManager=S
log.tag.ConnectivityService=S
log.tag.NetworkLogger=S
log.tag.IptablesRestoreController=S
log.tag.ClatdController=S
```

### Disables unnecessary debugging
> [!NOTE]
> - Stops Low memory killer service from reporting alot.
```
persist.sys.lmk.reportkills=false
```

# System Build property Tweaks
Add these lines in Build.prop, which is located in system folder.

> [!NOTE]  
> - We have some good bootanimations here, like <a href="https://github.com/forsaken-heart24/FLOSSIS/blob/main/ROG_bootanimation.tar.gz">ROG</a> and one from the <a href="https://github.com/forsaken-heart24/FLOSSIS/blob/main/Cyberpunk.tar.gz">oneplus cyberpunk edition</a> (you have to extract and copy it over by yourself) and those bootanimation(s) is built for 2340x1080 resolution devices, use it if it works perfectly.
### ¬ increase or decrease the bootanimation FPS (useful if you have an bootanimation with more frames)
```
boot.fps=xx # should be an integer like 60 or smth lower than it.
shutdown.fps=xx # should be an integer like 60 or smth lower than it.
```

### ¬ Use Dithering pattern for rendering and playbacks, better display quality but it lowers the overall performance.
```
persist.sys.use_dithering=1
```

### ¬ Disables built in error reporting.
```
profiler.force_disable_err_rpt=1
profiler.force_disable_ulog=1
```

### ¬ Disables logcat, improves performance significantly.
```
logcat.live=disable
```

### ¬ Disables Network Dropdump, might have an performance improvement.
```
sys.dropdump.on=Off
```

### ¬ Disables atrace logger, might have an performance improvement.
```
persist.debug.atrace.boottrace=0
```

### ¬ Disables samsung's ewlog logger, might have an performance improvement.
```
persist.log.ewlogd=0
```

### ¬ Video Acceleration Enabled And HW debugging (Will improve playback performance)
```
debug.hwui.renderer=skiagl
video.accelerate.hw=1
debug.sf.hw=1
debug.performance.tuning=1
debug.egl.hw=1
debug.composition.type=gpu
```

### ¬ Enable the newer google assistant.
```
ro.opa.eligible_device=true
```

### ¬ Safetynet Fix
```
ro.knox.enhance.zygote.aslr=1
```

### ¬ Disable Knox
```
ro.securestorage.knox=false
```

### ¬ RMM Fix
```
ro.security.vaultkeeper.native=0
```

### ¬ Dalvik Virtual Machine Tweaks
```
dalvik.vm.checkjni=false
dalvik.vm.dexopt-data-only=1
dalvik.vm.verify-bytecode=false
dalvik.vm.execution-mode=int:jit
dalvik.vm.dexopt-flags=m=v,o=y
dalvik.vm.stack-trace-file=/data/anr/traces.txt
dalvik.vm.jmiopts=forcecopy
```

### ¬ Force the UI elements to be rendered in Vulkun instead of OpenGL
```
ro.hwui.use_vulkan=1
```

### ¬ Dalvik JIT for Dex
```
debug.usejit=true
```

### ¬ RIL Wakelock Optimization
```
ro.ril.wake_lock_timeout=10000
```

### ¬ Enable Webcam support for OneUI6.0+
> [!NOTE]  
> - This flag requires kernel support & some plugins.
```
ro.usb.uvc.enabled=true
```
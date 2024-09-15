# System Build property Tweaks
Add these lines in Build.prop, which is located in system folder.

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
```
ro.usb.uvc.enabled=true
```
> [!NOTE]  
> - this code requires kernel support & plugins.
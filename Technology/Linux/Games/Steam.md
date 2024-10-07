Installing steam should be easy enough, check your distro's package manager for it. Make sure to install the appropriate drivers for your device first, especially your graphics driver.

## Games won't use NVIDIA in dual-graphics system
There is a chance that a game won't use your dedicated NVIDIA graphics card. There are 2 recommended ways to fix this:

- If you have the `prime-run` script:
```
prime-run %command%
```

- If you don't have the `prime-run` script:
```
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia %command%
```

- If you are using the `nouveau` driver:
```
DRI_PRIME=1 %command%
```

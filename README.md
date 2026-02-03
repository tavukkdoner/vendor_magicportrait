# vendor_magicportrait

## MagicPortrait for vanilla roms 

Download https://sourceforge.net/projects/nikgapps/files/Releases/Android-16/02-Feb-2026/Addons/NikGapps-Addon-16-PixelSpecifics-20260202-signed.zip/download

Flash in recovery mode

Reason: MagicPortrait works with Pixel Launcher so you need to flash Pixel Launcher if you have it in your gapps skip this step. Also it won't work with default launcher.

## How to add

Add in your local manifest:

```
<remote  name="tavukkdoner"
           fetch="https://github.com/tavukkdoner"
           revision="lineage-22.2" />

<project path="vendor/mp" name="vendor_magicportrait" remote="tavukkdoner" revision="main" />
```

Add in your device.mk

```
# MagicPortrait
ifeq ($(TARGET_USES_MAGICPORTRAIT), true)
$(call inherit-product-if-exists, vendor/mp/gms_magic_portrait.mk)
endif
```

and set true TARGET_USES_MAGICPORTRAIT whenever you want to use!

Credits: https://git.evolution-x.org/EvoX/vendor_gms

If there is an authoring error or a licensing issue, please open issue.
# kconfig
kconfig fragments for SOF development

The base-defconfig is intended to provide basic support for all platforms currently used for SOF development, including:
- boot
- i915/display
- USB (w/ Ethernet dongles)
- Ethernet
- WiFi

sof-defconfig lists all the options for SOF.

Those fragments are supposed to be applied on top of a default kernel
configuration.

```bash
cd <your kernel>
make defconfig
scripts/kconfig/merge_config.sh .config <PATH>/kconfig/base-defconfig <PATH>/kconfig/sof-defconfig
make -j8
```

Enjoy!
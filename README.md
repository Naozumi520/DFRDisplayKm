# Touch Bar (DFR) Display Driver for Windows

This driver implements custom display functionality for Apple Touch Bar (DFR)
on Windows 10. Touch feedback has not yet been discovered but should be quite
easy since it is a HID device.

## Motivation

Keep myself busy during the last few weeks of my internship (thank you LinkedIn & Microsoft)

## Installation

No official signed binary will be built at this moment. To build the driver, a
few software needs to be installed including Visual Studio 2019 (with C/C++ 
workload) and Windows 10 Driver Kit, Version 1903. Install `DFRUsbCcgp.inf`
for the "Apple Touch Bar" device first, then install `DFRDisplayKm.inf` for the
"iBridge Display" device.

**You need to turn off Secure Boot as described in the [Apple Knowledge Base](https://support.apple.com/en-us/HT208330)**.

## Known Caveats

* Only Apple T2-based MacBook Pro(s) are supported. I assume T1 support is similar but I don't have device to test.
* The driver might fails to load on T2 cold boot. Reboot the computer once and it should work.

## License

Copyright (c) Bingxing Wang. All rights reserved.

Licensed under the [MIT License](./LICENSE).
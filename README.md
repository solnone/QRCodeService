# QRCodeService
Show a MRTK2 service to read (and position) QR codes using HoloLens 2

PLEASE PLEASE PLEASE before opening issues: 
- [read this article first](https://localjoost.github.io/Reading-QR-codes-with-an-MRTK2-Extension-Service/'/), 
- [then read this article](https://localjoost.github.io/Positioning-QR-codes-in-space-with-HoloLens-2-building-a-'poor-man's-Vuforia'/), especially the build instructions at the end of the article
- And for this specific branch, [read this as well](https://localjoost.github.io/Upgrading-reading-and-positioning-QR-codes-with-HoloLens-2-to-Unity-2020-+-OpenXR-plugin/)


## Changes

- Unity Editor 2020.3.<span style="color:red">7f1</span> → 2020.3.<span style="color:green">19f1</span>
- Microsoft.MixedReality.OpenXR <span style="color:red">0.9.3</span> → <span style="color:green">1.3.1</span>
- MRTK <span style="color:red">2.6.1</span> → <span style="color:green">2.7.3</span>
    - Foundations, Assets, Extensions, Toolkit, Examples

<br>

- Added needed call to `QRCodeWatcher.RequestAccessAsync()` before creating `QRCodeWatcher`

- Removed use of `TimeSpan.UTCNow` and `QRCode.LastDetectedTime` to determine freshness of localizations
    - Did not work while remoting in editor


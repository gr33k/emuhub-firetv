# Getting Started

EmuHub Fire TV is the Fire TV / Android TV client for EmuHub, not a standalone
emulator. Its native shell opens your EmuHub server in a TV-oriented WebView and
adds platform navigation, account switching, and client controls. Game execution
depends on the configured EmuHub runtime and the device's capabilities.

This repository currently publishes documentation rather than an APK or a
complete independently buildable source export. A public release must identify
its signing identity, minimum API, supported models, exact version, and checksum.
Do not treat a development APK as an Amazon Appstore release.

## Connection and profiles

Enter your own server address, for example `https://emuhub.example`. Use HTTPS
for public servers. The inspected client allows HTTP only for local/private
targets. Server changes and sign-out must remain explicit user actions.

Legacy and enhanced Fire TV profiles have different rendering limits. A
WebGL2-capable newer device does not establish the same support on an older TV
stick. Preserve the selected device profile rather than applying one global
shader/resolution policy to every EmuHub client.

## First session

1. Open EmuHub, select your server, and verify login and the TV keyboard.
2. Test remote focus, wheel selection, and first-login media without a reload.
3. Pair a gamepad and test the shortcuts before launching a game.
4. Verify guest controls, safe exit, account boundaries, and a second launch.

See [Controller Mapping](Controller-Mapping.md). A connected controller may use
different button names depending on its Android input mode and firmware.

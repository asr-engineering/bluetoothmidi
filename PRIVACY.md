# Privacy Policy — BluetoothMIDI

**Effective date:** July 3, 2026

BluetoothMIDI ("the app") is a Windows desktop application that bridges Bluetooth LE MIDI devices to virtual MIDI ports so they can be used in DAWs and other music software.

This policy describes what information the app accesses, how it is used, and what (if anything) leaves your device.

## Summary

The app does **not** collect, store, or transmit any personal information. It contains no telemetry, no analytics, no advertising, no user accounts, and no third-party tracking SDKs. All data the app handles stays on your computer, with one exception: an optional, one-time download of a Microsoft runtime installer (described below).

## Information the app accesses

### Bluetooth device information
To discover and connect to MIDI devices, the app uses Windows Bluetooth APIs to scan for nearby Bluetooth LE devices. During scanning it reads:

- Device names and Bluetooth addresses broadcast by nearby devices
- Advertised GATT service identifiers (to determine whether a device supports BLE MIDI)
- Battery level, where a device exposes it

This information is used solely to display available MIDI devices in the app and to establish connections you request. It is processed in memory and is not transmitted anywhere.

### MIDI data
MIDI messages (notes, control changes, etc.) from your connected devices are forwarded in real time to virtual MIDI ports on your computer. MIDI data is not recorded or transmitted by the app. If you enable the optional MIDI monitor / debug logging, MIDI messages may be written to a local log file on your computer (see below); this is off by default and under your control.

### Settings and log files
The app stores the following files locally under `%LOCALAPPDATA%\BluetoothMIDI\` on your computer:

- **`settings.json`** — your app preferences, including the identifiers of Bluetooth devices you have chosen to enable or auto-connect
- **`startup.log`, `sdk_install.log`, `debug.log`** — diagnostic logs used to troubleshoot problems on your machine

These files never leave your computer. You can delete them at any time; deleting them resets the app's settings. Uninstalling the app does not automatically remove this folder — you may delete it manually if you wish.

## Network access

The app makes **no network connections** during normal operation.

The single exception: if the required **Windows MIDI Services runtime** (a Microsoft component) is not installed on your computer, the app offers to download its installer from Microsoft's official GitHub releases page (`github.com/microsoft/MIDI`). This is a standard file download — the app sends no personal data with the request. As with any internet download, the server (GitHub) receives your IP address; GitHub's handling of that data is described in [GitHub's Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-privacy-statement).

## Data sharing

The app shares no data with anyone. There are no third parties receiving data from the app, because the app transmits no data.

## Children's privacy

The app does not collect personal information from anyone, including children.

## Your choices and control

- Bluetooth access can be revoked at any time through Windows Settings → Privacy & security → Bluetooth.
- Debug/MIDI logging is optional and can be turned off in the app.
- All locally stored files can be deleted by removing the `%LOCALAPPDATA%\BluetoothMIDI\` folder.

## Changes to this policy

If the app's data practices ever change (for example, if a future version adds an online feature), this policy will be updated and the effective date revised before that version is released.

## Contact

If you have questions about this policy, contact:

**ASR Services** — asr.services@hotmail.com

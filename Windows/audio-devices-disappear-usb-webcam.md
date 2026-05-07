# Windows Audio Devices Disappear After Connecting USB Webcam

## Overview

This guide documents a real-world troubleshooting case where Windows audio input and output devices disappeared after a USB device conflict. Device Manager still detected audio hardware, but Windows Sound settings showed no available output or input devices.

The issue originally appeared to be related to a Dell AC511 USB soundbar, but further testing showed that a Razer Kiyo webcam was triggering the Windows Audio service to crash.

## Environment

- Windows laptop
- Dell docking station
- Dual Dell monitors
- Dell AC511 USB soundbar
- Blue Snowball USB microphone
- Razer Kiyo webcam
- External USB disk/CD reader

## Symptoms

- Windows Sound settings showed no available output devices
- Windows Sound settings showed no available input devices
- Device Manager still detected audio-related hardware
- Windows Audio service was not running
- Restarting Windows Audio temporarily restored devices
- Audio devices disappeared again shortly after
- Event Viewer showed repeated Windows Audio service crashes

## Initial Assumption

The issue first appeared to involve the Dell AC511 USB soundbar because it was the audio device that stopped working. The soundbar was connected through a Dell monitor USB hub, which was connected through a docking station to a laptop.

Because of that setup, the first assumption was that the issue might be caused by the docking station, monitor USB hub, or soundbar connection.

## Troubleshooting Steps

### 1. Checked Windows Sound Settings

Windows Sound settings showed no available input or output devices.

This suggested that Windows was not exposing any usable audio endpoints, even though hardware was still visible elsewhere in the system.

### 2. Checked Device Manager

Device Manager still showed several audio-related devices, including the Dell soundbar.

This helped confirm that Windows could still detect hardware, but the audio service was not presenting the devices correctly in Sound settings.

### 3. Checked Windows Audio Services

The following services were checked:

- Windows Audio
- Windows Audio Endpoint Builder

Windows Audio was not running. When it was started, audio devices briefly appeared, then disappeared again.

This indicated that the Windows Audio service was likely crashing shortly after starting.

### 4. Checked Event Viewer

Event Viewer showed repeated Windows Audio service failures.

The System log showed that the Windows Audio service had terminated unexpectedly multiple times.

The Application log showed an error involving:

```text
Faulting application: svchost.exe_Audiosrv
Faulting module: audiosrv.dll
Exception code: 0xc0000005
```

This confirmed that the Windows Audio service was crashing rather than simply failing to detect a device.

### 5. Removed External USB Devices

All external USB/audio devices were unplugged, including:

- Dell AC511 USB soundbar
- Blue Snowball USB microphone
- Razer Kiyo webcam
- External USB disk/CD reader

After the devices were unplugged, the normal audio outputs returned.

This showed that one of the external USB devices was likely triggering the Windows Audio crash.

### 6. Reconnected Devices One at a Time

Each device was plugged back in individually and tested.

| Device | Result |
|---|---|
| Dell monitor USB hub | No issue |
| Dell AC511 USB soundbar | No issue |
| Blue Snowball USB microphone | No issue |
| External USB disk/CD reader | No issue |
| Razer Kiyo webcam | Audio devices disappeared |

This isolated the Razer Kiyo as the device that triggered the issue.

### 7. Tested Kiyo Microphone Disable

The Razer Kiyo microphone was disabled in Device Manager, but the issue still occurred.

This suggested that the problem was not limited to the microphone endpoint. The issue may have involved the webcam’s USB device stack, driver behavior, or how the device interacted with Windows audio services.

## Root Cause

The Razer Kiyo webcam appeared to trigger the Windows Audio service crash.

When the Kiyo was connected, Windows audio input and output devices disappeared. Other USB devices worked normally when tested individually.

## Resolution

The Razer Kiyo was removed from the setup.

After removing the Kiyo, Windows audio devices remained stable, and the Dell soundbar, Blue Snowball microphone, monitor USB hub, and external disk reader worked normally.

## General Troubleshooting Guide

If Windows audio devices disappear but Device Manager still detects audio hardware, try the following process:

1. Open Windows Sound settings and confirm whether output/input devices are missing.
2. Open Device Manager and confirm whether audio hardware is still detected.
3. Open Services and check whether Windows Audio is running.
4. Restart Windows Audio and Windows Audio Endpoint Builder.
5. Check Event Viewer for Windows Audio service crashes.
6. Unplug external USB audio/video devices.
7. Reconnect devices one at a time.
8. Identify which device causes audio endpoints to disappear.
9. Remove, update, replace, or avoid using the problem device.

## Useful Windows Tools

- Windows Sound settings
- Device Manager
- Services
- Event Viewer
- Windows Audio service
- Windows Audio Endpoint Builder service

## Skills Demonstrated

- Windows audio troubleshooting
- Device Manager analysis
- Event Viewer log review
- Windows service troubleshooting
- USB device isolation
- Root cause analysis
- Technical documentation

## Final Notes

This issue looked like a Dell soundbar problem at first, but systematic testing showed that the soundbar was not the cause. Testing one USB device at a time made it possible to isolate the Razer Kiyo as the trigger.

# Shizuku + Accessibility Commands Reference

## Shizuku Execution Modes

### Intent Mode (Fast)
```bash
am start -a android.intent.action.VIEW -d '<deeplink_url>'
```

### UI Operation Mode
```bash
input tap <x> <y>          # Tap at coordinates
input swipe <x1> <y1> <x2> <y2> <duration>  # Swipe
input text <text>          # Input text
input keyevent <keycode>   # Key event
```

## System Control

| Action | Command |
|--------|---------|
| WiFi on | `svc wifi enable` |
| WiFi off | `svc wifi disable` |
| Bluetooth on | `svc bluetooth enable` |
| Bluetooth off | `svc bluetooth disable` |
| Screenshot | `screencap -p /sdcard/screenshot.png` |
| Brightness | `settings put system screen_brightness <0-255>` |
| Volume | `media volume --set <0-15>` |

## App Management

| Action | Command |
|--------|---------|
| Install | `pm install <path>` |
| Uninstall | `pm uninstall <package>` |
| Clear data | `pm clear <package>` |
| Open app | `monkey -p <package> 1` |

## Key Events

| Key | Code |
|-----|------|
| Home | 3 |
| Back | 4 |
| Recent Apps | 187 |
| Volume Up | 24 |
| Volume Down | 25 |
| Power | 26 |
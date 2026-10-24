# Can the display dim or turn off at night?

Yes. Night mode automatically dims or turns off the display during the hours you choose. You can configure it from the web UI (visit your Transit Tracker's IP address in a web browser, [how?](./find-ip-address)) or from [Home Assistant](../02-home-assistant.md) using these settings:

- **Night Mode**: choose `Disabled`, `Dim Display` or `Turn Off Display`.
- **Night Start** and **Night End**: the hours night mode is active, such as 22:00 to 07:00. The hours can span midnight.
- **Night Brightness**: how bright the display is during night hours when using `Dim Display`, from 0 to 255 like the normal brightness setting. The display is never made brighter than your normal brightness setting.

Your normal brightness setting is left untouched and comes back automatically when the night hours end.

## Waking the display

Pressing either brightness button while night mode is active wakes the display. It stays at your normal brightness until the night hours end, and night mode starts again the next night. The **Night Mode Active** sensor shows whether night mode is currently dimming the display.

## Time zone

Night hours use the Transit Tracker's local time. If it's connected to Home Assistant 2026.3 or newer, it uses Home Assistant's time zone automatically. Otherwise it uses the time zone set in the firmware, which is `America/Los_Angeles` by default. You can change it by [customizing the firmware](../../03-advanced/firmware-customization.md#change-the-time-zone).

# hass-display

ESPHome config for a Waveshare ESP32-S3-Touch-LCD-2.1B (480x480 round display) that shows
Octopus Energy data from Home Assistant:

- Current and next unit rate (p/kWh), coloured by price
- Live usage (W/kW) as a progress ring that fills to a configurable maximum
- Today's usage (kWh) and cost so far
- Backlight timeout, woken by touch or a Home Assistant motion sensor

## Requirements

- ESPHome 2026.10 or newer
- Home Assistant with the Octopus Energy integration
  (live usage and today's totals need an Octopus Home Mini)

## Setup

1. Copy `secrets.yaml.example` to `secrets.yaml` and fill in your values.
2. Edit the entity ID of your motion sensor near the bottom of `hass-display.yaml`.
3. Adjust the substitutions at the top (timeout, ring maximum, colour thresholds).
4. Compile and install with ESPHome, then add the device in Home Assistant
   (Settings > Devices & services > ESPHome).

`secrets.yaml` is git-ignored. Do not commit it.

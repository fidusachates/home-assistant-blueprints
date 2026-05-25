# Samotech Home Assistant Blueprints

Official Home Assistant blueprints for the Samotech SM-series Zigbee smart switch and dimmer range.

Each blueprint is engineered against actual Samotech hardware behaviour over ZHA (Zigbee Home Automation) and tested end-to-end in a live Home Assistant setup before publication.

## Current blueprints

### SM-Series Linked Sync Group
**File:** `samotech-sm-series-linked-sync.yaml`

Sync two to five Samotech SM-series Zigbee devices so they behave as a single coordinated lighting control. The UK-retrofit alternative to running new traveler wire for hardware 2-way switching. Works across any mix of dimmers (SM323, SM325-ZG, SM309-S) and switch modules (SM308-S) in the same group.

State changes mirror across all devices in the group; brightness changes mirror across dimmer-capable devices. Loop prevention via Home Assistant context tracking ensures the sync only fires from user interaction, never from itself.

**Read the full guide:** https://www.samotech.co.uk/samotech-linked-dimmers-home-assistant-blueprint/

**Import URL:**
```
https://raw.githubusercontent.com/fidusachates/home-assistant-blueprints/main/samotech-sm-series-linked-sync.yaml
```

### Pull Cord Bathroom Auto-Off
**File:** `samotech-pull-cord-bathroom-auto-off.yaml`

Automatic timeout for the Samotech Zigbee Pull Cord Dimmer — the world's only smart pull cord dimmer in production. Configurable auto-off period, optional dim warning before timeout, manual override always respected. Designed for UK BS 7671:2018 Zone 2 bathroom installations.

**Read the full guide:** https://www.samotech.co.uk/samotech-pull-cord-bathroom-auto-off-home-assistant-blueprint/

**Import URL:**
```
https://raw.githubusercontent.com/fidusachates/home-assistant-blueprints/main/samotech-pull-cord-bathroom-auto-off.yaml
```

## Importing into Home Assistant

In Home Assistant: **Settings → Automations & Scenes → Blueprints → Import Blueprint** and paste one of the raw URLs above.

## Compatibility

All blueprints assume devices are integrated via the **ZHA (Zigbee Home Automation)** integration. Zigbee2MQTT variants may follow if there is community demand.

## About Samotech

Samotech Ltd is a UK-based smart home product company. We design and manufacture Zigbee 3.0, Matter over Thread, Matter over Wi-Fi and direct Wi-Fi devices specifically engineered for British domestic wiring (BS 7671:2018 aligned).

The full product range is at https://www.samotech.co.uk/

## Issues and contributions

Open an issue if a blueprint doesn't work as documented or if you'd like a new blueprint added for a specific Samotech device or use case.

# Samotech Home Assistant Blueprints

Official Home Assistant blueprints for the Samotech SM-series Zigbee smart switch and dimmer range.

Each blueprint is engineered against actual Samotech hardware behaviour and tested end-to-end in a live Home Assistant setup before publication. Compatible with both **ZHA (Zigbee Home Automation)** and **Zigbee2MQTT** – the blueprints use standard Home Assistant state triggers and core light services that behave identically across both integrations.

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

### Direct Mirror Pair
**File:** `samotech-sm-series-direct-mirror-pair.yaml`

The 2-device specialisation. Pair exactly two Samotech SM323 dimmers so they behave as physically hardwired in parallel at the load. On/off state and brightness mirror in both directions within ~200 ms. Both dimmers retain independent power monitoring on independent circuits.

Optimised for the most common UK retrofit case: two dimmers acting as a virtual 2-way circuit, with cleaner UX and faster response than the multi-device sync group. Use this when you have exactly two dimmers; use the Linked Sync Group when you have three or more or a mix of dimmer and switch hardware.

**Read the full guide:** https://www.samotech.co.uk/samotech-direct-mirror-pair-home-assistant-blueprint/

**Import URL:**
```
https://raw.githubusercontent.com/fidusachates/home-assistant-blueprints/main/samotech-sm-series-direct-mirror-pair.yaml
```

### Pull Cord Bathroom Auto-Off
**File:** `samotech-pull-cord-bathroom-auto-off.yaml`

Automatic timeout for the Samotech Zigbee Pull Cord Dimmer – the world's only smart pull cord dimmer in production. Configurable 5–240 minute auto-off period, optional dim warning before timeout, manual override always respected. Designed for UK BS 7671:2018 Zone 2 bathroom installations.

**Read the full guide:** https://www.samotech.co.uk/samotech-pull-cord-bathroom-auto-off-home-assistant-blueprint/

**Import URL:**
```
https://raw.githubusercontent.com/fidusachates/home-assistant-blueprints/main/samotech-pull-cord-bathroom-auto-off.yaml
```

## Importing into Home Assistant

In Home Assistant: **Settings → Automations & Scenes → Blueprints → Import Blueprint** and paste one of the raw URLs above.

## Compatibility

All blueprints work with both **ZHA (Zigbee Home Automation)** and **Zigbee2MQTT**. The blueprints are integration-agnostic – they use standard Home Assistant state triggers and core light services that behave identically across both integrations. You can even mix ZHA and Zigbee2MQTT devices in the same blueprint instance if you have a hybrid setup.

## About Samotech

Samotech Ltd is a UK-based smart home product company. We design and manufacture Zigbee 3.0, Matter over Thread, Matter over Wi-Fi and direct Wi-Fi devices specifically engineered for British domestic wiring (BS 7671:2018 aligned). Companies House 11266444, VAT GB312010478. Trading since 2018.

The full product range is at https://www.samotech.co.uk/

## Issues and contributions

Open an issue if a blueprint doesn't work as documented or if you'd like a new blueprint added for a specific Samotech device or use case.

## Licence

MIT-licensed. Use, modify and redistribute freely.

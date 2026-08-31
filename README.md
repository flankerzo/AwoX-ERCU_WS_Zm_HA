# AwoX ERCU_WS_Zm - Home Assistant ZHA Blueprint

A Home Assistant automation blueprint for the **AwoX ERCU_WS_Zm** Zigbee remote control using **Zigbee Home Automation (ZHA)**.

## About

The AwoX ERCU_WS_Zm remote does not provide useful standard Home Assistant entities for its buttons. Instead, the remote sends Zigbee commands which are exposed by ZHA as `zha_event` events.

This blueprint converts those events into customizable Home Assistant actions.

## Supported device

- Manufacturer: `AwoX`
- Model: `ERCU_WS_Zm`
- Integration: `Zigbee Home Automation (ZHA)`

## Currently supported buttons

| Button | Zigbee cluster | Command | Action |
|---|---:|---|---|
| ON/OFF | `0x0006` | `toggle` | Custom action |
| Brightness + | `0x0008` | `step_with_on_off` | Custom action |
| Brightness - | `0x0008` | `step` | Custom action |

## Installation

### Import the blueprint

In Home Assistant:

1. Go to **Settings → Automations & Scenes → Blueprints**.
2. Import the blueprint from this repository.
https://raw.githubusercontent.com/flankerzo/AwoX-ERCU_WS_Zm_HA/main/ZHA%20-%20AwoX%20ERCU_WS_Zm%20Custom%20Actions.yaml

Alternatively, copy the YAML file manually to:

```text
/config/blueprints/automation/awox/ercu_ws_zm.yaml

---
title: Landroid Lawn Mower Card
hide:
  - toc
---

<!-- markdownlint-disable MD046 -->

# Custom-card "Landroid Lawn Mower Card"

This is a `custom-card` to control your Worx Landroid and display the state of the mower. The second section of the card shows the battery level and the status of the rain sensor. You can also toggle the party mode there.

![card-lightmode](../../docs/assets/img/custom_card_landroid/card_light.png)
![card-darkmode](../../docs/assets/img/custom_card_landroid/card_dark.png)

## Credits

Author: hartmann-jonas - 2024
Version: 1.0.0

## Changelog

<details>
<summary>1.0.0</summary>
Initial release
</details>

## Requirements

This card needs the [landroid_cloud](https://github.com/MTrab/landroid_cloud) integration and the [bar-card](https://github.com/custom-cards/bar-card) to function, you can install both via HACS.

## Usage

```yaml
type: custom:button-card
template: custom_card_landroid
entity: lawn_mower.landroid_m500
  variables:
    ulm_custom_card_landroid_battery: sensor.landroid_m500_battery
    ulm_custom_card_landroid_rain: binary_sensor.landroid_m500_rainsensor_triggered
    ulm_custom_card_landroid_party: switch.landroid_m500_party_mode
```

## Variables

<table>
<thead>
<tr>
<th>Variable</th>
<th>Example</th>
<th>Required</th>
<th>Explanation</th>
</tr>
</thead>
<tbody>
<tr>
<td>ulm_custom_card_landroid_battery</td>
<td>sensor.landroid_m500_battery</td>
<td>Yes</td>
<td>The sensor that holds the battery level of the mower</td>
</tr>
<tr>
<td>ulm_custom_card_landroid_rain</td>
<td>sensor.landroid_m500_rainsensor_triggered</td>
<td>Yes</td>
<td>The binary sensor that goes to 'on' when the mower detects rain</td>
</tr>
<tr>
<td>ulm_custom_card_landroid_party</td>
<td>switch.landroid_m500_party_mode</td>
<td>Yes</td>
<td>The switch that toggles the "Party mode"</td>
</tr>
</tbody>
</table>

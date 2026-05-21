# Bill of Materials 📋

Full components list for the LoRa Meshtastic device.
All components used in this build were sourced from The Pi Hut 
and standard UK suppliers.

## Core Electronics

| Component | Description | Supplier | Approx Cost |
|---|---|---|---|
| XIAO ESP32S3 + Wio SX1262 Kit | Main LoRa module, pre-flashed with Meshtastic | [The Pi Hut](https://thepihut.com/products/xiao-esp32s3-wio-sx1262-kit-for-meshtastic-lora) | £10.50 |
| 2-Way 18650 Battery Management Board | Handles charging, protection, and USB output | [The Pi Hut](https://thepihut.com/products/2-way-18650-battery-holder) | £8–£15 |
| 18650 Li-Ion Cells x2 | 2500–3500mAh recommended — not included | Any reputable supplier | £5–£15 |

## Antenna Components

| Component | Description | Supplier | Approx Cost |
|---|---|---|---|
| SMA Female Bulkhead Connector | Mounts in top of enclosure | Amazon / AliExpress | £1–£3 |
| U.FL to SMA Pigtail Cable | Connects LoRa module to SMA connector | Amazon / AliExpress | £1–£3 |
| 868MHz SMA Whip Antenna | External antenna, screws onto SMA connector | Amazon / AliExpress | £2–£5 |
| WiFi / BLE Antenna | Small stick-on antenna for XIAO module | Included with XIAO kit | £0 |

## Enclosure Hardware

| Component | Description | Supplier | Approx Cost |
|---|---|---|---|
| M4 Button Head Screws x8 | Holds enclosure halves together | Local hardware store | £1 |
| Neodymium Magnets x4 (approx 10mm dia) | Retains magnetic battery panel | Amazon / AliExpress | £2–£4 |
| Superglue | For securing magnets into pockets | Local hardware store | £1 |

## Wiring

| Component | Description | Approx Cost |
|---|---|---|
| Red wire — approx 8cm | 5V positive connection | £0 (off a reel) |
| Black wire — approx 8cm | GND connection | £0 (off a reel) |
| Header pins x2 | Clean plug-in connection to XIAO | £1 |

## 3D Printing

| Component | Description | Approx Cost |
|---|---|---|
| Black PLA Filament | Matte finish recommended | £1–£2 per print |

## Total Estimated Cost

| Scenario | Cost |
|---|---|
| Self-build (sourcing cheaply) | £24 – £35 |
| Self-build (standard pricing) | £35 – £50 |

---

## Notes

- 18650 cells are not included and must be sourced separately — 
  use reputable brands only, avoid unbranded cells from unknown suppliers
- The XIAO ESP32S3 + Wio SX1262 kit comes pre-flashed with Meshtastic 
  firmware so no additional flashing is required out of the box
- All electronic components sourced from The Pi Hut carry their own 
  compliance certifications — they are CE and UKCA marked 
  where applicable
- STL files for the 3D printed enclosure are in the `/CAD` folder 
  of this repository

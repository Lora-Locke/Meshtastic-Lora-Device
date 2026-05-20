# 📡 LoRa Meshtastic Device — lora-locke

> *"What if you could send messages across kilometres of countryside, through forests, over hills, with no phone signal, no internet, and no monthly bill?"*  
> That's exactly what this project does. Welcome to the mesh. 🌐

---

## What Is This?

This is an open source, 3D printed handheld LoRa Meshtastic communication node. It was designed and built as part of an **HNC Engineering Design (Unit 4001)** project, but it turned into something genuinely useful — a pocket sized off grid communication device that actually works.

The device is built around the **Seeed XIAO ESP32S3 + Wio SX1262 kit**, powered by dual hot swappable 18650 batteries, and housed in a custom designed 3D printed PLA enclosure with an external SMA antenna. It talks to your phone over Bluetooth via the free **Meshtastic app**, and it can communicate with other Meshtastic nodes up to several kilometres away with no infrastructure whatsoever.

No towers. No SIM card. No subscription. Just radio waves and clever firmware.

---

## Why Does This Exist?

Good question. The short answer: because conventional communication infrastructure is fragile.

Mobile networks go down in emergencies. Rural areas have black spots the size of small countries. Events with thousands of people bring networks to their knees. And if you've ever tried to coordinate a hiking group in the middle of nowhere, you'll know that shouting really doesn't scale well beyond about 50 metres.

Meshtastic LoRa devices are a genuinely viable solution for:

- 🏔️ **Outdoor adventures** — hiking, mountain biking, wild camping
- 🚨 **Emergency preparedness** — backup comms when infrastructure fails
- 🎪 **Events and festivals** — coordinate teams without relying on congested networks
- 🌍 **Remote IoT deployments** — sensor networks in areas without connectivity
- 🔬 **Experimentation** — because building your own radio network is just really cool

This isn't a niche hobbyist toy. As infrastructure resilience becomes more important, decentralised mesh communication networks like Meshtastic represent a genuinely compelling backup safety communication solution. A handful of these devices distributed across a team or community creates a self healing, self extending communication network that requires nothing external to operate.

---

## How Does Meshtastic Work?

Meshtastic uses **LoRa (Long Range)** radio to create a mesh network. Each device acts as both a client and a router — when you send a message, nearby nodes receive it and automatically forward it along until it reaches its destination. The more nodes on the network, the further messages can travel.

Think of it like a game of Chinese whispers, except it actually works and the message arrives intact.

![Meshtastic Mesh Network Diagram](images/mesh_diagram.png)

Each node operates on licence exempt frequencies (863–870 MHz in the UK, governed by Ofcom IR 2030 and ETSI EN 300 220), meaning anyone can use one legally without a radio licence.

For the full technical deep dive, the Meshtastic documentation is excellent:  
👉 [meshtastic.org/docs/introduction](https://meshtastic.org/docs/introduction/)

---

## The Design Journey

This project went through three design iterations before landing on the final build. The full engineering process — including SolidWorks CAD models, force studies, design considerations, and a Pugh matrix evaluation — is documented in the accompanying college assignment.

Here's the short version:

### Design 1 — The Brick 🧱
The first attempt. Functional, but at 105mm x 45mm x 50mm it was more portable safe than portable device. Everything stacked vertically which meant the height was excessive. Great as a fixed infrastructure node, terrible in a pocket. Back to SolidWorks.

![Design 1 CAD](images/design1_cad.png)
![Design 1 Sketch](images/design1_sketch.png)

### Design 2 — Getting There 📐
Rotated the internal layout so the battery board and LoRa module sit side by side instead of on top of each other. Result: 130mm x 50mm x 35mm — noticeably slimmer and much more natural to hold. A SolidWorks force study was also run on this design to simulate drop loading and identify stress concentration points at the enclosure corners.

![Design 2 CAD](images/design2_cad.png)
![Design 2 CAD](images/design22_cad.png)
![Design 2 Force Study](images/design2_force_study.png)
![Design 2 Force Study](images/design22_force_study.png)
![Design 2 Sketch](images/design2_sketch.png)
![Design 2 Sketch2](images/design22_sketch.png)

### Design 3 — The One That Actually Works ✅
Same dimensions as Design 2 but with two key improvements:

1. **External SMA antenna** — detachable, so the device stays pocketable when you don't need maximum range, and gains a proper antenna when you do
2. **Magnetic hot swap battery panel** — four neodymium magnets hold the battery cover in place, meaning you can swap cells in the field in seconds without a screwdriver. One battery at a time, so you never even have to power the device down.

This is the design documented in this repository, and the one you should build.

![Design 3 Product Photo](images/design3_main.png)
![Design 3 With Antenna](images/design3_antenna.png)
![Design 3 Battery Open](images/design3_battery_open.png)
![Design 3 LED Indicator](images/design3_leds.png)
![Design 3 Ports](images/design3_ports.png)
![Design 3 Sketch](images/design3_sketch.png)
![Design 3 CAD Exploded](images/design3_cad_exploded.png)

---

## Features

- 📡 LoRa mesh communication via Meshtastic (862–930 MHz)
- 📱 Bluetooth app control — no screen needed, your phone is the interface
- 🔋 Dual 18650 hot swappable batteries — up to 30 hours runtime
- ⚡ USB-A power output — doubles as a power bank for your phone
- 🔌 USB-C and Micro USB charging inputs
- 🧲 Magnetic battery panel — tool free battery swaps in seconds
- 📶 External SMA antenna — detachable for pocket carry, attachable for max range
- 🔴 Battery indicator LEDs — check charge at a glance
- 🖨️ Fully 3D printable enclosure in PLA
- 🌍 Open source hardware and software

---

## What You Need to Build One

### Electronics

| Component | Supplier | Approx Cost |
|---|---|---|
| XIAO ESP32S3 + Wio SX1262 Kit | [The Pi Hut](https://thepihut.com/products/xiao-esp32s3-wio-sx1262-kit-for-meshtastic-lora) | £10.50 |
| 2-Way 18650 Battery Holder with BMS | [The Pi Hut](https://thepihut.com/products/2-way-18650-battery-holder) | £8–£15 |
| 2x 18650 Li-Ion Cells (not included) | Any reputable supplier | £5–£15 |
| SMA Female Bulkhead Connector | Amazon / AliExpress | £1–£3 |
| SMA 868MHz Whip Antenna | Amazon / AliExpress | £2–£5 |
| U.FL to SMA Pigtail Cable | Amazon / AliExpress | £1–£3 |
| M4 Button Head Screws (x8) | Local hardware store | £1 |
| Neodymium Magnets (x4, ~10mm dia) | Amazon / AliExpress | £2–£4 |
| **Total** | | **~£30–£55** |

### Tools and Materials

- FDM 3D printer (any well calibrated machine will do)
- Black PLA filament — matte finish recommended
- Small screwdriver
- Soldering iron (for the SMA pigtail connection)
- Wire strippers

---

## How to Print the Enclosure

All STL files are in the `/CAD` folder of this repository.

**Recommended print settings:**
- Material: PLA or PLA+
- Layer height: 0.2mm
- Wall thickness: 2.4mm minimum (3 perimeter passes at 0.8mm)
- Infill: 20% honeycomb minimum
- Supports: Required for some features — check orientation notes in the CAD folder
- Print orientation: Primary load bearing faces parallel to print bed

If you're in a hot climate or leaving the device in a car, consider PETG instead of PLA — PLA starts to soften around 55°C which is a bad time.

---

## How to Flash Meshtastic

The XIAO ESP32S3 + Wio SX1262 kit comes pre-flashed with Meshtastic firmware straight out of the box, which is genuinely great. If you need to update or reflash it:

1. Go to 👉 [flasher.meshtastic.org](https://flasher.meshtastic.org)
2. Connect your device via USB-C
3. Select **XIAO ESP32S3** as your device
4. Click flash and wait about 30 seconds
5. Done. Seriously, that's it.

---

## How to Use It

1. Insert two 18650 cells into the battery compartment and close the magnetic panel
2. Press the power button on the top of the device
3. Download the **Meshtastic app** on your phone (iOS or Android — it's free)
4. Open the app, go to Bluetooth, and pair with your device
   - Default PIN: **123456**
5. Screw on the SMA antenna
6. You're on the mesh 🎉

From the app you can send messages, see other nodes on a map, configure channels, check battery level, and adjust settings. The device itself requires no further interaction — one button to rule them all.

---

## Assembly Guide

A full step by step assembly guide with photos is available in the `/Docs` folder of this repository. The short version:

1. Print all enclosure parts
2. Press fit the neodymium magnets into their pockets in the main body and battery panel
3. Route the U.FL to SMA pigtail cable from the LoRa module to the SMA bulkhead connector on the top of the enclosure
4. Place the battery management board and LoRa module into their respective compartments
5. Route power cables between the battery board and LoRa module
6. Secure the main enclosure halves with M4 button head screws
7. Insert batteries, close the magnetic panel, power on and test

---

## Project Context

This project was completed as part of an **HNC Engineering (Level 4) Unit 4001 — Engineering Design** assignment at college. The brief required the design and development of a sustainable, cost effective product through a structured iterative design process.

If you're a student looking at this as an example — hi 👋 — the key things the assignment covered were:

- Product Design Specification (PDS)
- Stakeholder analysis
- Three iterative design concepts in SolidWorks
- Structural analysis using SolidWorks Simulation
- Design evaluation using a weighted Pugh matrix
- Design considerations covering material, lifecycle, repairability, sustainability, standards compliance, and more
- A formal engineering design report

The full written assignment and SolidWorks files are included in this repository for reference.

---

## Licence

This project is released under the **MIT Licence** — do whatever you want with it, just give a nod to the original. See `LICENSE` for the full terms.

The Meshtastic firmware is a separate open source project — full credit and attribution to the Meshtastic team and community. Find them at [meshtastic.org](https://meshtastic.org).

---

## A Note on Safety Communication

Meshtastic is not a replacement for emergency services. If someone is in danger, call 999.

What it *is* genuinely useful for is **backup communication** in situations where conventional infrastructure is unavailable, degraded, or congested. Used as part of a wider preparedness strategy alongside conventional communication methods, a small network of Meshtastic devices provides a resilient, infrastructure independent communication layer that costs very little to deploy and requires no ongoing subscription or maintenance.

For event safety teams, mountain rescue support groups, remote work crews, and outdoor enthusiasts — it's worth thinking about seriously.

---

*Built with SolidWorks, printed in PLA, powered by 18650s, and fuelled by an unhealthy interest in radio waves. 📡*

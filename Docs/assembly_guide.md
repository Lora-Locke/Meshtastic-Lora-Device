# Assembly Guide 🔧

This guide walks you through assembling your LoRa Meshtastic device 
from scratch. It's not complicated, but read through the whole thing 
before you start so you know where you're headed. 
Nobody likes getting to step 6 and realising they forgot step 2.

Photos of the assembly process will be added to this folder soon.

---

## Before You Start

Make sure you have everything from the BOM ready before you begin. 
See [BOM.md](BOM.md) for the full components list and where to get them.

You'll also need your 3D printed enclosure parts ready. 
Print settings and STL files are in the `/CAD` folder of this repository.

### Tools Required

- Soldering iron and solder
- Wire strippers
- Small Phillips head screwdriver
- Superglue
- Needle nose pliers (helpful but not essential)
- Multimeter (recommended for checking connections before closing up)

---

## Parts Overview

Before you start, lay out your printed parts and familiarise yourself 
with them:

- **Back half of case** — houses the 18650 battery board and cells
- **Front half of case** — houses the XIAO LoRa module and internal plate
- **Internal plastic plate** — sits inside the front half, 
  holds the WiFi/BLE antenna
- **Magnetic battery panel** — the external cover for the battery 
  compartment, retained by magnets
- **Acrylic sheet** — sandwiches everything together on the front half, 
  secured by four screws

---

## Step 1 — Solder the Power Cables

Start by soldering two cables onto the **5V power rail** of the 
18650 battery management board. Each cable should be approximately 
**8cm long** — long enough to reach the XIAO module comfortably 
once everything is inside the case without being so long they 
become a tangled nightmare.

Once soldered, attach header pins to the free ends of the cables 
so they can plug directly into the XIAO ESP32S3 power input. 
This keeps the connection clean and means the board can be 
unplugged easily if you ever need to service it.

⚡ **Double check your polarity before moving on.** 
Positive to positive, negative to negative. 
Reversing this will kill the XIAO module instantly 
and there's no recovering from that. Ask me how I know. 🙃

---

## Step 2 — Superglue the Magnets

Before anything goes into the case, superglue the four neodymium 
magnets into their pockets in the **back half of the case** and into 
the **magnetic battery panel**.

⚠️ **Critical:** Test the polarity of each magnet before gluing. 
The magnets in the case and the panel need to **attract** each other. 
If you glue them in the wrong way round the panel will repel itself 
off the case which is both useless and embarrassing.

Hold each magnet in place for 30 seconds after applying glue 
and leave to fully cure before continuing.

---

## Step 3 — Install the SMA Connector

Press the SMA bulkhead connector into the hole at the top of the 
**front half of the case** and secure it with its locking nut. 
Firm but not overtightened — you're threading into printed plastic, 
not cast iron.

---

## Step 4 — Prepare the Internal Plastic Plate

Stick the **WiFi/BLE antenna** onto the internal plastic plate. 
This plate sits inside the front half of the case and the antenna 
lives on it, tucked neatly inside the enclosure.

Set this aside for now — it goes in during final assembly.

---

## Step 5 — Assemble the Back Half

Place the **18650 battery management board** into the back half 
of the case, routing the two power cables you soldered in Step 1 
toward the top of the case where the XIAO module will sit.

Insert your **18650 cells** into the battery holder.

Secure the back half of the case with the **first four screws**. 
These hold this half of the assembly together.

---

## Step 6 — Install the XIAO LoRa Module

Slot the **XIAO ESP32S3 + Wio SX1262 module** into its pocket 
at the top of the front half of the case.

Then:

1. Route the two power cables from the battery board and 
   plug them into the XIAO module header pins
2. Connect the **U.FL antenna extension to SMA pigtail** 
   to the LoRa antenna port on the Wio SX1262 module — 
   press it down firmly and straight until you feel a click, 
   this connector is small and does not appreciate being 
   forced at an angle
3. Plug the **WiFi/BLE antenna** cable onto its connector 
   on the XIAO module

---

## Step 7 — Test Before Closing

Before you button everything up, do a quick sanity check:

1. Press the power button on the battery board
2. Check the LED indicators light up
3. Open the Meshtastic app on your phone and confirm 
   the device appears over Bluetooth

If it works, great — power it back off and move to Step 8. 
If it doesn't, now is a vastly better time to find out 
than after you've put all the screws in.

---

## Step 8 — Close the Case

Bring the front half and back half of the case together, 
making sure all cables are routed neatly inside and nothing 
is being pinched at the join.

Slide the **internal plastic plate** (with the WiFi/BLE antenna 
attached) into its slot on the front of the case.

Push the **acrylic sheet** into place on the front of the case — 
this sandwiches the internal plate and antenna in position, 
holding everything securely without the need for additional fixings.

Finally, drive the remaining **four screws** through the acrylic sheet 
and front half of the case. These screws secure the whole assembly 
and hold the cables and antenna routing in place.

---

## Step 9 — Attach the Battery Panel and Antenna

Clip the **magnetic battery panel** over the battery compartment — 
the magnets will pull it into place automatically.

Screw on your **SMA whip antenna**.

Power on, open the Meshtastic app, set your region to **EU_868** 
for UK use, and you're on the mesh. 📡

---

## Tips and Common Mistakes

- **Check magnet polarity before gluing** — seriously, do this
- **Don't overtighten the screws** — printed threads strip easily, 
  snug is enough
- **Keep power cables to ~8cm** — too long and they'll bunch up 
  and cause problems when closing the case
- **Test before closing** — always, every time, no exceptions
- **Set your region in the app** — EU_868 for UK, 
  check Meshtastic docs for your region if you're elsewhere

---

## Need Help?

Open an issue on this repository and we'll help where we can. 
The Meshtastic Discord community is also extremely active and helpful — 
link in the [firmware guide](../Firmware/flashing_guide.md).

---

*Assembly photos coming soon — the device will be disassembled 
and photographed step by step to accompany this guide.* 📸

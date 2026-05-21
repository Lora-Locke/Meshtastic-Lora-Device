# Product Design Specification (PDS) 📄

> This PDS was produced as part of an HNC Engineering Design (Unit 4001) 
> college assignment. It represents the initial design brief created at 
> the start of the project which all three designs were measured against. 
> If you're a student looking at this as an example — hi 👋 — feel free 
> to use this as a reference for how to structure your own PDS, 
> but make sure you write your own version in your own words!

---

## Product Information

| Field | Detail |
|---|---|
| Designer | Theo Locke |
| Product Name | Long Range Communication Device using Meshtastic (LoRa) |
| Date | March 2026 |
| Project Context | HNC Engineering Design — Unit 4001 |

---

## What I Am Trying to Achieve

The goal of this project is to design and build a case which can house 
a LoRa Meshtastic radio module with a built in battery, small enough 
to fit in a pocket and be carried around on a daily basis for 
off grid communication. An additional goal is the possibility of 
the device also functioning as a portable battery pack for charging 
other devices such as a smartphone.

The enclosure must be made from as sustainable and environmentally 
friendly a material as possible, with PLA identified as a strong 
candidate due to its bio-based origin from corn starch.

---

## How LoRa Mesh Networks Work

LoRa (Long Range) is a wireless communication method that allows 
devices to send small messages over several kilometres whilst using 
very little power. Rather than relying on mobile networks, WiFi, 
or the internet, LoRa devices communicate directly with each other 
using radio waves on licence exempt frequencies.

LoRa mesh networks enable long range, off grid communications by 
allowing individual LoRa nodes to relay messages to each other 
through a series of hops — from one node to another — until the 
message reaches its destination.

> *"Meshtastic is a project that enables you to use inexpensive LoRa 
> radios as a long range off-grid communication platform in areas 
> without existing or reliable communications infrastructure. 
> This project is 100% community driven and open source!"*
> — [meshtastic.org](https://meshtastic.org/docs/introduction/)

Meshtastic is the firmware used by this device to join and operate 
within the mesh network. Full documentation is available at:
👉 [meshtastic.org/docs/introduction](https://meshtastic.org/docs/introduction/)

---

## Core Requirements

These are the non-negotiable requirements the final design must meet:

| # | Requirement | Reason |
|---|---|---|
| 1 | Device must be pocketable — fit in an average size pocket | Everyday carry use case |
| 2 | Easy to charge via a standard connector, ideally with fast charge support | Convenience and accessibility |
| 3 | Total cost below £50 as a kit or pre-built product | Accessibility for hobbyists and makers |
| 4 | Universal power and data port if no built in battery | Interoperability |
| 5 | Minimum 5km communication range with mesh hopping | Core functional requirement |
| 6 | Must support Meshtastic firmware | Core functional requirement |
| 7 | Enclosure material must be as sustainable as possible | Brief requirement |

---

## Optional Features and Possible Extras

These are desirable but not essential — nice to haves that would 
add value if achievable within the design constraints:

- MagSafe compatibility for attaching to the back of an iPhone
- Small enough to hold comfortably in one hand or attach to the 
  back of a phone
- Internal or external antenna depending on the chosen module and 
  design iteration
- Hot swappable battery — either for end of life replacement or 
  field swapping without powering down

> **Note:** The hot swap battery feature made it into the final 
> Design 3 via a magnetic battery panel — one of the most satisfying 
> moments of the whole project. 🧲

---

## Standards and Regulatory Requirements

| Standard | Description |
|---|---|
| ETSI EN 300 220 | UK and EU standard governing short range radio devices operating at 868MHz |
| Ofcom IR 2030 | UK Interface Requirement governing licence exempt LoRa operation |
| LoRa Alliance Network Protocol | Governs the LoRaWAN protocol and interoperability between devices |

---

## Operational Parameters

| Parameter | Value |
|---|---|
| Frequency range | 863 – 870 MHz |
| Regulatory framework | Ofcom IR 2030, ETSI EN 300 220 |
| Firmware | Meshtastic |
| Connectivity | Bluetooth Low Energy (BLE) to smartphone |

---

## Material Notes

PLA (Polylactic Acid) was identified early in the project as the 
preferred enclosure material. It is derived from renewable resources 
such as corn starch, making it significantly more sustainable than 
petroleum based alternatives such as ABS or PETG. It is also the 
most widely used FDM printing material, keeping the barrier to 
community manufacture as low as possible.

Recycled PLA was also considered and is documented as a preferred 
option where available in the full design considerations section 
of the assignment report.

---

## How Did the Final Design Measure Up?

Looking back at the PDS from the end of the project, here is how 
Design 3 — the final chosen design — performed against each requirement:

| Requirement | Met? | Notes |
|---|---|---|
| Pocketable | ✅ Partially | Fits jacket and cargo pockets comfortably. Trouser pockets are tight at 130mm length |
| Easy to charge | ✅ Yes | USB-C and Micro USB inputs, plus USB-A output |
| Under £50 | ✅ Yes | BOM cost £24–£50 depending on sourcing |
| Universal port | ✅ Yes | USB-C on all designs |
| 5km+ range | ✅ Yes | External SMA antenna on Design 3 improves range significantly |
| Meshtastic compatible | ✅ Yes | XIAO kit comes pre-flashed |
| Sustainable material | ✅ Yes | Matte black PLA enclosure throughout |
| Hot swap battery | ✅ Yes | Magnetic panel on Design 3 enables tool free hot swap |

---

## References

[1] Meshtastic, "Meshtastic Introduction," [Online]. 
Available: https://meshtastic.org/docs/introduction/. 
[Accessed 17 03 2026].

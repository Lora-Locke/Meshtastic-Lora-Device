# CAD Files 🖨️

This folder contains the 3D printable STL file for the 
LoRa Meshtastic device enclosure.

---

## Files

| File | Description |
|---|---|
| `Meshtastic Device 3D.stl` | Complete enclosure — contains both the front and back halves of the case, the internal plastic plate, and the magnetic battery panel |

---

## Print Settings

| Setting | Recommended Value |
|---|---|
| Material | PLA or PLA+ |
| Layer height | 0.2mm |
| Wall thickness | 2.4mm minimum (3 perimeter passes) |
| Infill | 20% honeycomb minimum |
| Supports | Yes — required for some features |
| Print orientation | Primary load bearing faces parallel to print bed |

---

## Notes

- Matte black PLA is recommended for the best finish — 
  it hides layer lines effectively and looks great
- If you're in a hot climate or the device will be left in a car, 
  consider PETG instead — PLA softens at around 55°C which is 
  not ideal on a hot sunny day 🌞
- All parts are included in the single STL file — 
  import it into your slicer and arrange the parts on the build plate
- Recommended slicers: PrusaSlicer, Cura, Bambu Studio

---

## Hardware Required

Once printed you'll need the following to complete the build:

- M4 button head screws x8
- Neodymium magnets x4 (approx 10mm diameter)
- Superglue (for securing magnets)

Full assembly instructions are in the `/Docs` folder. 
Full BOM is in `/Docs/BOM.md`.

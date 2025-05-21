# 3d-printed-uv-pcb-mask
An alternative version to make PCBs at home using a 3D printer instead of laser or inkjet paper printer

> [!CAUTION]
> This method isn't perfect, and it's pretty much under work, there's a lot to improve and probably it'll never be a perfect method

This open-source method describes a **fast**, **reliable**, and **reusable** way to create UV exposure masks for PCB fabrication using a 3D printer and dual-filament technique. Developed through trial and error, this approach replaces the traditional printed transparencies or toner transfers with a clean 10-minute print.

---

## Why This Exists

Traditional methods for making UV masks (inkjet/laser transparencies, toner transfer) are:
- Unreliable (small holes where ink is supposed to be) or blurry
- A pain to handle with repeated use

This technique solves that by using **black and translucent PLA** in one fused part to generate **opaque traces** and **transparent background** for UV light.

---

## Materials

| Item | Details |
|------|---------|
| 3D Printer | With **Optional** AMS/multi-material capability (e.g., Bambu X1C, Prusa MMU) |
| Filament | Black PLA + **Optional** Translucent / White PLA or any other filament which is more UV resistant|
| Nozzle | 0.2mm (recommended) but 0.4mm can work too|
| Layer Height | 0.08mm - 0.1mm|
| PCB Material | Pre-sensitized UV board or Dry photosensitive sheet |
| UV Light Source | 365–405nm recommended |
| Etching Setup | Ferric chloride, sodium persulfate, etc. |
| Flat Print Bed | No textured surface for better definition altough it is possible with textured bed as well |

---

## 3D Printing Tips

- Use **black PLA** for trace lines and **translucent/white PLA** for the light-pass areas.
- Slicer must **respect per-layer material changes**, set via modifier meshes or image extrusion tools.
- Mask files are exported as STEP from Gerber images, or drawn directly in CAD.
- Make sure **mask surface faces downward**, flat on the bed, with no warping.

---

## Exposure & Etching

- Place printed mask directly on copper board.
- Weigh down with a clear acrylic sheet or glass piece for tight contact.
- Typical UV exposure: **1–5 minutes** depending on light strength.
- Etch normally. Resulting traces should be clean and well-defined.

---

## Gallery & Results

Check `images` for microscope photos and versions:

| Version | Improvements |
|---------|--------------|
| v1 | 0.4mm nozzle, black PLA, textured bed – blurry, failed exposure |
| v2 | 0.2mm nozzle, textured bed – improved edges, sharper mask |
| v3 | Dual-filament with translucent PLA and black PLA – reliable, fast, reusable |

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Blurry edges | Use smaller nozzle (0.2mm) and fine layer height |
| Overexposure | Reduce UV time or increase opacity of black PLA |
| Mask curls | Ensure flat bed and solid adhesion |
| Light bleeding | Use dark filament and flat bed or more weight|

---


---

## My Setup

| Component           | Details                    |
|---------------------|----------------------------|
| 3D Printer          | Bambu Lab A1 Mini          |
| Nozzle Size         | 0.2 mm                     |
| Print Bed           | Super Tack Bed Sheet       |
| Black Filament      | Creality Black PLA         |
| Translucent Filament| Elegoo Translucent PLA     |
| PCB Material        | Dry Photosensitive Sheet   |
| Etchant             | Ferric Chloride            |
| Neutralizer         | Sodium Carbonate           |
| UV Light Source     | 365 nm LED Strips (8.64 W/m) |
| Post-processing Tool| Laminator                  |
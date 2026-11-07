# ESP32-S3 USB Module (KiCad)

An ESP32-S3 USB module designed in KiCad 10, taken from schematic to PCB layout, DRC checks, and 3D review.

> **Credit:** Built by following The Design Graveyard's YouTube tutorial: [paste video link here]

![3D view](<img width="1920" height="1136" alt="3d-view" src="https://github.com/user-attachments/assets/dd68b378-b86d-48ef-a34e-f895f1356121" />).

## What's in this repo
- `ESP32_USB.kicad_sch`: schematic
- `ESP32_USB.kicad_pcb`: PCB layout
- `ESP32_USB.kicad_pro`: KiCad project file
- `images/`: 3D render, schematic, and PCB screenshots

## Design overview
- **Power:** USB 5V is regulated to 3.3V by an AMS1117, with 10µF decoupling caps on input and output.
- **Reset and boot:** A 10k pull-up and 1µF cap on the EN pin give a clean power-on reset. The BOOT button pulls IO0 low to enter flash mode.
- **USB:** D+ and D- connect directly to the ESP32-S3's native USB pins, so no USB-UART chip is needed.
- **Antenna:** A keep-out zone keeps copper and ground away from the antenna to protect range.
- **Routing:** USB D+/D- are routed as a short, matched pair.

## Schematic and PCB
![Schematic](<img width="1920" height="1143" alt="schematic" src="https://github.com/user-attachments/assets/2fa8a9b4-8a90-4c9f-ad11-6a52affb3026" />
)
![PCB layout](<img width="1920" height="1138" alt="pcb-layout" src="https://github.com/user-attachments/assets/8ea913ea-e4f5-4cf1-8874-416bc6b6d493" />
)

## What I learned
- Schematic capture, footprint assignment, and PCB routing in KiCad
- Why the antenna needs a keep-out zone
- How DRC catches layout errors
- [Add one honest line, e.g. "Routing took far longer than the schematic."]

## Next steps
Design a board completely from scratch.

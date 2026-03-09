# Fabrication

This folder contains the PCB layout and manufacturing files for the circular patch antenna prototype.

## Workflow

1. Final geometry exported from FEKO as a **STEP file**
2. Imported into **FreeCAD** for geometric adjustments and format conversion
3. Imported into **EasyEDA** to define the feed port, ground plane, and layer stack
4. **Gerber files** generated from EasyEDA and submitted to JLCPCB for fabrication
5. SMA edge connector soldered manually after receiving the board

## PCB Specifications

| Parameter | Value |
|---|---|
| Substrate | FR4 |
| Substrate thickness | 1.6 mm |
| Board dimensions | 30 × 30 mm |
| Copper layers | 2 (patch + ground plane) |
| Fabrication service | JLCPCB (standard 2-layer) |
| Connector | SMA edge mount |

## Contents

- Gerber files — ready for PCB fabrication
- EasyEDA project files — editable layout source

## Notes

The fabricated substrate thickness (1.6 mm) differs slightly from the simulation model (1.575 mm). Combined with the typical permittivity variation of commercial FR4, this accounts for the ~225 MHz downward frequency shift observed experimentally (resonance at 5.485 GHz vs. 5.72 GHz in simulation). Despite this shift, the prototype achieved a stronger adaptation (−42.4 dB) and a wider measured bandwidth than the simulation predicted.

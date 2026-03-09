# Fabrication

This folder contains the PCB layout and manufacturing files for the circular patch antenna prototype.

## Workflow

1. Final geometry exported from FEKO as **STEP files** (see `cad/` folder)
2. STEP files imported into **FreeCAD** for geometric adjustments
3. **DXF files** exported from FreeCAD and imported into **EasyEDA** to define the feed port, ground plane, and layer stack
4. **Gerber files** generated from EasyEDA and submitted to JLCPCB for fabrication
5. SMA edge connector soldered manually after receiving the board

## Contents

| File | Description |
|---|---|
| `Antena Parche Circular.dxf` | Patch and feed line exported from FreeCAD — ground plane slot not included, see separate file below |
| `groundplane Parche Circular.dxf` | Ground plane exported separately from FreeCAD to preserve the coupling slot geometry |
| `full model Antena Parche Circular.dxf` | Complete assembly exported from FreeCAD, used as visual reference |
| `Antena Parche Circular.epro` | EasyEDA project file — open this to edit the PCB layout and re-export Gerbers |
| `Gerber_Antena_Parche_Circular_PCB1_2026-03-09.zip` | Gerber files ready for PCB fabrication |

## Why Three DXF Files?

The ground plane contains a coupling slot that does not export correctly in the full model DXF. For this reason the geometry was split into separate files: one with the patch and feed line, and one with the ground plane including the slot. The third DXF is the full assembly exported from FreeCAD, useful as a visual reference.

To reproduce or modify the PCB layout, open `Antena Parche Circular.epro` directly in EasyEDA — all layers are already defined there and new Gerbers can be exported from it.

## PCB Specifications

| Parameter | Value |
|---|---|
| Substrate | FR4 |
| Substrate thickness | 1.6 mm |
| Board dimensions | 30 × 30 mm |
| Copper layers | 2 (patch + ground plane) |
| Fabrication service | JLCPCB (standard 2-layer) |
| Connector | SMA edge mount |

## Notes

The fabricated substrate thickness (1.6 mm) differs slightly from the simulation model (1.575 mm). Combined with the typical permittivity variation of commercial FR4, this accounts for the ~225 MHz downward frequency shift observed experimentally (resonance at 5.485 GHz vs. 5.71 GHz in simulation). Despite this shift, the prototype achieved a stronger adaptation (−42.4 dB) and a wider measured bandwidth than predicted.

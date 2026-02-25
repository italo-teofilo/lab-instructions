# Bambu Lab AMS (Automatic Material System) - Technical Overview

## 1. Introduction
The **AMS (Automatic Material System)** is an intelligent material management unit designed by Bambu Lab. It automates the process of filament feeding, retraction, and switching, allowing for multi-color and multi-material 3D printing. It actively communicates with the printer's toolhead to ensure smooth transitions and supports features like automatic spool backup.



## 2. How the AMS Works
The AMS operates through a synchronized workflow involving multiple sensors and motors to actively push and pull filament.

* **Intelligent Feeding System:** Unlike traditional passive spool holders, the AMS has active motors for each filament slot. It pushes filament forward towards the extruder and pulls it back (rewinds) onto the spool when unloading.
* **Filament Path:**
    1.  **Filament Slots:** The user inserts filament into one of the 4 slots. A sensor detects the filament and automatically pre-loads it.
    2.  **Filaments Hub:** Located at the base of the AMS, this merges the 4 filament paths into one. It uses a brushless motor and a magnetic rotary encoder to drive the filament for the second stage.
    3.  **Filament Buffer (Standard AMS only):** Located on the back of the printer, the buffer regulates tension. It uses a slide and spring mechanism with a Hall sensor to ensure the toolhead pulls filament without excessive resistance.
* **RFID Recognition:** The AMS features an RFID reader that automatically detects official Bambu Lab spools, syncing the filament type, color, and remaining capacity directly to the Bambu Studio slicer.



## 3. Types of AMS
There are currently two distinct versions of the AMS ecosystem, designed for different printer series.

### A. Bambu Lab AMS (Standard)
The original enclosed unit designed for the **X1** and **P1** series printers.
* **Enclosed Design:** It features an airtight lid with silicone seals and desiccant slots, keeping hygroscopic materials (like Nylon or PC) dry during printing.
* **Expandability:** Up to 4 AMS units can be connected via an **AMS Hub**, allowing for printing with up to **16 different colors/materials** simultaneously.
* **Compatibility:** X1 Series, P1 Series.

### B. Bambu Lab AMS Lite
A simplified, open-frame unit designed specifically for the **A1** series printers.
* **Open Design:** The spools are exposed to the air. It does not provide humidity protection.
* **Mechanism:** It uses a rotary spool holder system that grips the spool from the center hole (Spool Claw) rather than rolling it on bottom rollers. This makes it more tolerant of different spool types, including cardboard spools.
* **Compatibility:** A1, A1 Mini.



## 4. Comparison: AMS vs. AMS Lite

| Feature | Standard AMS | AMS Lite |
| :--- | :--- | :--- |
| **Printer Compatibility** | X1 Series, P1 Series | A1 Series (A1, A1 Mini) |
| **Enclosure** | Fully Enclosed (Airtight) | Open Air |
| **Humidity Control** | Yes (Desiccant slots + Seals) | No |
| **Max Capacity** | 4 Spools (Expandable to 16) | 4 Spools (Not Expandable) |
| **Filament Buffer** | External (Back of printer) | Not required |
| **Spool Compatibility** | Strict (Plastic preferred) | Flexible (Cardboard friendly) |

## 5. Important Technical Notes & Constraints

* **Filament Limitations:**
    * **TPU:** Generally **NOT** supported in the AMS due to its flexibility; it can jam the long internal filament path.
    * **Abrasive Materials:** Materials like CF (Carbon Fiber) are supported but can wear down internal PTFE tubes and funnels.
    * **Cardboard Spools:** In the **Standard AMS**, cardboard spools can slip on the rollers. It is officially recommended to use spool adapters.
* **Spool Dimensions:** The standard AMS has strict size limits (Width: 50-68mm, Diameter: 197-202mm).



***

**References:**
* [Bambu Lab Wiki - Intro to AMS](https://wiki.bambulab.com/en/x1/manual/intro-ams)
* [Bambu Lab - Compare AMS](https://bambulab.com/pt-br/compare/ams)

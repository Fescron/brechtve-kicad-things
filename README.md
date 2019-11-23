
# KiCad

![License](https://img.shields.io/badge/licence-CC%20BY--SA%204.0-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/Fescron/KiCad.svg)
<!--
[GitHub Release Date](https://img.shields.io/github/release-date/Fescron/KiCad.svg)
[GitHub release](https://img.shields.io/github/release/Fescron/KiCad.svg)
-->

This repository is a collection of all of my self-made footprints and symbols for [KiCad](http://www.kicad-pcb.org/) among with important settings and some shortcuts.

<br/>

## Table of Contents

- [KiCad](#kicad)
  - [Table of Contents](#table-of-contents)
  - [1 - Tips & Tricks](#1---tips--tricks)
  - [2 - Board Setup](#2---board-setup)
  - [3 - PCB design](#3---pcb-design)
    - [3.1 - Much used things](#31---much-used-things)
    - [3.2 - Grid](#32---grid)
    - [3.3 - Fills](#33---fills)
  - [4 - Gerber generation](#4---gerber-generation)
    - [4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)](#41---pcbway-quick-turn-pcb-as-of-21112019)
  - [5 - Footprints and Libraries](#5---footprints-and-libraries)
  - [Terms of Use](#terms-of-use)

<br/>

## 1 - Tips & Tricks

- **Watch out for top/bottom views on mechanical drawings!!**
- Ohm sign: `Ω`
<!-- fix vertical spacing -->
- Snap component/symbol to grid: `m` (move) & `ctrl + shift`
- Fill all zones: `b` (PCB design)
<!-- fix vertical spacing -->
- Grid: 50 mils (schematic)
<!-- fix vertical spacing -->
- PCB thickness: 1,6 mm
- Copper weight: 35 µm (1 oz)

<br/>

## 2 - Board Setup

See [this](board-setup.md) file.

<br/>

## 3 - PCB design

Use **rounded corners** with a diameter of **75 mils (0,0750 inch)**.

<br/>

### 3.1 - Much used things

| Symbol                                | Package                                                             | Dimensions                                             |
| ------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------ |
| `SparkFun-PowerSymbols: XXXX`         | VDD, GND, VDDA                                                      |                                                        |
| `power: XXX`                          | PWR_FLAG, GNDA, GNDPWR, +15V                                        |                                                        |
|                                       |                                                                     |                                                        |
| `Device: R/C/L_Small`                 | `XXXX_SMD: X_0805_XXXX_HandSolder`                                  | Pads: 1,15 mm x 1,40 mm                                |
|                                       |                                                                     |                                                        |
| `Device: Jumper_XX_Small`             | `Connector_PinHeader_2.54mm: PinHeader_1x02_P2.54mm_Vertical`       | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
| `Jumper: SolderJumper_3_Bridged12`    | `Jumper: SolderJumper-3_P1.3mm_Bridged12_Pad1.0x1.5mm_NumberLabels` |                                                        |
|                                       |                                                                     |                                                        |
| `Connector: TestPoint`                | `TestPoint: TestPoint_THTPad_D2.0mm_Drill1.0mm`                     | Drill: 1 mm - Pad: 2 mm                                |
| `Connector_Generic: Conn_XXxXX`       | `Connector_PinHeader_2.54mm: PinHeader_XXXX`                        | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
|                                       | `PhoenixContact: PTSA 1,5 XXXX`                                     | 2 Contacts - Spacing pads: 3,5 mm - Diam. wire: 1,5 mm |
|                                       |                                                                     |                                                        |
| `Mechanical: MountingHole`            | `MountingHole: MountingHole_3.2mm_M3`                               | Diameter hole: 3,2 mm                                  |
| `Switch: SW_Push`                     | `Button_Switch_SMD: SW_SPST_FSMSM`                                  | Pads: 2,18 mm x 1,60 mm - Distance between pads: 7 mm  |
|                                       |                                                                     |                                                        |
| **TODO: Make own symbol**             | `Connector: Tag-Connect_TC2050-IDC-FP_2x05_P1.27mm_Vertical`        | 2x5 TagConnect with legs                               |
| **TODO: Make own symbol**             | **TODO: ARM 1.27mm standard Cortex Debug**                          |                                                        |
| **TODO: Make own symbol**             | **TODO: UART TX RX GND VCC**                                        |                                                        |
|                                       |                                                                     |                                                        |
| `CreativeCommons: Symbol_CC-XXXX_5mm` | `CreativeCommons: Symbol-CC-BY-SA-v4-SilkMask-5mm`                  | Height: 5 mm                                           |
|                                       | `KiCadLogo: KiCad-Logo2_5mm_SilkMask`                               | Height:  5mm                                           |

| Connector Package | Pitch   | Usage                            |
| ----------------- | ------- | -------------------------------- |
| Molex KK 254      | 2,54 mm | Dupont but polarized             |
| JST-XH            | 2,54 mm | **TODO: Usage?**                 |
| JST-PH            | 2 mm    | Lithium batteries, STEMMA, Grove |
| JST-SH            | 1 mm    | STEMMA QT, Qwiic                 |

**TODO: Add KiCad packages?**

<br/>

### 3.2 - Grid

- Draw the PCB in inches!
- Regular: 25 mils (0,6350 mm)
- Fine: 5 mils (0,2540 mm)

<br/>

### 3.3 - Fills

The default values are fine:

- Clearance: 20 mils (0,508 mm)
- Minimum width: 10 mils (0,254 mm)
- Thermal clearance: 20 mils (0,508 mm)
- Thermal spoke width: 20 mils (0,508 mm)

<br/>

## 4 - Gerber generation

### 4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)

- Check the `Protel` box
- Drill files: Check the `suppress leading zeros` and `minimal header` boxes

<br/>

## 5 - Footprints and Libraries

See [this](footprints-libraries.md) file.

<br/>


## Terms of Use

**Copyright (C) 2019 - Brecht Van Eeckhoudt**

This documentation is licensed under a CreativeCommons **Attribution-ShareAlike 4.0 International** licence (*CC BY-SA 4.0*). Find more info at: https://creativecommons.org/licenses/by-sa/4.0/

[![License: CC BY-SA 4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/)

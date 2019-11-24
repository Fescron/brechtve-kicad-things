
# KiCad

![License](https://img.shields.io/badge/licence-CC%20BY--SA%204.0-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/Fescron/KiCad.svg)
<!--
[GitHub Release Date](https://img.shields.io/github/release-date/Fescron/KiCad.svg)
[GitHub release](https://img.shields.io/github/release/Fescron/KiCad.svg)
-->

This repository is a collection of all my commonly used settings/symbols/packages and selfmade footprints/symbols among with a page layout containing [CERN Open Hardware Licence](https://ohwr.org/cernohl) information. These can be used in the schematic editor and PCB layout program [KiCad](http://www.kicad-pcb.org/).

<br/>

## Table of Contents

- [KiCad](#kicad)
  - [Table of Contents](#table-of-contents)
  - [1 - Tips & Tricks](#1---tips--tricks)
  - [2 - Board Setup](#2---board-setup)
  - [3 - PCB design](#3---pcb-design)
  - [4 - Gerber generation](#4---gerber-generation)
    - [4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)](#41---pcbway-quick-turn-pcb-as-of-21112019)

<br/>

## 1 - Tips & Tricks

- **Watch out for top/bottom views on mechanical drawings!!**
- Ohm sign: `Ω`
<!-- fix vertical spacing -->
- Snap component/symbol to grid: `m` (move) & `ctrl + shift`
- Fill all zones: `b` (PCB design)
<!-- fix vertical spacing -->
- Draw the PCB in inches!
- Use **rounded PCB corners** with a diameter of **75 mils (0,0750 inch)**.
<!-- fix vertical spacing -->
- PCB thickness: 1,6 mm
- Copper weight: 35 µm (1 oz)

|            | Grid size |             | Usage    |
| ---------- | --------- | ----------- | -------- |
| Schematic  | 50 mils   |             | Standard |
| PCB layout | 25 mils   | (0,6350 mm) | Standard |
| PCB layout | 5 mils    | (0,2540 mm) | Fine     |

| Standard board information |
| ------------------- |
| <pre>`< project title >         v1.0`<br/>`Licensed under CERN OHL v.1.2.`<br/>`github.brechtve.be`     `01/2020`</pre> |

| Resistor package | Power dissipation | Usage                      |     | Diode package | Other name | Size   |
| ---------------- | ----------------- | -------------------------- | --- | ------------- | ---------- | ------ |
| 0603             | 1/10 W = 100 mW   |                            |     | DO-214AC      | SMA        | Small  |
| 0805             | 1/8 W = 125 mW    | Hand soldering             |     | DO-214AA      | SMB        | Middle |
| 1206             | 1/4 W = 250 mW    | Power sensing (i.e. 0,1Ω) |     | DO-214AB      | SMC        | Large  |

<br/>

## 2 - Board Setup

See [THIS](board-setup.md) file.

<br/>

## 3 - PCB design

| Commonly used symbol                                    | Commonly used package                                                               | Dimensions                                             |
| ------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------ |
| `SparkFun-PowerSymbols: XXXX`                           | VDD, GND, VDDA                                                                      |                                                        |
| `power: XXXX`                                           | PWR_FLAG, GNDA, GNDPWR, +15V                                                        |                                                        |
|                                                         |                                                                                     |                                                        |
| `Device: R/C/L_Small`                                   | `XXXX_SMD: X_0805_XXXX_HandSolder`                                                  | Pads: 1,15 mm x 1,40 mm                                |
|                                                         |                                                                                     |                                                        |
| `Device: Jumper_XX_Small`                               | `Connector_PinHeader_2.54mm: PinHeader_1x02_P2.54mm_Vertical`                       | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
| `Jumper: SolderJumper_3_Bridged12`                      | `Jumper: SolderJumper-3_P1.3mm_Bridged12_Pad1.0x1.5mm_NumberLabels`                 |                                                        |
|                                                         |                                                                                     |                                                        |
| `Connector: TestPoint`                                  | `TestPoint: TestPoint_THTPad_D2.0mm_Drill1.0mm`                                     | Drill: 1 mm - Pad: 2 mm                                |
| `Connector_Generic: Conn_XXxXX`                         | `Connector_PinHeader_2.54mm: PinHeader_XXXX`                                        | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
|                                                         | `Connector_Phoenix_PTSA_extra: PhoenixContact_PTSA_1,5_2-G-3,5_1x02_P3.50mm_Angled` | 2 Contacts - Spacing pads: 3,5 mm - Diam. wire: 1,5 mm |
|                                                         |                                                                                     |                                                        |
| `Mechanical: MountingHole`                              | `MountingHole: MountingHole_3.2mm_M3`                                               | Diameter hole: 3,2 mm                                  |
| `Switch: SW_Push`                                       | `Button_Switch_SMD: SW_SPST_FSMSM`                                                  | Pads: 2,18 mm x 1,60 mm - Distance between pads: 7 mm  |
|                                                         |                                                                                     |                                                        |
| **TODO: Make own symbol**                               | `Connector: Tag-Connect_TC2050-IDC-FP_2x05_P1.27mm_Vertical`                        | 2x5 TagConnect with legs                               |
| **TODO: Make own symbol**                               | **TODO: ARM 1.27mm standard Cortex Debug**                                          |                                                        |
| **TODO: Make own symbol**                               | **TODO: UART TX RX GND VCC**                                                        |                                                        |
|                                                         |                                                                                     |                                                        |
| `BrechtVE_Aesthetics: Symbol_OSHW-EEVBLOG_SPFMDBC_10mm` | `BrechtVE_Aesthetics: OSHW-EEVBLOG2_SPFMDBC_SolderMaskTop_5mm`                      | Height: 5 mm                                           |
|                                                         | `BrechtVE_Aesthetics: KiCad-Logo2_SilkScreenMaskTop_5mm`                            | Height:  5mm                                           |

| Connector package | Pitch   | Usage                            |
| ----------------- | ------- | -------------------------------- |
| Molex KK 254      | 2,54 mm | Dupont but polarized             |
| JST-XH            | 2,54 mm | **TODO: Usage?**                 |
| JST-PH            | 2 mm    | Lithium batteries, STEMMA, Grove |
| JST-SH            | 1 mm    | STEMMA QT, Qwiic                 |

**TODO: Add KiCad packages?**

| Fill setting        | Size    | (default sizes are fine) |
| ------------------- | ------- | ------------------------ |
| Clearance           | 20 mils | (0,508 mm)               |
| Minimum width       | 10 mils | (0,254 mm)               |
| Thermal clearance   | 20 mils | (0,508 mm)               |
| Thermal spoke width | 20 mils | (0,508 mm)               |

<br/>

## 4 - Gerber generation

### 4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)

- Check the `Use Protel filename extensions` box
- Drill files:
  - Check the `suppress leading zeros` and `minimal header` boxes
  - Uncheck the `PTN and NPTH in single file` box 

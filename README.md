
# KiCad Things

![Shortcut](https://img.shields.io/badge/website-kicad.brechtve.be-yellow)
![License](https://img.shields.io/badge/licence-CC%20BY--SA%204.0-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/Fescron/brechtve-kicad-things.svg)
<!--
[GitHub Release Date](https://img.shields.io/github/release-date/Fescron/KiCad.svg)
[GitHub release](https://img.shields.io/github/release/Fescron/KiCad.svg)
-->

This repository is a collection of all my commonly used settings/symbols/packages and selfmade footprints/symbols among with a page layout containing [CERN Open Hardware Licence](https://ohwr.org/cernohl) information. These can be used in the schematic editor and PCB layout program [KiCad](http://www.kicad-pcb.org/).

<br/>

## Table of Contents

- [KiCad Things](#kicad-things)
  - [Table of Contents](#table-of-contents)
  - [1 - Tips & Tricks](#1---tips--tricks)
  - [2 - Keyboard shortcuts](#2---keyboard-shortcuts)
  - [3 - Board Setup](#3---board-setup)
  - [4 - PCB design](#4---pcb-design)
  - [5 - Gerber generation](#5---gerber-generation)
    - [5.1 - PCBWay (Quick-turn PCB as of 21/11/2019)](#51---pcbway-quick-turn-pcb-as-of-21112019)

<br/>

## 1 - Tips & Tricks

- **Watch out for top/bottom views on mechanical drawings!!**
- Ohm sign: **Ω**
- Select X7R capacitors if possible
- Use VDD instead of VCC
- **PLOT the schematic so the text becomes selectable!**
<!-- fix vertical spacing -->
- Draw the PCB in inches!
- Use **rounded PCB corners** with a diameter of **75 mils (0,0750 inch)**.
- Use `Lock Footprint` to make sure manually placed footprints stay on the PCB when the netlist is refreshed.
<!-- fix vertical spacing -->
- PCB thickness: 1,6 mm
- Copper weight: 35 µm (1 oz)

|            | Grid size |             |  Usage   |  Shortcut   |     |     |     | Standard board information                                          |
| :--------: | :-------: | :---------: | :------: | :---------: | --- | --- | --- | ------------------------------------------------------------------- |
| Schematic  |  50 mils  |             | Standard |             |     |     |     | `< project title >` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;`v1.0` |
| PCB layout |  25 mils  | (0,6350 mm) | Standard | `Alt` + `1` |     |     |     | `Licensed under CERN OHL v.1.2`                                     |
| PCB layout |  5 mils   | (0,2540 mm) |   Fine   | `Alt` + `2` |     |     |     | `github.brechtve.be` &nbsp; &nbsp; `01/2020`                        |

| Resistor package | Power dissipation | Usage                 |     | Diode package | Other name |  Size  |
| :--------------: | :---------------: | --------------------- | --- | :-----------: | :--------: | :----: |
|       0603       |  1/10 W = 100 mW  |                       |     |   DO-214AC    |    SMA     | Small  |
|       0805       |  1/8 W = 125 mW   | Hand soldering        |     |   DO-214AA    |    SMB     | Middle |
|       1206       |  1/4 W = 250 mW   | Power sensing (0,1 Ω) |     |   DO-214AB    |    SMC     | Large  |

<br/>

## 2 - Keyboard shortcuts

- Snap component/symbol to grid: `m` (move) & `ctrl + shift`
- Mouse left click = `RETURN`
- Mouse left double click = `END`

| Shortcut           | Function (PCB layout)            | Shortcut    | Function (PCB layout)              |
| ------------------ | -------------------------------- | ----------- | ---------------------------------- |
| `Alt + 3`          | 3D Viewer                        | `W`         | Switch Track Width to Next         |
| `Ctrl + U`         | Switch Units                     | `Shift + W` | Switch Track Width to Previous     |
| `B`                | Fill or Refill All Zones         | `Del`       | Delete Full Track                  |
| `Ctrl + B`         | Remove Filled Areas in All Zones | `Back`      | Delete Track Segment               |
| `O`                | Add Footprint                    | `G`         | Drag Item                          |
| `X`                | Add New Track                    | `C`         | Copy Item                          |
| `/`                | Switch Track Posture             | `M`         | Move Item                          |
| `D`                | Drag Track Keep Slope            | `T`         | Get and Move Footprint             |
| `V`                | Add Through Via                  | `F`         | Flip Item                          |
| `Ctrl + Shift + V` | Add Vias                         | `R`         | Rotate Item                        |
| `Ctrl + Shift + Z` | Add Filled Zone                  | `L`         | **Lock/Unlock Footprint**          |
| `Ctrl + Shift + K` | Add Keepout Area                 | `Ctrl + F`  | Find Item                          |
| `Ctrl + Shift + L` | Draw Line                        | `E`         | Edit Item                          |
| `Ctrl + Shift + C` | Draw Circle                      | `PgUp`      | Switch to Component (`F.Cu`) layer |
| `Ctrl + Shift + A` | Draw Arc                         | `PgDn`      | Switch to Copper (`B.Cu`) layer    |
| `Ctrl + Shift + P` | Draw Graphic Polygon             | `+`         | Switch to Next Layer               |
| `U`                | Select Single Track              | `-`         | **Switch to Previous Layer**       |
| `Ctrl + Shift + T` | Add Text                         | `N`         | Switch Grid to Next                |
| `Ctrl + Shift + H` | Add Dimension                    | `Shift + N` | Switch Grid to Previous            |
| `I`                | Select Connected Tracks          | `Ctrl + M`  | **Move Exactly**                   |

**TODO: Move the bulk of the shortcuts to another file and add schematic shortcuts?**

<br/>

## 3 - Board Setup

See [THIS](board-setup.md) file.

<br/>

## 4 - PCB design

| Commonly used symbol                                                 | Commonly used package                                                               | Dimensions                                             |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------ |
| `SparkFun-PowerSymbols: XXXX`                                        | VDD, GND, VDDA                                                                      |                                                        |
| `power: XXXX`                                                        | PWR_FLAG, GNDA, GNDPWR, +15V                                                        |                                                        |
|                                                                      |                                                                                     |                                                        |
| `Device: R/C/L_Small`                                                | `XXXX_SMD: X_0805_XXXX_HandSolder`                                                  | Pads: 1,15 mm x 1,40 mm                                |
|                                                                      |                                                                                     |                                                        |
| `Device: Jumper_XX_Small`                                            | `Connector_PinHeader_2.54mm: PinHeader_1x02_P2.54mm_Vertical`                       | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
| `Jumper: SolderJumper_3_Bridged12`                                   | `Jumper: SolderJumper-3_P1.3mm_Bridged12_Pad1.0x1.5mm_NumberLabels`                 |                                                        |
|                                                                      |                                                                                     |                                                        |
| `Connector: TestPoint`                                               | `TestPoint: TestPoint_THTPad_D2.0mm_Drill1.0mm`                                     | Drill: 1 mm - Pad: 2 mm                                |
| `Connector_Generic: Conn_XXxXX`                                      | `Connector_PinHeader_2.54mm: PinHeader_XXXX`                                        | Diameter hole: 1 mm - Pads: 1,7 mm x 1,7 mm            |
|                                                                      | `Connector_Phoenix_PTSA_extra: PhoenixContact_PTSA_1,5_2-G-3,5_1x02_P3.50mm_Angled` | 2 Contacts - Spacing pads: 3,5 mm - Diam. wire: 1,5 mm |
|                                                                      |                                                                                     |                                                        |
| `Mechanical: MountingHole`                                           | `MountingHole: MountingHole_3.2mm_M3`                                               | Diameter hole: 3,2 mm                                  |
| `Switch: SW_Push`                                                    | `Button_Switch_SMD: SW_SPST_FSMSM`                                                  | Pads: 2,18 mm x 1,60 mm - Distance between pads: 7 mm  |
|                                                                      |                                                                                     |                                                        |
| `BrechtVE_DebugHeader: DebugHeader_Cortex-M_SWD_UART_10p`            | `Connector_PinHeader_1.27mm: PinHeader_2x05_P1.27mm_Vertical_SMD`                   |                                                        |
| `BrechtVE_DebugHeader: DebugHeader_Cortex-M_SWD_UART_10p_TagConnect` | `Connector: Tag-Connect_TC2050-IDC-NL_2x05_P1.27mm_Vertical`                        |                                                        |
| `BrechtVE_DebugHeader: DebugHeader_UART_4p`                          | `Connector_PinHeader_2.54mm: PinHeader_1x04_P2.54mm_Vertical (_SMD)`                |                                                        |
|                                                                      |                                                                                     |                                                        |
| `BrechtVE_Aesthetics: Symbol_OSHW-Logo_11.4x12mm`                    | `BrechtVE_Aesthetics: OSHW-Logo_5.7x6mm_SolderMask`                                 |                                                        |
|                                                                      | `BrechtVE_Aesthetics: KiCad-Logo2_SilkScreenMaskTop_5mm`                            | Height:  5mm                                           |

| Connector    | Usage                                   | Commonly used package                                             |
| ------------ | --------------------------------------- | ----------------------------------------------------------------- |
| Molex KK 254 | Dupont but polarized                    | `Connector_Molex: Molex_KK-254_AE-6410-02A_1x02_P2.54mm_Vertical` |
| JST-XH       | Lithium batteries                       | `Connector_JST: JST_XH_B2B-XH-A_1x02_P2.50mm_Vertical`            |
| JST-PH       | Small LiPo packs (1+ 2-), STEMMA, Grove | `Connector_JST: JST_PH_B2B-PH-K_1x02_P2.00mm_Vertical`            |
| JST-SH       | STEMMA QT, Qwiic                        | `Connector_JST: JST_SH_SM02B-SRSS-TB_1x02-1MP_P1.00mm_Horizontal` |

| UART  | Color  |     | Cortex-M SWD       | Color  |
| :---: | :----: | --- | ------------------ | :----: |
|  RXD  | White  |     | 01. VTREF (3.3V)   |  Red   |
|  TXD  | Green  |     | 02. SWDIO          | Orange |
|  GND  | Black  |     | 03. GND            | Black  |
| 3.3V  |  Red   |     | 04. SWCLK          | Purple |
|       |        |     | 05. GND            |        |
|  DTR  |  Blue  |     | 06. SWO            |  Grey  |
|  RTS  | Purple |     | 07. (key) JL.RX    | White  |
|  CTS  |  Grey  |     | 08. (nc) JL.TX     | Green  |
|       |        |     | 09. (nc) GNDdetect |        |
|       |        |     | 10. nRESET         |  Blue  |

<br/>

## 5 - Gerber generation

### 5.1 - PCBWay (Quick-turn PCB as of 21/11/2019)

- Check the `Use Protel filename extensions` box
- Drill files:
  - Check the `suppress leading zeros` and `minimal header` boxes
  - Uncheck the `PTN and NPTH in single file` box 

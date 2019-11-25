
# 2 - Board Setup

[[BACK]](README.md)
<!-- [Back](https://img.shields.io/badge/BACK-<-lightgrey?url=README.md) -->

<br/>

## Table of Contents

- [2 - Board Setup](#2---board-setup)
  - [Table of Contents](#table-of-contents)
  - [2.1 - Layers](#21---layers)
    - [2.1.1 - Text & Graphics](#211---text--graphics)
  - [2.2 - Design Rules](#22---design-rules)
    - [2.2.1 - Net Classes](#221---net-classes)
    - [2.2.2 - Tracks & Vias](#222---tracks--vias)
    - [2.2.3 - Solder Mask/Paste](#223---solder-maskpaste)
  - [2.3 - Fill settings](#23---fill-settings)
  - [2.4 - Design rules for board houses](#24---design-rules-for-board-houses)
    - [2.4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)](#241---pcbway-quick-turn-pcb-as-of-21112019)

<br/>

## 2.1 - Layers

### 2.1.1 - Text & Graphics

The **default settings** for text and graphics using the *metric* system are fine:

|                   | Line Thickness | (mils)     | Text Width | (mils)     | Text Height | Text Thickness | (mils)     |
| ----------------- | -------------- | ---------- | ---------- | ---------- | ----------- | -------------- | ---------- |
| **Silk Layers**   | 0,12 mm        | (4,724409) | 1,0 mm     | (39,37008) | 1,0 mm      | 0,15 mm        | (5,905512) |
| **Copper Layers** | 0,20 mm        | (7,874016) | 1,5 mm     | (59,05512) | 1,5 mm      | 0,30 mm        | (11,81102) |
| **Edge Cuts**     | 0,05 mm        | (1,968504) |            |            |             |                |
| **Courtyards**    | 0,05 mm        | (1,968504) |            |            |             |                |
| **Other Layers**  | 0,15 mm        | (5,905512) | 1,0 mm     | (39,37008) | 1,0 mm      | 0,15 mm        | (5,905512) |

<br/>

## 2.2 - Design Rules

### 2.2.1 - Net Classes

Here we `change` the values regarding **TRACKS** to values using the *imperial* system.

| Clearance  | Track Width | Via Size        | Via Drill       | uVia Size       | uVia Drill      | dPair Width | dPair Gap  |
| ---------- | ----------- | --------------- | --------------- | --------------- | --------------- | ----------- | ---------- |
| `10 mils`  | `10 mils`   | 0,8 mm          | 0,4 mm          | 0,3 mm          | 0,1 mm          | `10 mils`   | `10 mils`  |
| (0,254 mm) | (0,254 mm)  | (31,49606 mils) | (15,74803 mils) | (11,81102 mils) | (3,937008 mils) | (0,254 mm)  | (0,254 mm) |

<br/>

### 2.2.2 - Tracks & Vias

Here we add all new values for the **TRACKS** using the *imperial* system.

| Width     |            | Current (^10 °C / A) |
| --------- | ---------- | -------------------- |
| `10 mils` | (0,254 mm) | 0,9 A (35 µm)        |
| `15 mils` | (0,381 mm) |                      |
| `20 mils` | (0,508 mm) | 1,4 A (35 µm)        |
| `25 mils` | (0,635 mm) |                      |
| `30 mils` | (0,762 mm) | 1,9 A (35 µm)        |
| `40 mils` | (1,016 mm) | 2,4 A (35 µm)        |

<br/>

For the **VIAS** we use the following values while keep using the *metric* system.

| Size     |                 | Drill    |                 | Current (^10 °C / A) |
| -------- | --------------- | -------- | --------------- | -------------------- |
| `0,8 mm` | (31,49606 mils) | `0,4 mm` | (15,74803 mils) | 1,6 A                |
| `1,4 mm` | (55,11811 mils) | `0,7 mm` | (27,55906 mils) | 2,4 A                |
| `2,0 mm` | (78,74016 mils) | `1,0 mm` | (39,37008 mils) | 3,1 A                |

<br/>

### 2.2.3 - Solder Mask/Paste

Here we also switch to slightly other values using the *imperial* system.

|                                  | Size      |             |
| -------------------------------- | --------- | ----------- |
| **Solder mask clearance**        | `2 mils`  | (0,0508 mm) |
| **Solder mask minimum width**    | `10 mils` | (0,254 mm)  |
|                                  |           |             |
| **Solder paste clearance**       | -0 mils   |             |
| **Solder paste ratio clearance** | -0,00 %   |             |

<br/>

## 2.3 - Fill settings

|                     | Size    | (default sizes are fine) |
| ------------------- | ------- | ------------------------ |
| Clearance           | 20 mils | (0,508 mm)               |
| Minimum width       | 10 mils | (0,254 mm)               |
| Thermal clearance   | 20 mils | (0,508 mm)               |
| Thermal spoke width | 20 mils | (0,508 mm)               |

<br/>

## 2.4 - Design rules for board houses

### 2.4.1 - PCBWay (Quick-turn PCB as of 21/11/2019)

**DRC settings**

- Minimum track width: `6 mils`
- Minimum track gap: `6 mils`
- Minimum via drill: `0,3 mm` (`11,81102 mils`)

<br/>

**Text (silkscreen) settings**

- Positive:
  - Minimum character line width: `0,15 mm`
  - Minimum character height: `0,8 mm`
  - (A ratio of `1:5` is recommended)
- Inverted:
  - Minimum character line width: `0,25 mm`
  - Minimum character height: `1,25 mm`

<br/>

[[BACK]](README.md)

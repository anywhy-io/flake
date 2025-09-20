**English** | [简体中文](./internationalization/Chinese/build_guide.md) | [Русский](./internationalization/Russian/build_guide.md)

# Flake Keyboard Build Guide

Welcome to the official build guide for the Flake keyboard! This guide is designed to be comprehensive and easy to follow, even if this is your first time building a keyboard.

I recommend reading through the entire guide once before you begin to familiarize yourself with the process.

## Prerequisites

Before you start soldering or assembling, make sure you have all the necessary components and tools.

### Required Tools
*   **Soldering Iron:** A quality soldering iron with adjustable temperature control is essential.
*   **Solder:** Lead-free solder is strongly recommended for health and safety.
*   **Flux:** A flux pen or paste will make soldering significantly easier.
*   **Tweezers:** Essential for handling small components.
*   **Screwdriver:** For the M2 screws used in the case.
*   **(Optional) Multimeter:** Useful for troubleshooting.

### Required Files
You will need the manufacturing files for the PCB and the enclosure. You can find all the necessary files and instructions on where to order them here:
➡️ **[Essential Files and Ordering Guide](essential_files.md)**

### Bill of Materials (BOM)

The required components vary based on the size of the keyboard you are building. The number of keys for each size is:
*   **Small:** 40 keys
*   **Medium:** 46 keys
*   **Large:** 58 keys

| Component | Small (40) | Medium (46) | Large (58) | Notes |
|:---|:---:|:---:|:---:|:---|
| **Soldering Components** | | | | |
| Anywhy Flake v2 PCB | 2 | 2 | 2 | One for each half |
| Seeed Xiao nRF52840 | 2 | 2 | 2 | The microcontroller |
| JST 1.25 SMD 2pin Connector | 2 | 2 | 2 | For the battery |
| MX Hot-swap Sockets | 40 | 46 | 58 | See note below |
| Choc Hot-swap Sockets | 40 | 46 | 58 | See note below |
| 1N4148 Diodes | 40 | 46 | 58 | 1 per switch (SOD-123 or SOD-323) |
| **Assembly Components** | | | | |
| Soldered PCB | 2 | 2 | 2 | From the step above |
| Switches (Choc v1/v2 or MX) | 40 | 46 | 58 | 1 per socket |
| Keycaps | 40 | 46 | 58 | Must be compatible with your switches |
| Enclosure | 1 set | 1 set | 1 set | Includes top and bottom parts for each half |
| 502030 LiPo Battery | 2 | 2 | 2 | Or smaller, with a JST 1.25 plug |
| 6x2mm Rubber Feet | 8 | 8 | 8 | |
| M2x4mm Stand-offs | 6 | 8 | 8 | |
| M2x8mm Flat Countersunk Screws | 12 | 16 | 16 | e.g., DIN965 |

> [!NOTE]
> **Sockets:** The Flake PCB supports both MX and Choc switches simultaneously. This guide shows you how to solder both socket types for maximum flexibility. If you are certain you will only ever use one type of switch, you can choose to solder only the corresponding sockets (MX or Choc) and omit the other set.

---

## 1. Soldering the PCB

This is the most detailed part of the build. Take your time, work in a well-ventilated area, and double-check your work as you go.

### Preparation

#### A. Understand the Reversible PCB

The Flake uses a **reversible PCB**. This means you use the same PCB design for both the left and right halves - you just flip one over. The assembly process is identical for both halves. This guide will walk you through building one half. **Simply repeat all steps on the second PCB, ensuring it is flipped to the opposite side.**

<img alt="Two reversible Flake PCBs" width="100%" src="./img/build_guide/pcb.webp">

#### B. Clean the Holes Under the Controller
Due to the manufacturing process, the controller pin holes may be partially obstructed. Before placing the controller, you must carefully clear these obstructions using a tip of your tweezers.

<img alt="Before and after cleaning the controller pin holes" width="100%" src="./img/build_guide/rings.webp">

#### C. Break the PCB (Small Version Only)
If you are building the 40-key **Small** version, as I do in this guide, you must snap off the outer pinky column from both PCBs. **If you are building the Medium or Large version, skip this step and leave the PCBs intact.**

<img alt="Breaking off the outer column for the Small version" width="100%" src="./img/build_guide/column.webp">

#### D. Prepare Your Components
Lay out the PCB and the components you will be soldering for one half.

<img alt="All components for soldering one PCB half" width="100%" src="./img/build_guide/electronics.webp">

### Step 1: Battery Connector (JST)

> [!TIP]
> If your battery doesn't have a JST plug, you can solder it directly to the `RAW` (+) and `GND` (-) pads next to the JST footprint. However, this is not recommended as it makes the battery difficult to replace later.

1. Place the JST 1.25 connector onto its footprint at position `BT1`.
2. Solder the two large mounting pads to secure connector.
3. Solder the two small pins.

<img alt="Soldering the JST battery connector" width="100%" src="./img/build_guide/jst.webp">

### Step 2: Controller (Seeed Xiao)

> [!IMPORTANT]
> Proper alignment is critical. A misaligned controller may prevent the keyboard from fitting into the enclosure.

1.  Place the Xiao controller onto its footprint inside the `U1` outline. The USB-C port should face outwards.
2.  Solder **one corner pin** to tack the controller in place.
3.  Check the alignment. If it's crooked, re-heat the pin and adjust.
4.  Once aligned, solder the **diagonally opposite corner pin** to lock it in place.

<img alt="Tacking opposite corner pins of the controller first" width="100%" src="./img/build_guide/opposite.webp">

5.  Proceed to solder all remaining pins.

<img alt="All controller pins soldered" width="100%" src="./img/build_guide/controller.webp">

6.  Flip the PCB and solder the `RAW` and `GND` pads under the controller.

<img alt="Soldering the RAW and GND pads under the controller" width="100%" src="./img/build_guide/power.webp">

### Step 3: Diodes

> [!WARNING]
> Diodes are directional! The line on the diode must match the line on the PCB silkscreen. An incorrectly oriented diode will cause that key to fail.

For each switch position:
1.  Add a small amount of solder to one of the two diode pads.
2.  Using tweezers, slide a diode into place, re-heating the solder blob to secure one side. **Ensure the line on the diode aligns with the line on the PCB outline.**
3.  Solder the other leg of the diode.

<img alt="Three-step process for soldering a diode" width="100%" src="./img/build_guide/diode.webp">

### Step 4: Hot-swap Sockets

For each switch position:
1.  Place the **MX socket** in the top position and the **Choc socket** in the bottom position.
2.  Solder both metal legs on each socket.

<img alt="Soldering MX and Choc hot-swap sockets" width="100%" src="./img/build_guide/sockets.webp">

### Soldering Complete!
Congratulations! You have a fully soldered PCB. Take a moment to inspect all your solder joints.

<img alt="Completed PCB with all components soldered" width="100%" src="./img/build_guide/soldered.webp">

Now, repeat the entire soldering process for the second PCB. Remember to work on the **opposite side** of the PCB so it becomes a **mirror image** of the first half.

## 2. Case Assembly

With both PCBs soldered, it's time to put everything into the enclosure.

1.  Gather the soldered PCB, case parts, battery, standoffs, and screws.

<img alt="All components for final assembly" width="100%" src="./img/build_guide/hardware.webp">

2.  Screw the M2x4mm standoffs into the **bottom half** of the case.

<img alt="Standoffs installed in the bottom plate" width="100%" src="./img/build_guide/standoff.webp">

3.  Seat the soldered PCB into the **top half** of the case. Connect the battery's JST plug and place the battery into its dedicated cutout.

> [!WARNING]
> **Battery Safety:** Triple-check the polarity before connecting battery. Connecting the battery backwards (red wire to `GND (-)`, black wire to `RAW (+)`) will destroy the microcontroller.

<img alt="PCB and battery placed in the top case" width="100%" src="./img/build_guide/inside.webp">

4.  Carefully place the bottom plate onto the top part, aligning the standoff holes. Stick the self-adhesive rubber feet onto the dedicated spots on the bottom of the case.

> [!TIP]
> For the second half, place the feet on the opposite corners. This allows the two halves to sit flush against each other back-to-back for transport.

<img alt="Assembled case from the bottom with rubber feet" width="100%" src="./img/build_guide/feets.webp">

5. Insert the M2x8mm screws from the top and tighten them. Do not overtighten.

<img alt="Screws installed from the top to secure the case" width="100%" src="./img/build_guide/assembled.webp">

**Repeat** this assembly process for the second half of the keyboard.

## 3. Final Assembly

> [!IMPORTANT]
> If you are using MX switches, you must place the included MX plate onto the keyboard *before* inserting the switches.

1.  **Insert Switches:** Gently press your chosen switches (MX or Choc) into the corresponding hot-swap sockets. Ensure the switch pins are straight to avoid bending them.

<img alt="Inserting either MX or Choc switches" width="100%" src="./img/build_guide/switches.webp">

2.  **Install Keycaps:** Press your keycaps firmly onto the switch stems.

<img alt="Fully assembled Flake keyboard" width="100%" src="./img/build_guide/done.webp">


## You're Done!
Congratulations on building your Flake keyboard! Your keyboard is now physically complete.

The final step is to flash the firmware to make it fully functional. Please proceed to the next guide:
➡️ **[Flashing Guide](flashing_guide.md)**
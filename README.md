# ATtiny3217-MNR Development Board (Schematic Reference)

> **⚠️ STATUS: SCHEMATIC ONLY / NO PCB ROUTING**
>
> This repository contains the **logical schematic design** for a compact ATtiny3217-MNR development board.
> **There is currently no PCB layout or routing included.** This project is released to validate the pinout, peripheral configuration, and USB-to-SerialUPDI implementation before proceeding to the physical design phase.

## Project Overview

This dev board is designed to maximize the utility of the Microchip ATtiny3217 in a minimal footprint while providing robust debugging capabilities. It features a built-in USB-to-UART bridge with specific CBUS configurations for visual feedback during programming and communication.

**Key Features:**

- **MCU:** Microchip ATtiny3217-MNR (WQFN-24)
- **Programmer/Debug:** Built-in USB-to-SerialUPDI via **FT231XS-U**
- No external programmer needed; program directly via USB-C/Micro (connector footprint pending).

- **Visual Debugging LEDs:**
- **PWR:** Power indicator.
- **TX Blink:** Connected to FT231X **CBUS2** (Active during transmission/flashing).
- **RX Blink:** Connected to FT231X **CBUS1** (Active during reception).
- **User LED:** Connected to a configurable GPIO (Default: PB0/PC0 - *final assignment TBD in routing phase*).

- **Connectivity:** All MCU GPIO pins broken out to standard 2.54mm headers.
- **Power:** 3.3V LDO regulation (Footprint included).

## Current State & Missing Components

As of this release, the project is **Logic Complete** but **Physically Incomplete**.

| Component | Status | Notes |
| :--- | :--- | :--- |
| **Schematic** | ✅ Complete | Pin assignments, pull-ups, and USB interface are finalized. |
| **PCB Routing** | ❌ Not Started | **Help Wanted!** Need suggestions for stackup and impedance control for USB lines. |
| **Footprints** | ⚠️ Partial | Most passive components are 0402. USB connector footprint needs final selection. |
| **Firmware** | ❌ None | This is hardware-only. Example code for SerialUPDI will be added later. |

## Why Release Now?

I am releasing the schematic early to gather feedback on:

1. **Pin Mapping:** Are the chosen default pins for the User LED and headers optimal for common libraries (e.g., `megaTinyCore`)?
2. **USB Layout:** Best practices for routing the FT231XS-U differential pairs in a small form factor.
3. **Form Factor:** Suggestions for board shape to fit into standard breadboards or wearable constraints.

## How to Contribute

We are specifically looking for help with:

- **PCB Layout:** Creating the initial routing in KiCad or EasyEDA.
- **Footprint Verification:** Double-checking the WQFN-24 thermal pad and USB connector dimensions.
- **Documentation:** Adding pinout diagrams and usage examples once the board is routed.

Please read the [CONTRIBUTING.md](CONTRIBUTING.md) guidelines before submitting issues or pull requests. Note that by contributing, you agree to the [CLA.md](CLA.md), allowing ElectroSpark to maintain flexibility in future proprietary iterations of this hardware.

## Tools Used

- **Design Software:** EasyEDA (Schematic)
- **Target Architecture:** AVR Dx Core (ATtiny3217)
- **License:** AGPL-3.0 (See GitHub License Selector)

---
*Designed by Shihan @ ElectroSpark*
*Date: 2025-10-07*

# Contributing to ATtiny3217-MNR Dev Board

Thank you for your interest in helping bring this development board to life! Since this project is currently **schematic-only**, your contributions are vital to moving us toward a manufacturable PCB.

## 🚀 Where We Need Help

### 1. PCB Routing (High Priority)

The biggest gap right now is the physical layout. If you have experience with:

- **USB Differential Pairs:** Routing the FT231XS-U D+/D- lines with proper impedance (90Ω differential).
- **Thermal Management:** Designing the thermal via array for the ATtiny3217-MNR WQFN package.
- **Compact Layout:** Fitting the board into a small form factor while keeping headers accessible.

Please fork the repo, create a `pcb-layout` branch, and submit your design files (KiCad preferred, EasyEDA accepted).

### 2. Schematic Review

Double-check the logical connections:

- Are the CBUS configurations on the FT231XS-U correct for TX/RX blinking?
- Are the pull-up/down resistors on the UPDI line appropriate?
- Is the power rail decoupling sufficient for the selected LDO?

### 3. Documentation

- Create a pinout diagram based on the schematic.
- Draft a basic "Getting Started" guide for using SerialUPDI with this board.

## Code of Conduct

- **Be Constructive:** Critique the design, not the designer. This is a learning project.
- **Respect the Vision:** The goal is a minimal, hacker-friendly dev board. Avoid feature creep (e.g., adding Bluetooth or SD cards) unless discussed in an issue first.
- **Collaborate:** Use GitHub Issues to discuss major changes before opening a Pull Request.

## Submission Guidelines

- **Check Issues:** See if someone is already working on the PCB layout.
- **Branching:** Create a branch named `feature/your-name-pcb-v1` or `fix/schematic-review`.
- **File Formats:** Prefer open formats (e.g., KiCad `.kicad_pcb`) alongside native EasyEDA files if applicable.
- **Commit Messages:** Be descriptive. Example: "Add thermal vias under ATtiny3217 EP pad."

## Licensing & CLA

By contributing to this repository, you agree to the terms of our **Contributor License Agreement (CLA)**. This ensures that while this version remains open source (AGPL), ElectroSpark retains the right to relicense future hardened versions or commercial derivatives if necessary.

## Questions?

Open an issue with the label `question` or `design-discussion`. Let's build a great tinyDev board together!

# USB-C High-Speed Interface & Power Management PCB

A USB-C interface PCB designed using **KiCad 9.0**, focusing on USB 2.0 connectivity, ESD protection, power regulation, and practical PCB design workflows.

## Project Overview

This project focuses on designing a USB Type-C interface board that provides USB 2.0 data connectivity and a regulated power supply for a USB-to-UART interface.

The design combines USB-C connector interfacing, USB data-line protection, power management, and PCB layout considerations in a structured hardware design project.

**Project status:** PCB design uploaded to GitHub for educational and portfolio purposes. Physical fabrication and hardware testing have not been performed.

## Objectives

* Design a USB Type-C receptacle interface for USB 2.0 data communication.
* Incorporate ESD protection for USB data lines.
* Implement USB-C CC1/CC2 configuration using appropriate pull-down resistors.
* Design a protected 5 V power input and 3.3 V regulation stage.
* Develop a schematic and PCB layout using KiCad.
* Practice PCB design-rule checking, electrical-rule checking, and hardware documentation.

## Key Features

* USB Type-C connector interface
* USB 2.0 D+ and D− signal routing
* USBLC6-2SC6 ESD protection
* CH340C USB-to-UART interface
* AP2112K-3.3 voltage regulator
* Protected VBUS power input
* CC1/CC2 pull-down configuration
* UART TX/RX header interface
* PCB layout and design validation using KiCad

## Tools Used

| Tool      | Purpose                                 |
| --------- | --------------------------------------- |
| KiCad 9.0 | Schematic capture and PCB layout        |
| LTspice   | Optional future circuit simulation      |
| Python    | Optional future analysis and automation |

## Hardware Design

### 1. USB Type-C Interface

The USB-C receptacle provides the physical connection for USB communication and power input. The CC1 and CC2 pins use configuration pull-down resistors intended for a USB device/sink interface.

### 2. USB Data-Line Protection

The USBLC6-2SC6 is included to provide electrostatic discharge protection for the USB data lines.

### 3. USB-to-UART Conversion

The CH340C provides a USB-to-UART bridge, allowing USB communication to be converted into serial TX/RX signals.

### 4. Power Management

The design includes a protected VBUS power path and an AP2112K-3.3 regulator intended to provide a 3.3 V supply.

The final power performance depends on component selection, circuit implementation, loading, and validation.

### 5. PCB Layout

The PCB is designed in KiCad with attention to component placement, ground return paths, routing, clearances, and USB differential-pair layout considerations.

A four-layer stackup and controlled-impedance routing are design goals that require appropriate stackup specifications and impedance verification before fabrication.

## Project Structure

```text
USB-C-High-Speed-Interface-PCB/
├── 01_Design and manufacturing/
├── 06_Documention
├── 07_Images/
├── README.md
├── USB_C_Interface.kicad_pro
├── USB_C_Interface.kicad_sch
└── USB_C_Interface.kicad_pcb
```

The folder contents may be expanded as supporting documentation, calculations, and design images are added.

## Design Validation

The design has been checked using KiCad's Electrical Rules Checker (ERC) and Design Rules Checker (DRC).

* **ERC errors:** 0 reported
* **DRC errors:** 0 reported
* **Unconnected items:** 0 reported

These results reflect the checks performed on the current design at the time of validation. They do not independently establish electrical performance, USB signal integrity, controlled impedance, or physical hardware functionality.

## Limitations

* USB signal integrity and differential impedance have not been established through physical measurements.
* Power regulation performance has not been validated under real load conditions.
* Connector footprint dimensions and fabrication requirements should be rechecked against the selected manufacturer's documentation before manufacturing.

## Future Improvements

* Verify all footprints and pin mappings against manufacturer datasheets.
* Document the intended PCB stackup and obtain impedance calculations from suitable tools or the fabricator.
* Perform appropriate circuit simulations and document genuine results.
* Review USB routing and return paths for signal integrity.
* Generate and review Gerber, drill, and bill-of-materials outputs.
* Fabricate a prototype and perform electrical and functional tests.

## Learning Outcomes

This project provides practical experience in:

* Electronic schematic design
* USB Type-C interface fundamentals
* USB 2.0 data-line protection
* Power regulation and decoupling
* PCB layout and routing
* KiCad ERC/DRC workflows
* Engineering documentation and version control using GitHub

## Disclaimer

This is an educational PCB design project. All validation statements refer only to the design checks explicitly performed. No claim of USB certification, measured signal integrity, manufacturing readiness, or hardware functionality is made.


# Embedded System Vault Design — MSP430

Conceptual embedded system architecture for a secure vault using **RFID authentication**, **LCD user feedback**, and **PWM servo actuation** on an MSP430 microcontroller platform.

<img src="media/embedded_system_block_diagram.png" width="550"/>

## Project Summary
This project presents the design of an access-control embedded system built around the MSP430FR5994. The system integrates multiple communication protocols and peripherals to authenticate a user, provide LCD feedback, and actuate a servo-based lock mechanism.

## System Architecture

| Subsystem | Component | Interface | Purpose |
|---|---|---|---|
| Authentication | RFID-RC522 | SPI | Reads and validates RFID tags |
| User Interface | LCD display | I2C | Displays access status and user feedback |
| Actuation | Servo motor | PWM | Controls lock/unlock mechanism |
| Controller | MSP430FR5994 | GPIO/peripherals | Coordinates system logic |

## System Behavior
1. System waits for RFID tag input.
2. RFID module sends tag data to the MSP430 over SPI.
3. Control logic compares the tag against authorized credentials.
4. LCD displays access granted or denied.
5. Servo actuates the locking mechanism only when access is approved.

## Architecture Highlights
- SPI communication for RFID authentication
- I2C communication for LCD status feedback
- PWM servo control for lock actuation
- Modular embedded control logic
- Clear separation between input, processing, feedback, and actuation

## My Contributions
- Designed the embedded system architecture and component integration plan.
- Defined communication interfaces across RFID, LCD, and servo subsystems.
- Developed control-flow logic for authentication and actuation behavior.
- Created system-level block diagram and technical documentation.

## Project Type
This repository documents a **conceptual embedded system design**. The focus is system architecture, peripheral integration, interface planning, and control logic rather than a fully built hardware implementation.

## Repository Structure
```text
docs/    embedded system report
media/   system block diagram
```

## Documentation
- [Full Report](docs/embedded-system-report.pdf)

## Future Improvements
- Add MSP430 firmware implementation.
- Add pin mapping table and wiring diagram.
- Add test plan for RFID validation, LCD output, and servo response.
- Build a prototype enclosure and demonstrate the full access-control sequence.

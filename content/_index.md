---
title: "Home"
---

> [!ABSTRACT] *An open-source modding platform for espresso machines*
> Openpresso is a community-driven open platform for espresso machine modification and experimentation. It provides a flexible foundation that can be adapted, extended, and built upon to transform an entry-level espresso machine and a handful of affordable hardware modules into a feature-rich brewing platform. The project embraces transparency, modularity, and knowledge sharing, enabling ideas, improvements, and innovations to be shared and refined by the entire community.

---

> [!DANGER]
> Espresso machine works with **mains electricity**, hot surfaces, **pressurized steam and water**. Incorrect assembly, wiring, firmware changes, or operation can cause electric shock, burns, fire, equipment damage, serious injury, or **death**. Use only if you are qualified to work safely on mains-powered, heated, pressurized equipment. Provided **as is**, without any warranty; you assume all risks and all responsibility for compliance, testing, installation, and use.

## Features

Openpresso transforms a traditional espresso machine into a programmable brewing platform.

### Measure

Monitor extraction with real time graphs using digital:

- Temperature sensing
- Pressure sensing
- Weight measurement
- Flow-rate calculation

### Control

Openpresso actively controls machines heating elements, pumps and valves.

Features include:

- PID temperature control with cold water feed-forward compensation
- Pressure profiling
- Flow profiling
- Extended steaming with automatic boiler refill

### Program

Create multiple reusable multi-step brew profiles that define:

- Pressure or flow step target
- Time or weight step change condition
- Time or weight brew stop condition

### Analyze

Openpresso stores extraction history together with measured metrics, making it possible to compare results, refine recipes, and reproduce successful shots.

### Integrate

All functionality is exposed through REST API and a lightweight web interface that can run on a touchscreen attached directly to the machine or be accessed from any device on the local network. Some actions can also be invoked from the terminal using a simple CLI tool.

### Preserve the Original Experience

For users who prefer a stock appearance, Openpresso allows to build a "sleeper" that uses the machine's original buttons and indicator lamps while advanced control logic operates in the background.

---

## Why Openpresso?

Many espresso machine modification projects are built around microcontrollers and tightly coupled firmware. While this approach works well for dedicated appliances, it can make customization, experimentation, and extension difficult.

Openpresso takes a different path.

Instead of using a microcontroller as the central controller, Openpresso uses a Linux-based Single Board Computer (SBC) as the system's brain. This architectural decision was made to maximize:

- **Modularity** — independent components can be developed, replaced, or extended without redesigning the entire system.
- **Customizability** — developers can create their own services, user interfaces, automation workflows and integrations.
- **Accessibility** — the project relies on widely available hardware and well-known open-source technologies.
- **Developer friendliness** — contributors can use familiar programming languages, frameworks, and Linux tooling instead of specialized embedded development environments.

By building on Linux, Openpresso can leverage existing drivers and subsystems for:

- GPIO
- I²C
- SPI
- UART
- Networking
- USB devices
- HDMI displays
- Touchscreen interfaces

This allows the project to use commodity hardware such as Raspberry Pi boards and standard HDMI touchscreens rather than custom display firmware and specialized embedded hardware.

---

## Design Principles

Openpresso is built around a few core principles:

### Open Source First

All software components are developed and published under open-source licenses. The project aims to foster a community-driven ecosystem where users can share modifications and improvements.

### Hardware Accessibility

The project prioritizes commonly available components that can be purchased from multiple vendors worldwide.

### Machine Agnostic Foundation

The core architecture is intended to support multiple machine designs and hardware configurations rather than targeting a single espresso machine forever.

### Service-Oriented Architecture

Instead of a monolithic firmware image, Openpresso is composed of independent services and applications that communicate through well-defined interfaces.

### Extensibility

Adding new sensors, controllers, machine types, user interfaces and automation features should be possible without redesigning the entire platform.

---

## Current State

> [!IMPORTANT] Openpresso is currently under active development.

Current state can be observed on the [roadmap](/roadmap/) page.

The primary development and testing platform is built with:

- Raspberry Pi Zero 2W
- Gaggia Classic Pro
- Analog pressure transducer and ADS1115 DAC
- K-Type thermocouple and MAX31856 module
- Parallel connected two strain gauge load cells under a drip tray and NAU7802 module
- 3-ch AC-dimmer that controls pump, valve and heater
- Original power, brew and steam buttons connected to the SBC GPIO pins
- Indication LEDs mounted in place of original power, brew and steam neon lamps and connected to the SBC GPIO pins

While the architecture is designed to support other hardware in the future, most real-world testing currently happens on this combination.

## Project Architecture

Openpresso is composed of several independent projects that together form the complete platform.
Visit [subprojects](/subprojects/) page with compelete listing of the components and an architecture diagram.

## Join the Journey

The project is developed by a single contributor, but its long-term success depends on community involvement.
Openpresso wants be a foundation that others can adapt to their own machines, workflows, and use as an open platform for experimentation, learning, and innovation in the espresso community.
Users are encouraged to contribute improvements, share public forks, and build new modules on top of the platform.

---

## Credits

[![Cloudsmith](https://img.shields.io/badge/OSS%20hosting%20by-cloudsmith-blue?logo=cloudsmith&link=https%3A%2F%2Fcloudsmith.com)](https://cloudsmith.com)
_Package repository hosting is graciously provided by [Cloudsmith](https://cloudsmith.com).
Cloudsmith is the only fully hosted, cloud-native, universal package management solution, that
enables your organization to create, store and share packages in any format, to any place, with total
confidence._

### Logo design

by **Kymlach Anzhela**

_I'm deeply grateful to Anzhela for designing Openpresso logo. Thank you for your amazing work and for contributing your creative talent to this project!_

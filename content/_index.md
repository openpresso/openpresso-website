---
title: "Home"
---

<div class="hero-container">
    <div class="home-logo">
        <img class="logo-light" src="/logo.svg" alt="Openpresso Logo">
    </div>
    <div class="hero-text">
        <h1 class="hero-title accent">Openpresso</h1>
        <p class="hero-subtitle">An open-source modding kit for espresso machines.</p>
    </div>
</div>

> [!CAUTION] Safety Caution
> Espresso machines operate with **high voltages** and water under **high temperature and pressure**, which is **extremely dangerous**.
> Any modifications should only be performed if you fully understand what you are doing and assume all risks.
> Openpresso developers provide **no warranty** and are not responsible for any injuries or damages.

## Philosophy & Goals

The main goal of the Openpresso project is to provide a flexible, accessible, and highly customizable platform that allows coffee enthusiasts to transform and extend their machines using modern hardware and software.

The project is developed by a single contributor, but its long-term success depends on community involvement. Openpresso is designed to be a foundation that others can adapt to their own machines, workflows, and brewing philosophies. Users are encouraged to contribute improvements, share public forks, and build new modules on top of the platform.

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

The primary development and testing platform consists of:

- Raspberry Pi Zero 2W
- Gaggia Classic Pro

While the architecture is designed to support other hardware in the future, most real-world testing currently happens on this combination.

## Project Architecture

Openpresso is composed of several independent projects that together form the complete platform.
Visit [subprojects](/subprojects/) page with compelete listing of the components and an architecture diagram.

## Join the Journey

Openpresso aims to become an open platform for experimentation, learning, and innovation in the espresso community. Contributions, feedback and forks are welcome.

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

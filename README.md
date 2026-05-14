# OMS Starter Kit - Critical Abstraction Layer (SK-CAL)

These CAL files were released in conjunction with and implement message definitions for [Ghost Detector](https://gitlab.com/open-arsenal/oms/ghost-detector).

The Open Mission Systems (OMS) standard is a government-owned, non-proprietary open architecture specification designed to integrate modular components—called Units of Replaceability (UoRs)—into mission packages. 

Within this ecosystem, the **Critical Abstraction Layer (CAL)** serves as the standard Application Programming Interface (API) that abstracts the underlying messaging technology stack (the Abstract Service Bus, or ASB). This repository contains the Starter Kit implementation of the CAL (SK-CAL), providing the necessary libraries and commonality to connect your Subsystems and Services.

> [!NOTE]
> **OMS Standard Version:** This architecture and implementation align with OMS Version 2.5 (released January 22, 2026), governed by the Open Architecture Collaborative Working Group (OACWG).

## 🚀 Architecture Overview

At its core, OMS promotes interoperability by emphasizing loose coupling and a publish/subscribe messaging paradigm. The CAL is the critical bridge that allows disparate components to communicate seamlessly without being hardcoded to a specific network protocol or message broker.

### Key OMS Architecture Elements:

*   **Mission Package:** The top-level composition of Platforms, Subsystems, Services, and Isolators.
*   **Platform:** The infrastructure (hardware and software) that provides the ASB, the **CAL**, data storage, and the Open Computing Environment (OCE).
*   **Subsystem:** Payloads and sensors with dedicated hardware/software (e.g., RADAR, EO/IR, ESM).
*   **Service:** Software-only capabilities (e.g., auto-router, tracker, fusion engine).
*   **Isolator:** The security and isolation layer between the Mission Package and external systems.

## 🔌 The CAL Implementation

A provider of an OMS Platform is responsible for delivering a CAL Implementation. By programming against the CAL API, developers ensure their UoRs remain decoupled from the specific implementation of the ASB. 

The Starter Kit provides CAL implementations to support different environments:

*   **Language-Specific CALs:** APIs tailored for specific programming languages (like **Java** and **C++**) that meet the required attributes and behaviors of the standard.
*   **Language-Agnostic (LA) CAL:** A CAL Server implementation with a well-defined API that provides commonality across disparate systems. 

The CAL makes no restriction on the underlying tools, libraries, or products (e.g., ActiveMQ) that may be used to meet the messaging requirements, so long as the CAL API contract is fully implemented.

## 📊 Why Use the OMS CAL?

*   **Reduced Costs and Schedule:** The modular design enables rapid integration and lowers acquisition and sustainment expenses through reusable components.
*   **Enhanced Interoperability:** Standardized interfaces allow "plug-and-play" capabilities across platforms, supporting machine-to-machine data exchanges for battlespace superiority.
*   **Tiered Compliance:** Allows gradual adoption. Tier 1 permits legacy adoption of key portions of OMS, up to Tier 3 for full interoperability and maximum benefit.
*   **Fosters Competition:** The non-proprietary nature empowers providers to deliver innovative, future-proof solutions.

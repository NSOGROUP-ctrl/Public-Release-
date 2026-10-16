
# Pegasus Architecture & Mobile Endpoint Research Archive: WhatsApp v. NSO Group Documentation

<p align="center">
  <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?auto=format&fit=crop&w=1200&q=80" alt="Mobile Security Architecture and Data Analysis Dashboard" width="100%">
</p>

> **Abstract:** An open-source research compilation examining technical architectures, zero-click installation vectors, system requirements, and internal documentation concerning mobile endpoint monitoring software. Derived entirely from public court records and unsealed discovery exhibits from **_WhatsApp Inc. and Meta Platforms, Inc. v. NSO Group Technologies Limited_** (Case No. 4:19-cv-07123-PJH, U.S. District Court for the Northern District of California).

---

## 📌 Table of Contents
1. [Overview & Legal Context](#-overview--legal-context)
2. [Zero-Click Architecture: Heaven, Eden, and Erised](#-zero-click-architecture-heaven-eden-and-erised)
3. [Product Capabilities & Endpoint Modules](#-product-capabilities--endpoint-modules)
4. [Operational Security (OpSec) & Rule Engines](#-operational-security-opsec--rule-engines)
5. [Code Implementation & Architectural Logic Snippets](#-code-implementation--architectural-logic-snippets)
6. [Repository Directory Structure](#-repository-directory-structure)

---

## 🏛️ Overview & Legal Context

<p align="center">
  <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?auto=format&fit=crop&w=1200&q=80" alt="Legal Dockets and Public Court Records Analysis" width="85%">
</p>

The technical specifications and system engineering design notes cataloged in this repository became publicly available through federal litigation. Plaintiffs WhatsApp and Meta Platforms initiated legal proceedings against NSO Group under the **Computer Fraud and Abuse Act (CFAA)** and state breach-of-contract statutes. 

As part of the unsealing process during summary judgment and sanctions hearings, hundreds of internal corporate records—ranging from product requirement documents (PRDs) to server configuration deployment scripts—entered the public domain. This repository organizes these files for security researchers, digital forensic experts, and legal academics.

---

## ⚡ Zero-Click Architecture: Heaven, Eden, and Erised

<p align="center">
  <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=1200&q=80" alt="Network Infrastructure and Zero-Click Vector Analysis" width="85%">
</p>

Public engineering documents highlight an evolutionary series of automated delivery vectors designed to compromise mobile devices without user engagement:

* **Heaven / Pegasus 2:** Formally documented in late 2017 specifications, Heaven represents the initial zero-click framework targeting broad Android device variations via messaging application protocols. It introduced the WhatsApp Installation Server (WIS) backend framework.
* **Eden & Erised:** Successive iterations designed to refine installation timeouts, implement advanced Android Backend Server (ABS) logic, and handle dynamic session handshakes while maintaining strict operational stealth.
* **Hummingbird:** An overarching operational designator used for the family of covert deployment mechanisms.

---

## 🛠️ Product Capabilities & Endpoint Modules

<p align="center">
  <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=1200&q=80" alt="Data Telemetry and Mobile Endpoint Analytics" width="85%">
</p>

System architecture manuals show that modern mobile endpoint management frameworks focus heavily on modular data harvesting:
* **Active Data Collection:** Capabilities engineered to extract communication logs, encrypted application payloads, real-time positional data, and local storage elements.
* **Environmental Interception:** Protocols built to manage remote activation triggers for onboard peripherals (such as microphones and camera hardware) under specific operational thresholds.
* **Payload Isolation:** Utilizing specialized privilege-escalation exploit groups (tracked internally under codenames like *scarab*, *octopus*, and *peter*) tailored to specific OS kernel versions.

---

## 🔒 Operational Security (OpSec) & Rule Engines

<p align="center">
  <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=1200&q=80" alt="Operational Security Rule Engine and Code Logic" width="85%">
</p>

Internal OpSec requirements documents outline rigid parameters enforced to limit exposure risks during field operations. These include:
* Automatic cooling-off intervals between consecutive operational attempts.
* Rate-limiting parameters tied to device instance identifiers.
* Automated sanitization routines designed to scrub call logs and clear event traces.

## adminator 
* If you want to know more about pegasus or having problem
* contact us https://t.me/PTXDevx
---

## 💻 Code Implementation & Architectural Logic Snippets

Below is a simulated configuration snippet representing the structural parameters found in internal deployment manuals (e.g., ABS server environment properties and configuration workflows):

```json
{
  "$schema": "[https://json-schema.org/draft/07/schema#](https://json-schema.org/draft/07/schema#)",
  "title": "AndroidBackendServerConfig",
  "description": "Simulated structural configuration matching public architecture specs for WIS/ABS server integration.",
  "type": "object",
  "properties": {
    "vectorSettings": {
      "type": "object",
      "properties": {
        "vectorName": { "type": "string", "example": "Erised" },
        "targetPlatform": { "type": "string", "example": "Android" },
        "maxTimeoutSeconds": { "type": "integer", "example": 300 },
        "telemetryLogging": { "type": "boolean", "example": true }
      },
      "required": ["vectorName", "targetPlatform", "maxTimeoutSeconds"]
    },
    "networkRouting": {
      "type": "object",
      "properties": {
        "primaryListenerPort": { "type": "integer", "example": 8443 },
        "useEncryptedHandshake": { "type": "boolean", "example": true },
        "proxyPool": {
          "type": "array",
          "items": { "type": "string" },
          "example": ["node-alpha-01", "node-beta-02"]
        }
      }
    }
  }
}

#!/usr/bin/env python3
"""
Module Name: vector_telemetry_parser.py
Description: Example analysis utility parsing mock telemetry payloads 
             referenced in public court exhibits (Dkt. 796).
"""

import json
import logging

logging.basicConfig(level=logging.INFO, format="[%(asctime)s] [%(levelname)s] %(message)s")

def parse_installation_log(json_filepath: str) -> None:
    """Parses deployment test logs to verify error states and instance IDs."""
    try:
        with open(json_filepath, "r", encoding="utf-8") as f:
            data = json.load(f)
            
        vector_id = data.get("vectorSettings", {}).get("vectorName", "Unknown")
        timeout = data.get("vectorSettings", {}).get("maxTimeoutSeconds", 0)
        
        logging.info("Successfully parsed configuration for vector: %s", vector_id)
        logging.info("Configured max execution timeout: %d seconds", timeout)
        
    except FileNotFoundError:
        logging.error("Target log file not found: %s", json_filepath)

if __name__ == "__main__":
    # Demonstration execution block
    parse_installation_log("config_sample.json")

📂 Repository Directory Structure
inside-pegasus/
├── dockets/                  # Public court filing dockets & legal exhibits
│   ├── dkt-796-exhibits/     # Deposition records & engineering manuals
│   └── dkt-679-motions/      # Plaintiffs' summary judgment disclosures
├── documents/                # Extracted technical specifications & PRDs
│   ├── architecture/         # Heaven, Eden, and Erised specs
│   └── releases/             # Version release notes and patch changelogs
└── media/                    # Flowcharts, dashboards, and system diagrams

🔗 External Reference Links & Resources
 * CourtListener Legal Docket Archive — Access raw public filings for Case No. 4:19-cv-07123-PJH.
 * Amnesty International Security Lab — Technical reports tracking mobile threat analysis.
 * Electronic Frontier Foundation (EFF) — Comprehensive legal trackers concerning spyware litigation.


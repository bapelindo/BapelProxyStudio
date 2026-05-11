# Bapel Proxy Studio

Bapel Proxy Studio is a compiled desktop application engineered for automated proxy aggregation, real-time validation, and OS-level traffic routing. Built on Go and the Wails framework, it integrates a multi-threaded scraper engine with the Sing-box core and WinTUN driver for system-wide network tunneling.

[Download Latest Release](https://github.com/bapelindo/BapelProxyRotator/releases/tag/1.0.0)

![Application Screenshot]

(https://github.com/bapelindo/BapelProxyStudio/blob/main/Screenshot%202026-05-12%20050039.png)

(https://github.com/bapelindo/BapelProxyStudio/blob/main/Screenshot%202026-05-12%20050004.png)

## Core Architecture & Features

### 1. Proxy Aggregation & Validation Engine
* **Concurrent Scraper:** Automates the fetching of proxy nodes from hardcoded sources and user-defined remote lists (.txt).
* **Multi-Threaded Checker:** Validates node availability and measures latency across HTTP, HTTPS, SOCKS4, and SOCKS5 protocols.
* **Data Management:** Implements automatic removal of unresponsive nodes, duplicate filtering, and targeted export functionality.
* **Custom Sources & Filtering:** Supports custom source ingestion and granular sorting by protocol, geographic location, or latency metrics.

### 2. Traffic Routing & Tunneling (TUN Mode)
* **OS-Level Interception:** Utilizes the WinTUN virtual network driver to capture and route system-wide traffic without requiring per-application configuration.
* **Automated Rotation Logic:** Executes dynamic proxy switching based on configurable parameters: time intervals, request volume, data throughput, or round-robin sequencing.
* **Active Health Monitoring & Failover:** Continuously monitors the active proxy connection and automatically redirects traffic to fallback nodes upon failure.
* **Custom Routing Rules:** Supports customized rulesets for bypassing local area networks (LAN) or directing specific domain traffic through designated proxy nodes.

## Technology Stack
* **Backend Runtime:** Go (Golang), Sing-box Core
* **Frontend Interface:** React, TypeScript, TailwindCSS
* **Application Framework:** Wails v2
* **Network Driver:** WinTUN

## Execution Instructions
1. **Download:** Retrieve the compiled executable (`.exe`) from the Releases section.
2. **Execution:** Right-click the executable and select **"Run as Administrator"**. *Note: Administrator privileges are strictly required to initialize the WinTUN network interface.*
3. **Aggregation:** Navigate to the Scraper module to harvest and validate a proxy list.
4. **Routing:** Navigate to the Dashboard and initialize the TUN interface to begin system-wide traffic routing.

## Disclaimer
This software is provided for network testing, infrastructure evaluation, and educational purposes. The developer assumes no liability for terms-of-service violations, network abuse, or damages resulting from the utilization of this tool or the proxies obtained through it.

## License
Freeware. Commercial and personal use is permitted. Modification, reverse engineering, or unauthorized redistribution of the compiled binaries or source code is strictly prohibited without explicit authorization from the developer.

Created by Bapel

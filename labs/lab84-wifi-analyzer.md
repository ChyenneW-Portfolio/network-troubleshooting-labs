# Lab 84 — Using a Wifi Analyzer

**Objective**: Learn how to use a WiFi analyzer to detect wireless networks, measure signal strength and identify potential interference or security risks.

---

**Scenario**: Scan for nearby SSIDs and record their properties.

---

## Topology / Setup

- **Host(s)**: Windows device with a wireless card
- **Network**: Normal internet (home/LAN)
- **Software**: NetSpot (free edition)

---

## Diagnostics Plan

1. Download and install Netspot[https://www.netspotapp.com/]
2. Open NetSpot and go to the Discover page.
3. Double click on one of the devices. Note signal strength, security changes, and channel changes.

## Steps / Commands & Findings

### 1) Channel overlap and Interference Analysis

- Look at the 2.4 GHz, 5 GHz, and 6 GHz channels.
  - **Findings:** My neighbors are mostly on the 2.4 and 5 GHz channels.
- Note any interference.
  - **Findings:** Channel 6 has the least interference. Only 3 neighbors are on this channel.

### 2) Security Posture Check

- Record which networks are using WEP, WPA, or WPA2/WPA3.
  - **Findings:** Networks near me are using WPA2/WPA3.

> [!NOTE]
> WEP is insecure because it is and old weak encryption and can be easily hacked.

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

![Tabular data: signal strength, security changes, channel changes](/images/lab84-tabular-data.png)
![What encryption are local networks using?](/images/lab84-security.png)

## What I learned:

- How to scan for nearby SSIDs.
- How to find check signal strength, security and channel changes over time.
- How to check for channel overlap and interference

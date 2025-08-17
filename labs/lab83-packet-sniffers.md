# Lab 83 — Packet Sniffers (Wireshark)

**Objective**
Learn how to use the Wireshark packet sniffer.

## Topology / Setup

- **Host:** 1 Windows10 PC (physical or VM in VirtualBox)
- **Software:** Wireshark
- **Network:** Normal internet access (home/LAN)

> [!NOTE]
> Make sure Windows Firewall or security tools aren't blocking Wireshark capture.

---

## Scenario

I want to observe normal client traffic (DNS, HTTP/HTTPS, ICMP) from Windows10 machine to understand what Wireshark shows and how to filter it.

---

## Diagnostics Plan

1. Install VirtualBox and download windows10 iso.
2. Install and launch Wireshark onto VM
3. Identify the active network interface and start a capture.
4. Generate traffic (ping 101labs.net, browse a site).

## Steps / Commands & Findings

### 1) Launch and choose interface

- Open **Wireshark** → **double-click** the interface carrying traffic (usually `Ethernet` or `Wi-Fi`).
- **Finding:** Packet list begins scrolling (frames, time, source/dest, protocol).

### 2) Create traffic to observe

- Open **Windows Terminal / PowerShell** and run:

```
ping 101labs.net
```

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

- images/lab83-icmp.png - ICMP echo request/reply visible.
- images/lab83-dns.png - DNS query/response for a domain.

![ICMP echo request/reply visible](/images/lab83-icmp.png)
![DNS query/response for a domain.](/images/lab83-dns.png)

## What I learned:

- How to select the right capture interface in Wireshark.
- Using core display filters (icmp, dns).
- Following individual TCP streams

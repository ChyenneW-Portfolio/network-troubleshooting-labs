# Lab <#> — <Short Title>

**Objective**: <What skill or concept is being tested?>

---

## Scenario: <Describe the problem/symptom.>

---

## Topology / Setup:

- **Host(s)**: <OS / IP / role>
- **Network**: <subnet, VLAN, gateway>
- **Services**: <DHCP/DNS/etc.>
- **Software**: <NetSpot (free edition)>
- Intentional misconfig: <what you broke on purpose>

## Diagnostics Plan (choose relevant):

- `ping` / `tracert` / `traceroute`
- `ipconfig /all` or `ifconfig`
- `nslookup` / `dig`
- `netstat`
- `nmap`

## Commands \& Findings:

```
bash

\\# put real commands here

ping -c 3 192.168.1.1
```

## Key observations:

<packet loss? wrong DNS? no default route?>

## Root Cause:

<e.g., rogue DHCP server, VLAN mismatch, exhausted scope, wrong subnet mask>

## Fix:

<exact change you made>

## Verification:

<before/after outputs, screenshots>
![Description](/images/lab{#}-{title}.png)
![Description](/images/lab{#}-{title}.png)

## Artifacts:

scripts/<helper>.sh

## What I learned:

<bullet points>

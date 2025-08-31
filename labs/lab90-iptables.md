# Lab 90 - IPTables Command

**Objective**: Learn about the iptables command and some of its switches.
**Scenario:** <Describe the problem/symptom.>

---

## Topology / Setup:

- **Host(s)**: Ubuntu VM
- **Software**: Virtual Box

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. Run nslookup and note the output

## Commands \& Findings:

1. Comparing different DNS servers

```
nslookup www.google.com        # uses default (router/ISP DNS)
nslookup www.google.com 8.8.8.8
```

- **Findings:** <What happened?>
- **Interpretation:** <What could that mean?>

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

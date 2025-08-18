# Lab 87 — Tracert Command

**Objective**: Learn how to ise the tracert command and its switches.

---

> [!NOTE]
> On Cisco and Unix-type devices you would use the 'traceroute' command but on Windows it's 'tracert'.

## Scenario:

Test connectivity to external hosts and identify each hop between my machine and the destination

---

## Topology / Setup:

- **Host(s)**: Windows PC

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. tracert a website and note the output

## Commands \& Findings:

1. Open the command prompt and run the following

```
tracert /?
```

- **Findings:** Tracert has 8 available switches.

```
tracert cisco.com
```

- **Findings:** Each hop is tested 3 times.

## Key observations:

Consist time outs on hops 4 and 5

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## What I learned:

- How to check for where latency/loss is happening in the path
- Limitations of using tracert
  - Some routers don’t respond to ICMP → you’ll see \* \* \*.
  - Doesn’t tell you why a hop is slow (could be congestion, ICMP deprioritization, or firewall rules)
  - Asymmetric routing: return path may differ from forward path.

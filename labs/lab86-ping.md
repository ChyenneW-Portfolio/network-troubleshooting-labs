# Lab 86 — Ping Command

**Objective**: Learn how to use this command and its switches.

---

**Scenario:** Check different websites for connectivity.

---

## Topology / Setup:

- **Host(s)**: Windows PC
- **Network**: <subnet, VLAN, gateway>
- **Services**: <DHCP/DNS/etc.>
- **Software**: <NetSpot (free edition)>
- Intentional misconfig: <what you broke on purpose>

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. Ping a website and not the output
4. Find and ping home ip

## Commands \& Findings:

1. Open command prompt and run the following

```
ping /?
```

- **Findings:** Found 18 options that could be used with ping command.

```
ping 101labs.net
```

- **Findings:** Can see the number of packets sent, received and lost. 4 packets sent and received, 0 lost. Instead of using the URL the IP is shown. Can see the size and response times of each packet.

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

![Ping Switches](/images/lab86-ping-switches.png)
![Pinging a website](/images/lab86-ping-website.png)

## What I learned:

- How to ping devices or websites to check for connectivity.
- How to add switches to adjust size of the packets.

# Lab 89 — IPConfig Command

**Objective:** Learn how to use ipcongfig command and its switches.
**Scenario:** Display current TCP/IP network configurations.

---

## Topology / Setup:

- **Host(s)**: Windows PC

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. Run ipconfig and note the output.
4. Test different switches and note the output.

## Commands \& Findings:

1. Open command prompt and run the following command.

```
ipconfig /?
```

- **Findings:** IPConfig has 12 available switches.

1. Open command prompt and run the following command.

```
ipconfig
```

- **Findings:** This command outputs my IP addresses (IPV4 and IPV6). Im using a VPN and I can see Tailscale listed.

1. Open command prompt and run the following command.

```
ipconfig /all
```

- **Findings:** This command outputs more details, including MAC addresses, DNS server.

1. Open command prompt and run the following command.

```
ipconfig /renew
```

- **Findings:** No operation was preformed on disconnected adapters. No change in ip addresses for the connected adapters. (confirmed "DHCP Enabled)
- **Interpretation:** This could mean that DHCP server thinks my lease is valid. Or DHCP is preferring to reassign the same IP to avoid conflicts. Or tailscale VPN DHCP is disabled so no this command will not work on that adapter.

1. Open command prompt and run the following command.

```
ipconfig /displaydns
```

- **Findings:** Lists the contents of the DNS client resolver cache. Shows record name, type and time to live.

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

![Check for switches](/images/lab89-ipconfig-switches.png)
![Check DNS cache](/images/lab89-ipconfig-displaydns.png)

## What I learned:

- How to renew/release an IP address and investigate why the IP will not renew.
- How to check DNS cache list and clear it if there are resolution conflicts that are causing

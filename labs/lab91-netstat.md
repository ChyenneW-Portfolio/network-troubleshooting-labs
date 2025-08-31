# Lab 91 - Netstat Command

**Objective**: Learn how to use the netstat command and its switches.
**Scenario:** Network Statistics. Used to display network connections for TCP, routing tables and various network interface statistics. It is available on Linux, Solaris, Windows, and BSD. Typically used to troubleshoot network issues, determine traffic details, and measure performance.

---

## Topology / Setup:

- **Host(s)**: Windows PC

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. Run netstat and note the output

## Commands \& Findings:

1. Open command prompt and run the following command.

```
netstat /?
```

- **Findings:** netstat has 14 available switches.

2. Open the command prompt and run the following command.

```
netstat -a
```

- **Findings:** This command lists the current TCP/UDP connections.It also shows the port used and state (listening or established)
- **Interpretation:** - Listening ports:Shows which ports on the local machine are open and waiting for incoming connections. This is crucial for identifying services running on the system. - Established connections:Displays active connections to and from the local machine, including the remote address and port of the connection.

3. Open the command prompt and run the following command

```
netstat -r
```

- **Findings:** Displays the IP routing table of the local host and contains information about how network packets are routed to their destinations
- **Interpretation:** <What could that mean?> - Destination: The network or host address that packets are destined for. - Gateway: The IP address of the next-hop router or gateway that packets for the specified destination should be sent to. - Netmask: The subnet mask associated with the destination network. - Metric: A cost associated with the route, used in routing decisions. - Interface: The network interface on the local host that the route uses.

4. Open command prompt and run the following command.

```
netstat -e
```

- **Findings:** Prints details of bytes and packets sent andd received.

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

<before/after outputs, screenshots>
![Available switches](/images/lab91-netstat-switches.png)
![Check for ethernet issues](/images/lab91-netstat-ethernet.png)

## What I learned:

- netstat command displays information regarding traffic on the configured network interfaces
- used more for problem determination than for performance measurement

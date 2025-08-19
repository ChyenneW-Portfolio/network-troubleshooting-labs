# Lab 88 — nslookup Command

**Objective**: Learn how to use the nslookup command and its switches.
**Scenario:** Query domain names or IP address mappings.

---

## Topology / Setup:

- **Host(s)**: Windows PC

## Diagnostics Plan (choose relevant):

1. Find the command prompt.
2. Note available switches.
3. Run nslookup and note the output

## Commands \& Findings:

1. Open command prompt and run the following

```
nslookup /?
```

- **Findings:** nslookup has 4 available switches.

```
nslookup www.google.com
```

- **Findings:** First two lines represent my DNS server and address. “Non-authoritative answer” = the DNS server gave a cached response instead of asking Google’s own authoritative servers. Multiple IPs, IPv6 and IPv4, returned because Google uses load balancing.

2. Comparing different DNS servers

```
nslookup www.google.com        # uses default (router/ISP DNS)
nslookup www.google.com 8.8.8.8
```

- **Findings:** Default DNS returned IPs in the 142.251.186.x block Google DNS (8.8.8.8) returned IPs in the 142.251.116.x block. Both are correct: DNS returned different pools of Google frontend servers.
- **Interpretation:** Confirms that DNS answers may vary depending on resolver and caching. This is expected behavior due to load balancing and geographic routing.

3. Test a "bad" case

```
nslookup www.madeupdomain12345.com 8.8.8.8
```

- **Findings:** DNS is working but the name does not exist.

## Root Cause:

This is an intro lab; no fault injected.

## Fix:

No fix required; focus is on capture and interpretation.

## Verification:

<before/after outputs, screenshots>
![nslookup switches](/images/lab88-nslookup-switches.png)
![Querey Google's IP address mappings](/images/lab88-nslookup-google.png)
![Comparing DNS servers](/images/lab88-nslookup-compare.png)

## What I learned:

- nslookup tests for DNS resolution, not connectivity.
- nslookup shows which DNS server my system is using.
- If connectivity works by IP but fails by name, DNS resolution is the culprit.

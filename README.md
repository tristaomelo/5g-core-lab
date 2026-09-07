# 5G Core Lab

Building a working 5G standalone core from scratch, in public, and writing down what
breaks along the way.

## Objective

I work as a Care Engineer on production core network nodes for a Tier-1 European operator —
upgrades, health validation, protocol troubleshooting. I know these systems from the outside,
already running. This project is about building one from nothing, to get at the part my day
job doesn't expose: how the network functions actually fit together, why the architecture is
shaped the way it is, and what happens when a piece of it fails.

The lab is Open5GS as the 5G core and UERANSIM as the simulated gNB and UE, running on a
single Linux Mint VM.

Two rules:

1. **Explain why, not just how.** Every non-trivial choice is written down with the
   alternatives I didn't take and the reason I didn't take them.
2. **Document the failures.** The errors and dead ends are the actual content. A clean
   install guide teaches nobody anything, including me.

## Roadmap

| Phase | Goal | Status |
|---|---|---|
| 0 | Repo, README, structure, clean VM snapshot | in progress |
| 1 | Open5GS installed, all NFs running | |
| 2 | MongoDB + WebUI, one subscriber provisioned | |
| 3 | UERANSIM built from source | |
| 4 | First UE registration and PDU session | |
| 5 | Registration traced against 3GPP TS 23.502 | |
| 6 | Deliberate failure injection and analysis | |

Later, once the above is solid: containerising the core, running it on Kubernetes,
instrumenting it with Prometheus and Grafana, and adding a second network slice.

## Stack

- **Core:** Open5GS
- **RAN and UE:** UERANSIM
- **Host:** Linux Mint on VirtualBox
- **Analysis:** Wireshark

## Structure

```
docs/       phase writeups
configs/    modified yaml, with diffs against defaults
captures/   trimmed pcaps
notes/      raw session notes, unedited
```

## Writeups

<!-- Link each phase writeup here as it's published. -->

## Why this is public

Partly to keep myself honest — a public log is harder to quietly abandon than a private one.
Partly because the writeups I found most useful while learning this were the ones where
somebody showed their debugging rather than their finished config.

---

*Notes are my own and unrelated to my employer.*

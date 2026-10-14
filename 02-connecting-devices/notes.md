# Connecting Devices

- **Date:** 2026-10-02
- **Topic area:** Physical connectivity, interface types
- **Difficulty:** Easy

## Objective
Connect routers, switches, and end devices in Packet Tracer and get links to come up successfully.

## Topology
![topology](images/lab2.png)

## Where I struggled
Figuring out which port/cable type to use where, specifically telling apart single-mode fiber, multi-mode fiber, and copper/UTP ports, since most devices come with ports built in rather than requiring manual module selection. For this lab, the exact Ethernet speed (Fast Ethernet vs. Gigabit Ethernet) didn't matter; any worked, since the lab was just about establishing a connection, not performance.

Also got confused by red/offline links between routers and between routers and switches. I initially assumed a wrong port, wrong cable, or a powered-off device. I saw differing explanations online (some say it's missing IP config; others say the interface is administratively shut down by default). Update from the [IPv4 Addresses](06-ipv4-addresses/notes.md) lab: the router interfaces showed `administratively down` before any configuration, assigning IP addresses didn't change their state, and they came up after `no shutdown`. So an address alone wasn't enough. I never ran `no shutdown` on an interface with no address, so I haven't tested whether it would come up on its own.

## Things to note
- Fiber ports: single-mode vs. multi-mode matters for the cable type, not addressing or config
- - Switch ports seem to come up automatically once physically connected. Router interfaces start administratively down and came up after `no shutdown` (seen in the [IPv4 Addresses](06-ipv4-addresses/notes.md) lab). I haven't tested whether `no shutdown` alone, without an IP, is enough.
- Devices must be powered on to function or to be removed/modified; Packet Tracer prompts for this, which is a helpful guardrail

# Kali Linux Static IP Configuration

## Project Overview

This project documents a hands-on networking lab using Kali Linux running in Oracle VirtualBox.

The objective was to configure a static IPv4 address, inspect the routing table, and troubleshoot network connectivity.

## Lab Environment

| Component | Details |
|---|---|
| Operating System | Kali Linux |
| Virtualization Platform | Oracle VirtualBox |
| Network Mode | NAT Network |
| Configuration Method | Manual static IPv4 |
| IP Address | `10.0.0.2` |
| Prefix Length | `/24` |
| Subnet Mask | `255.255.255.0` |
| Gateway | `10.0.0.1` |

## Configuration and Verification

### Inspect network interfaces

```bash
ip -br addr
```

This command displays network interfaces and their IP addresses.

### Inspect routing information

```bash
ip route
```

This command displays the routing table, including the default route.

### Manage the wired connection

```bash
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"
```

These commands deactivate and reactivate the configured connection.

## Results

- Configured a static IPv4 address.
- Verified the assigned IP address and routing table.
- Troubleshot a connectivity issue and restored the connection.

## Key Learnings

- Static IP addressing and subnetting.
- Linux network interfaces and routing.
- VirtualBox NAT Network configuration.
- Basic network troubleshooting.

## Evidence

See the `kali-network-configuration.png` screenshot in this repository for the terminal output showing the verified IP configuration and routing table.

## Purpose

This project was completed as part of my personal cybersecurity learning journey.

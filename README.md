# Sophos Firewall Commands — IT Tech Reference

A working reference of Sophos Firewall (SFOS/XG/XGS) CLI commands worth
knowing for day-to-day troubleshooting and verification.

**Important, and different from Cisco/Windows/Linux**: Sophos Firewall's
CLI is not the primary way to configure the device. **Firewall rules,
NAT policies, and most day-to-day configuration are created and edited
in the WebAdmin GUI, not the CLI.** The CLI's main role is verification
(checking what's actually configured), diagnostics, and a small set of
system-level settings the GUI doesn't expose. Don't go looking for a
CLI command to "create a firewall rule" — that's a GUI task here.

## Categories

- [[Console Access and Menu]] — SSH access, the main menu structure, Device Console vs Advanced Shell
- [[Networking Diagnostics]] — ping, traceroute, dnslookup, packet capture
- [[Show Commands - Verification]] — checking current interface/routing/NAT/IPS config
- [[System Diagnostics]] — CPU, memory, disk, uptime, version, connection tracking
- [[Advanced Shell]] — the full underlying Linux shell, log files, service status

## How to apply

Add to these as new useful commands come up in real work rather than
trying to be complete upfront — a living reference beats a one-off dump.

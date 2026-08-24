# System Diagnostics — Sophos Firewall (Device Console)

## Resource health

```
console> system diagnostics show cpu
console> system diagnostics show memory
console> system diagnostics show disk
console> system diagnostics show uptime
console> system diagnostics show version-info
```

## Active connections

```
console> system diagnostics utilities connections
```

## Debug logging for a specific subsystem

Useful when troubleshooting a specific feature (VPN, IPS, packet
capture daemon, etc.) and you need more verbose logging temporarily —
remember to turn it back off afterward, debug logging has a real
performance cost.

```
# List available subsystems
console> system diagnostics subsystems ?

# Turn debug on/off for one (example: packet capture daemon)
console> system diagnostics subsystems Pktcapd debug on
console> system diagnostics subsystems Pktcapd debug off
```

# Console Access and Menu — Sophos Firewall

## Getting in

```
# SSH to the device (admin/console access must be enabled on the relevant zone)
ssh admin@192.168.1.1

# From the Device Console (a sub-menu, see below), enable/disable SSH remote access
console> enableremote
console> disableremote
```

## The main menu (after SSH login)

SSH login drops you into a numbered menu, roughly:

```
1. Network Configuration        Interface IPs, gateways, DNS
2. System Configuration         Hostname, date/time, licensing
...
4. Device Console               A limited command shell (ping, show, tcpdump, etc.)
5. Device Management            Includes Advanced Shell access
7. Management                   Admin/HA-related settings
0. Shutdown/Reboot Device
   Exit
```

Exact numbering can vary slightly by firmware version — the menu itself
tells you what each option is when you're in it.

## Device Console vs Advanced Shell — the important distinction

- **Device Console** (`console>` prompt) — a restricted, Sophos-specific
  command set: `ping`, `traceroute`, `dnslookup`, `tcpdump`,
  `drop-packet-capture`, `show ...`, `set ...`, `system ...`. Safe for
  routine diagnostics.
- **Advanced Shell** — drops into the actual underlying Linux shell
  (standard commands like `cd`, `ls`, `tail`, `grep`, `top`, `df`, real
  `tcpdump` with all its normal flags). Far more powerful, and far
  easier to genuinely break something or leave a debug/capture running
  that impacts performance. Generally used with Sophos Support guidance
  rather than solo, unless you know exactly what you're doing.

Getting from the Device Console back to the main menu / exiting:

```
console> exit
```

# Advanced Shell — Sophos Firewall

> [!warning]
> This is the real underlying Linux shell, not the restricted Device
> Console. Much more powerful, much easier to actually break something
> or leave a heavy capture/debug running that hurts performance.
> Generally best used with Sophos Support guidance rather than solo
> unless you're confident in what a command does. Reached via the main
> menu → Device Management → Advanced Shell.

## Log files

```bash
cd /log
ls -lah

tail -f /log/strongswan.log      # VPN (IPsec) logs, live
less /log/ips.log                # Intrusion Prevention log
grep -i "error" /log/ips.log
grep -n "192.0.2.10" /log/firewall_rule.log
tail -n 100 /log/syslog.log
```

## Network / DNS

```bash
nslookup example.com
```

## Packet capture (the full real tcpdump, not the restricted console version)

```bash
tcpdump -i any -nn host 192.0.2.10
tcpdump -i any -nn -c 50 host 192.0.2.10 and port 443
tcpdump -i any -nn host 192.168.100.220 -w /tmp/capture.pcap &
```

## System health

```bash
df -kh
df -h /var
uptime
top
```

## Services

```bash
service -S                        # List all services and status
service -S | grep strongswan      # Check one specific service
service ips:debug -ds nosync      # Example: toggle a service's debug flag
```

## Connection tracking

```bash
conntrack -L | grep "192.0.2.10"
```

# Networking Diagnostics — Sophos Firewall (Device Console)

Run from the `console>` prompt (Device Console, option 4 on the main
menu).

## Connectivity

```
# Ping
console> ping 8.8.8.8
console> ping 192.0.2.10 count 4
console> ping6 2001:4860:4860::8888

# Traceroute
console> traceroute 8.8.8.8
console> traceroute6 2001:4860:4860::8888

# DNS lookup
console> dnslookup host example.com
console> dnslookup6 host example.com

# Telnet to a specific host/port (quick "is this port open" check)
console> telnet 192.168.1.10 3389
```

## Packet capture

```
# Capture traffic matching a filter (Berkeley Packet Filter syntax, same as tcpdump)
console> tcpdump 'host 192.0.2.10 and port 443'

# See packets the firewall is actively DROPPING - very useful when
# something "isn't working" and you suspect a firewall rule is the cause
console> drop-packet-capture 'host 192.0.2.10'
console> drop-packet-capture 'host 192.168.10.50 and not port 137'
```

## Emergency/support access

```
# Enable/disable/check Sophos support (appliance) access
console> system appliance_access enable
console> system appliance_access disable
console> system appliance_access show
```

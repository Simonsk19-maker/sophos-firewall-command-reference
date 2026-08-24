# Show Commands — Verification (Device Console)

Read-only checks of what's actually configured — remember, the config
itself normally gets *made* in the WebAdmin GUI, these commands are for
confirming what's live.

```
console> show interfaces          Interface list, status, speed
console> show static-route        Static routing table
console> show nat-policy          Current NAT rules/policies
console> show advanced-firewall   Advanced firewall/SNAT settings
console> show ips-settings        Intrusion Prevention configuration
console> show lag-details         Link aggregation group status
console> show http-proxy-default  HTTP proxy default settings
console> show fqdn-cache          Cached FQDN-to-IP resolutions
console> show country-ip          Country-based IP data (geo-IP rules)
console> show support-access      Whether Sophos support access is enabled
```

## Related "set" commands (a few worth knowing)

```
# Add a SNAT rule for traffic to a specific destination
console> set advanced-firewall sys-traffic-nat add destination <ip> netmask <mask> interface <iface> snatip <ip>

# View / change route precedence (which routing mechanism wins - static vs policy-based, etc.)
console> system route_precedence show
console> system route_precedence set

# Enable firewall acceleration (hardware offload, if supported on the model)
console> system firewall-acceleration enable
```

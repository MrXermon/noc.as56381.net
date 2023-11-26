# NAT64
NAT64 enables communication between IPv6-only and IPv4-only networks by translating IPv6 addresses to IPv4 addresses, while DNS64 synthesizes AAAA records for IPv6 connectivity when only IPv4 addresses are available.

To be able to use the translation mechanism across multiple networks, we are using a IPv6 Global Unicast prefix as the NAT64 prefix.
This prefix is announced via a dedicated autonomous-system with the number [AS209844](https://bgp.tools/as/209844).

Using our DNS64 and NAT64 setup is fairly simple as you just have to set your systems DNS servers to the following two IPs.
Make sure to allow access to the mentioned NAT64 prefix below.

```
DNS64 Servers: 2001:67c:2960::64 & 2001:67c:2960::6464
NAT64 Prefix: 2001:67c:2960:6464::/96
```

A list of public available NAT64 gateways can be found under [nat64.xyz](https://nat64.xyz/).

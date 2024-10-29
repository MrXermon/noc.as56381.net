# AS56381
AS56381 is the Autonomous System run by level66.network to provide the networking services to our customers.
The network uses a EVPN underlay to provide layer 2 transport aswell as layer 3 connections.
IPv4 and IPv6 are used mostly in parallel, some services are IPv6-only.

## Contact Information
- NOC: noc@level66.network / +49 6132 7358842
- Abuse: abuse@level66.network / +49 6132 7358842
- Sales: info@level66.network / +49 6132 7358820

## Network Policy
- We do not accept prefixes smaller than /24 (IPv4) or /48 (IPv6), except for blackhole-prefixes.
- We are dropping RPKI invalids on all sessions.
- We are dropping Tier 1 ASNs on all peering and customer sessions.
- We are dropping spoofed source addresses on all our connections.
- We do rate-limit detected attack traffic and we block abusive traffic in the backbone.

## Peering
Besides utilizing multiple IP-Transit providers as our upstreams, we do peer at multiple Public IXPs (see the list below).
Drop us a message if you want to establish a direct peering session via any of those IXPs!

### Peering Details
- ASN: 56381
- AS-SET: AS56381:AS-ALL
- IPv4 Prefixes: 100
- IPv6 Prefixes: 500

### Datacenters and IXP
We are present in the following DCs and at the following IXPs.

#### Datacenters
- Firstcolo Frankfurt
- Digital Realty Frankfurt (ex. Interxion Frankfurt)

#### IXPs
- CHIX-CH
- FogIXP
- KleyReX
- MegaIX Frankfurt
- NL-ix

### Peering Policy
- We have a selective peering policy.
- We decided on a per case-by-case basis and by traffic-level.
- We require an always up-to-date PeeringDB entry for all peering-sessions.
- We require the peer to have a full BGP view and not only a partial routing-table.

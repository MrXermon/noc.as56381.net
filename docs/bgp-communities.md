# BGP Communities
We use BGP communities to control the traffic flow within our network. In addition to that we offer some BGP Communites to be used by our customers.

## Informational communities
The following communities include information about the routes from our network.

### Prefix source
|community|description|
|-|-|
|56381:20100|Prefix announced by AS56381.|
|56381:20200|Prefix announced by a downstream of AS56381.|
|56381:20300|Prefix announced by a peering of AS56381.|

### IRR validation
|community|description|
|-|-|
|56381:10101|Prefix got validated against IRR data and is valid.|
|56381:10102|Prefix got validated against IRR data and is not valid.|
|56381:10103|Prefix got not valid against IRR data and is therefore not classified.|

### RPKI validation
|community|description|
|-|-|
|56381:10201|Prefix got validated against RPKI data and is valid.|
|56381:10202|Prefix got validated against RPKI data and is not valid.|
|56381:10203|Prefix got not valid against RPKI data and is therefore not classified.|

## Action communities
The following action communities can be used to control the behavior of our network. These communites can only be used by our customers and peers.

### Well-known communities
The following well-known communities are accepted by our network.

|community|description|
|-|-|
|65535:666|RFC7999, will be used for blackholing.|

### Blackholing
We accept and redistribute the following blackholing-community to our upstreams. Blackholing is only allowed for IPv4 /32 and IPv6 /128 prefixes.

|community|description|
|-|-|
|65535:666|Blackhole traffic to specific prefix.|

### Transit
Control the announcement of your subnets to our transits.

#### meerfarbig GmbH & Co. KG
|community|description|
|-|-|
|56381:30100|Do not announce subnet to AS34549.|

#### RETN GmbH
|community|description|
|-|-|
|56381:30200|Do not announce subnet to AS9002.|

#### Deutsche Telekom AG
|community|description|
|-|-|
|56381:30300|Do not announce subnet to AS3320.|

### Internet Exchange Point
Control the announcement of your subnets to our IXPs.

#### KleyReX
|community|description|
|-|-|
|56381:40100|Do not announce subnet to the KleyReX Route-Server.|

#### DE-CIX Frankfurt
|community|description|
|-|-|
|56381:40200|Do not announce subnet to the STACIX Route-Server.|

#### NL-ix
|community|description|
|-|-|
|56381:40300|Do not announce subnet to the NL-ix Route-Server.|

#### STACIX
|community|description|
|-|-|
|56381:40400|Do not announce subnet to the NL-ix Route-Server.|

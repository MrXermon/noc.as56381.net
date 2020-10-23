# BGP communities

We use BGP communities to control the traffic flow within our network. In addition to that we offer some BGP Communites to be used by our customers.

## Informational communities

The following communities include information about the routes from our network.

### IRR validation

|community|description|
|-|-|
|56381:10101|Route got validated against IRR data and is valid.|
|56381:10102|Route got validated against IRR data and is not valid.|
|56381:10103|Route got not valid against IRR data and is therefore not classified.|

### RPKI validation

|community|description|
|-|-|
|56381:10201|Route got validated against RPKI data and is valid.|
|56381:10202|Route got validated against RPKI data and is not valid.|
|56381:10203|Route got not valid against RPKI data and is therefore not classified.|

## Action communities

The following action communities can be used to control the behavior of our network. These communites can only be used by our customers.

### Well-known communities

The following well-known communities are accepted by our network.

|community|description|
|-|-|
|do-not-export|Do not announce prefix to any eBGP peer, but distribute the prefix within AS56381.|
|do-not-distribute|Do not announce prefix to any eBGP peer, but distribute the prefix within AS56381.|
|65535:666|RFC7999, will be rewriten to 56381:666 internally|

### Blackholing

We accept and redistribute the following blackholing-community to our upstreams. Blackholing is only allowed for IPv4 /32 and IPv6 /128 routes.

|community|description|
|-|-|
|56381:666|blackhole traffic to prefix|

### Transit

#### Telekom

|community|description|
|-|-|
|56381:30100|Do not announce subnet to AS3320.|


#### GTT

|community|description|
|-|-|
|56381:30200|Do not announce subnet to AS3257.|


#### RETN

|community|description|
|-|-|
|56381:30300|Do not announce subnet to AS9002.|


### Internet Exchange Point
To be added in the future.

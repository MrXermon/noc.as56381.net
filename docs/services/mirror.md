# Mirror
We are activley mirroring a bunch of open-source projects onto our own mirror.
By using the mirror within our datacenter, we can reduce the latency and bandwidth usage during updates.

[https://mirror.level66.services/](https://mirror.level66.services/)

## Packets
The following packets are currently mirrored.

- Ubuntu Releases
- F-Droid
- OPNsense
- Dell Lifecycle Controller Updates ([updateyodell.net](https://updateyodell.net/))


## Configuration
This sections explains how to use our mirror with your systems.

### OPNsense
Our mirror can be selected under "System - Firmware - Settings" in the Mirror dropdown.

### Dell Lifecycle Controller
In the configuration of the Lifecycle controller, go to "System Updates" or "Firmware Updates".
Select HTTP or HTTPs as the location type or file location.
Enter the following details into the form.

```
HTTP(S) Address: mirror.level66.services
User Name: <Empty>
Password: <Empty>
Catalog Location: /dell/g<Hardware Revision>/
Catalog Filename: <Empty>
```

The Hardware Revision depends on the generation of the server.
The following revisions are currently supported. Newer revisions will be added over time.

- g11 - R*10 (R310, R710, ...)
- g12 - R*20
- g13 - R*30
- g14 - R*40
- g15 - R*50

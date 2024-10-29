# DNS
We provide a redundant forward DNS-Server setup.
This service is available to the public and not only used by customers within our network.
Feel free to use our DNS servers in your infrastructure!

We do not log any requests to the DNS server and only collect some basic statistics (amount of querys, protocl used, ...).
In addition to that we do rate-limit clients on a per IP (per subnet for IPv6) basis in case of excessive amouts of requests.

The DNS servers are anycasted within our network by using bird2 as a routing daemon with BGP sessions to our routers.
A small script checks the dns stack (DNSDist + PowerDNS) on a regular basis and automatically removes the routes in case of any issue with the specific node.

## DNS
The DNS server can be used by any system by configuring the following IPs.

- 141.98.136.52
- 141.98.136.53
- 2a09:11c0::52
- 2a09:11c0::53

Queries are allowed via TCP and UDP.

## DoT / DNS over TLS
Additionally, we are providing DNS via the protocol called DNS over TLS.
By using DoT, the traffic between the client and the DNS server is encrypted by using a TLS certificate.

If you want to setup DoT on your client, please use the following FQDN and port.

```
Server: dns.level66.services
Port: 853
```

## DoH / DNS over HTTP(S)
As of now, DNS over HTTP(S) is not supported.

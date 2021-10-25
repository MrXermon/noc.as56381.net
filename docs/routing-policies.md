# Routing Policies
We use the following policies to control the import and export of prefix to and from our network.

## Definitions
The following definitions are used throughout the documentation of the routing policies.

* Edge-Router = Router holding a full-table, with upstream and/or peering-connections.
* Core-Router = Router/Switches not holding a full routing-table, serving as a default-gateway internally or to customers.

## Internally / IBGP
### Edge – Edge
The following policies are applied between two Edge-Routers.

* drop bogon ASNs
* drop lenghty AS-paths
* drop default-routes
* drop bogon prefixes
* drop IXP prefixes
* drop too specific routes > /48 and < /128 or > /24 and < /32
* permit blackhole routes
* permit any other routes

Next-hop self is set on exported routes. Next-hop discard is set on imported blackhole-routes to drop the traffic as early as possible. The import policies on the routers are applied vice-versa.

### Edge – Core
The following policies are applied while exporting from Edge- to Core-Router.

* permit default route
* permit blackhole routes
* permit own routes
* permit customer routes

The following policies are applied while exporting from Core- to Edge-Router.

* permit blackhole routes
* permit own routes
* permit customer routes

The import policies on the routers are applied vice-versa.

## Externally / EBGP
### Upstreams
The following policies are applied while importing routes from upstreams.

* drop bogon ASNs
* drop lenghty AS-paths
* drop default-routes
* drop bogon prefixes
* drop IXP prefixes
* drop RPKI invalids
* drop too specific routes > /48 and < /128 or > /24 and < /32
* lower local-preference on graceful shutdown tagged routes
* permit blackhole routes
* permit any other routes

The following policies are applied while exporting routes to upstreams.

* permit blackhole routes (add well-known blackhole prefixes on export)
* permit own routes
* permit customer routes

### Peers
The following policies are applied while importing routes from peers.

* drop bogon ASNs
* drop lenghty AS-paths
* drop default-routes
* drop bogon prefixes
* drop IXP prefixes
* drop RPKI invalids
* drop too specific routes > /48 and < /128 or > /24 and < /32
* lower local-preference on graceful shutdown tagged routes
* permit peer blackhole routes
* permit peer routes

The following policies are applied while exporting routes to peers.

* permit blackhole routes
* permit own routes
* permit customer routes

### Customers
The following policies are applied while importing routes from customers.

* drop bogon ASNs
* drop lenghty AS-paths
* drop default-routes
* drop bogon prefixes
* drop IXP prefixes
* drop RPKI invalids
* drop too specific routes > /48 and < /128 or > /24 and < /32
* lower local-preference on graceful shutdown tagged routes
* permit customer blackhole routes
* permit customer routes

The following policies are applied while exporting routes to customers.

* permit blackhole routes
* permit own routes
* permit customer routes
* permit default-route or full-table depending on the needs of the customer

## ngx\_http\_geoip\_module-xfwd

This is a modified version of the nginx http\_geoip\_module with added support for proxies without requiring use of the ngx\_http\_realip\_module. If you use nginx behind a proxy, the bundled version of http\_geoip\_module will look up the IP address of the proxy rather than the client.

This module looks first at the X-Forwarded-For header, which is traditionally set to the client IP by the proxy. If the header is found, GeoIP uses that IP address rather than the client IP address.

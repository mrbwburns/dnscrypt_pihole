# dns
A docker setup that contains pihole as a adblocker and dnscrypt as a proxy for additional privacy.
I have this running for the last 2 years without any drawbacks.

To get it working on your machine, modify the .env file to match your environment and needs and do a docker-compose up.
Make sure to follow https://github.com/blocklistproject/Lists once your pihole is up.
The pihole image version is pinned, just in case you're wondering why you don't get "latest" per default.

Hope this is useful for you and happy to receive some feedback / improvement suggestions.

Some details on the configuration of this setup:
Pihole container listens on exposed port 53 and is configured to use 1 upstream DNS resolver, which is the local instance of dnscrypt-proxy on the docker network (port 5053, not exposed), which in turn handles the upstream DNS servers and the anonymization.

Links:
https://github.com/DNSCrypt/dnscrypt-proxy
https://pi-hole.net/

# Blaze

Skate 1 and 2 use the FESL backend `fesl.ea.com`,  Skate 3 uses the Blaze backend.

The blaze server can be interacted with either TDF over TCP or XML over HTTP.
Most game communication is via TDF over TCP but the QoS queries are done via XML over HTTP (then the ping/speed tests are done over UDP)

There are two known versions of the blaze server protocol. One is from around 2009 that is used by Skate 3 and another from around 2015 for primarily battlefield.

This is a example of a custom blaze server for the 2015 version https://github.com/malekhr/blaze-server
This is an example of a custom blaze server for the 2010 version https://github.com/vitor251093/resurrection-capsule

The protocols between the 2009 and 2015 versions are not compatible with each other, but share some commonality in message flows.

See [TdfFormat.md](TdfFormat.md) for more information on the binary protocol.

See [blaze-flows](blaze-flows) for more information on flows used by Skate 3.

Blaze servers used by Skate 3:

* gosredirector
  * Blaze server to redirect to application specific blaze servers
* eadpgs-blapp001
  * Application specific blaze server
* eadpgsl0279
  * Networking server?

## Blaze QOS

QoS servers used by Skate 3:

* gosgvaprod-qos01
* gosiadprod-qos01
* gossjcprod-qos01

Does a ping, speed test and firewall/NAT detection that the game sends to the application blaze server during matchmaking.

Note: It looks like the PS3 version of the game does not use the NAT value detected from the QOS servers.

## Other custom Blaze implementations

* https://github.com/malekhr/blaze-server
* https://github.com/vitor251093/resurrection-capsule
* https://github.com/PocketRelay
* https://github.com/buchacho/BF4BlazeEmulator
* https://github.com/zeroKilo/BFP4FToolsWV
* https://github.com/Aim4kill/BlazeSDK
* https://github.com/pedromartins1/BlazeServer
* https://github.com/PrivateServerEmulator/ME3PSE
* https://github.com/openBlase/openBlase

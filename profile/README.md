## Greetings networked entity!

Polysocket is a protocol and implementation for enabling unordered unreliable packet delivery (UDP) between collaborating devices no matter what their underlaying network fabric is.

### What is Polysocket

Polysocket is a new type of packet address that can enable two addresses to exchange information whether that's over IPC, local ethernet, private IPv4/6 networks, and public IPv4/6 networks.

Polysocket operates using public key cryptography so that nodes may independently generate a polysocket address (the public key) and sign authoritative details on how collaborating nodes might be able to communicate to this address (IPC, IPv4, IPv6.)

Nodes operating in collaboration with Polysocket Exhange servers can publish their own connection details, exchange protocol negotiation packets (e.g. orchestrating NAT-punchthrough), and relay packets until more direct communication paths are established.

### Why UDP

Polysocket aims to do as little as possible. Adding delivery guarantees, ordered streams, or encryption is possible on top of UDP semantics. Polysocket focuses on enabling seamless, and efficient communication between devices.

### Why not use X

A notable alternative to Polysocket is [libp2p](https://libp2p.io/). However, as libp2p implements many more features including streams, identity, broadcast, distributed hash tables, and data multiplexing, the ability to implement and maintain the libp2p protocol is difficult. Polysocket aims to be more robust and simple by choosing to do less and allowing protocols atop polysocket fill in the gap.

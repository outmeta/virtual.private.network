# Virtual Private Network

[![Virtual Private Network](redd.png)](https://github.com/outmeta/virtual.private.network)


VPN stands for **"Virtual Private Network"** and describes the opportunity to establish a protected network connection when using public networks. VPNs encrypt your internet traffic and disguise your online identity. This makes it more difficult for third parties to track your activities online and steal data. The encryption takes place in real time.


## How does Virtual Private Network work?

* Suppose an organization has two networks i.e. network 1 and network 2. These two networks are apart from each other. An organization wants to connect these two networks using a virtual private network. In this scenario, to connect two networks, two firewalls are used. Firewall 1 and Firewall 2. These firewalls perform the encryption and decryption process itself. Network 1 is connected to the internet with its own firewall 1. Similarly, network 2 connects to the internet with its own firewall 2. Here firewalls are virtually connected to each other over the internet.

* Suppose, host A on network 1 wants to send a data packet to host B on network 2. The transmission of a data packet between this network is traveled as follows.

* First host A creates a packet and inserts its own IP address as the source address and the IP address of host B as the destination address. Then it sends the data packet using the appropriate mechanism.
* Data packet reaches firewall 1. Then firewall 1 adds the new headers to the packet. In these new headers, it changes the source IP address of the packet from that of host A to its own address. It also changes the destination IP address of the packet from that of host B to the IP address of firewall 2. It also performs encryption and authentication on packets depending on the settings. Then it sends the modified packet over the internet.
* Then packet reaches firewall 2 over the internet via routers. Firewall 2 then discards the outer header and performs decryption and encryption functions. This process results in the original packet that was created by host A in step 1 as we discussed above. Then it takes the content of the packet in plaintext form and realizes that the packet is meant for host B. Therefore it delivers the data packet to host B.

**Address Block: 192.168.0.0/16**
**Subnetting need to be implemented for assigning network to 5 different projects**

IP Address: 192.168.0.0 
Class C subnet mask : 255.255.0.0 or 11111111.11111111.00000000.00000000
Subnetting done for 5 projects or we can say 5 subnets are to be created so to find smallest subnet size that can accomodate atleast 5 networks is 

**2^n >= 5** 

So n = 3 so 3 bits from host id of subnet mask needs to set to 1. New subnet mask would be 

**11111111.11111111.11100000.00000000  or  255.255.224.0**

Number of network id 2^3 = 8 but we need only 5 for our projects
Number of host id per subnet 2^13 - 2 = 8190 addresses (2 are subtracted one for network address and another for broadcast address). So usable host id addresses per subnet are 8190. Increment of 8190 host ids per ip address.

Block size of third octate is calculated by 8192 / 256 = 32. So start of network range would be 192.168.0.0 to 192.168.31.255

**Project 1:**

Network Address: 192.168.0.0/19

Broadcast Address: 192.168.31.255/19

First Usable host address: 192.168.0.1/19

Last Usable Host address: 192.168.31.254/19

**Project 2:**

Network Address: 192.168.32.0/19

Broadcast Address: 192.168.63.255/19

First Usable host address: 192.168.32.1/19

Last Usable Host address: 192.168.63.254/19

**Project 3:**

Network Address: 192.168.64.0/19

Broadcast Address: 192.168.95.255/19

First Usable host address: 192.168.64.1/19

Last Usable Host address: 192.168.95.254/19

**Project 4:**

Network Address: 192.168.96.0/19

Broadcast Address: 192.168.127.255/19

First Usable host address: 192.168.96.1/19

Last Usable Host address: 192.168.127.254/19

**Project 5:**

Network Address: 192.168.128.0/19

Broadcast Address: 192.168.159.255/19

First Usable host address: 192.168.128.1/19

Last Usable Host address: 192.168.159.254/19

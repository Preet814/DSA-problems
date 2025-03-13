**IP Address:** 205.11.2.0

**Class C IP Address**

**What is the subnet mask for the maximum number of hosts?**

Our task is to create **30 subnets** for class C IP Address starting 24 bits are used for network id, now from remaining 8 bits for creating 30 subnets **5 bits** will be sufficient as 2^5 is 32 subnets.
Accordingly 24 bits from network id and 5 bits from host id leads to a subnet mask of **11111111.11111111.11111111.11111000** or **255.255.255.248**


**How many hosts can each subnet have?**

Now to calculate valid host for each subnet we have a formula: **2^(number of host bits left after subnet masking) - 2**. Here difference of 2 is taken because 2 id's are used one by Subnet id and another by Direct Broadcast id.
So number of host bits left are:
Total bits = 32
Bits used for subnetting = 29
Bits left for valid Hosts = 3 = number of host bits
so **(2^3) - 2 = 6** So **6 hosts available per subnet**


**What is the IP address of host 3 on subnet 2?**

Now to find the subnet numbers our subnet mask is **255.255.255.248**. First thing to note that our octate does not equal to 255 or 0, our octate is equal to 248. Secondly to get the range of subnet to ip address 205.11.2.0 using our subnet mask 255.255.255.248 formula is: **256 - (octate value)**.
So range is **256 - 248 = 8**
Our first subnet would be in range of **205.11.2.0 - 205.11.2.7**
Second subnet would be in range of **205.11.2.8 - 205.11.2.15**
Third subnet would be in range of **205.11.2.16 - 205.11.2.23**
So IP address of host 3 from subnet 2 would be:
subnet 2 - **205.11.2.8 to 205.11.2.15** 1st usable host is **205.11.2.9** So the third usable host is **205.11.2.11**



**Subnet Mask :** 255.255.255.248

**Number of valid hosts per subnet :** 6

**Host 3 on subnet 2 :** 205.11.2.11


# IP Address

We need to understand following three concepts to understand IP Address very well. When we take about IP Address, these 3 concepts go hand in hand.

- IP Address
- Subnet Mask
- Gateway

Let us see example of IP Address, Subnet Mask and Gateway

**IP Address:** 192.168.100.225 </br>
**Subnet Mask:** 255.255.255.0 </br>
**Gateway:** 192.168.100.1 </br>

## IP Address

An IP Address is consists of 4 octects each octet is devided by dot(.). An Octet is group of 8 bits. So IPv4 is 32 bits because 8 bits in each octel * 4 total octels in an IP address == 32 bits. The 8 bits in each octet is displayed as decimal number. 


If we convert above IP address in binary form, it will look like this: 11000000.10101000.01100100.11100001

IP Address can take 0 to 255 in each octet. If all the bits in the octet are 0's then its decimal number is 0. If all the bits in the octel are 1's then its decimal number is 255. So value from 00000000 to 11111111 is the range of octet. The number outside of this range is considered as invalid

## Subnet Mask

Each IP Address has two information. It has *network field* and *host field*. We can indentity network field and host field by *Subnet Mask*. The subnet mask will always be series of 1's and 0's. Transition from 1's to 0's happens at place where separets network and host part.

In above example, first 3 octets are from network part because first 3 octets are *255.255.255* in subnet mask where as last octet is host part because it has *0*. So in above IP Address *192.169.100* is network part and *255* is host part. So from *192.169.100.0* to *192.169.100.255* are total number of hosts in above example. 

    
## Gateway

Gateway is also called router. Any packet going out of current network, it goes via gatway

In above example, *192.168.100.1* is our gateway IP Address. Gateway IP needs to be in same network


## IPv4 Classes

IPv4 classes are identified by the first octal

***???***.xxx.xxx.xxx

| Class   | Range   |
|---------|---------|
| Class A | 1-126   |
| Class B | 128-191 |
| Class C | 192-223 |
| Class D | 224-239 |
| Class E | 240-255 |

- Class D is used for multicast
- Class E is reserved for experimental purpose
- Any IP starting from 127 is loop back IP Address

### Class C

Let us start with example of Class C

**IP Address:** 192.168.100.225<br>
**Subnet Mask:** 255.255.255.0<br>
**Gateway:** 192. 168.100.1<br>

Please note the IP Address in above example, its first octal is 192 which comes under Class C range. So this is Class C IP Address. This IP Address can be written as 192.168.100.225/24 in cidr notation because 24 bits are represented as network part.

**Network ID(First):** 192.168.100.0 </br>
**Broadcard ID(Last):** 192.168.100.255


The total number of host = 2^8-2 = 254. We are subtracting 2 because of Network ID and Broadcast ID are taken from host IP range. The valid IP Address range from 192.168.100.1 to 192.168.100.254


### Class B

Let us see the example of Class C

**IP Address:** 172.123.100.225<br>
**Subnet Mask:** 255.255.0.0<br>
**Gateway:** 172.123.1.225<br>

Please note the IP Address in above example, its first octal is 172 which comes under Class B range. So this is Class B IP Address. This IP Address can be written as 172.123.100.225/16 in cidr notation because 16 bits are represented as network part.

**Network ID(First):** 172.123.0.0 </br>
**Broadcard ID(Last):** 172.123.255.255


The total number of host = 2^16-2 = 65534. We are subtracting 2 because of Network ID and Broadcast ID are taken from host IP range. The valid IP Address range from 172.123.0.1 to 172.123.255.254


### Class A

Let us see the example of Class A

**IP Address:** 100.228.111.225<br>
**Subnet Mask:** 255.0.0.0<br>
**Gateway:** 100.101.123.1<br>

Please note the IP Address in above example, its first octal is 100 which comes under Class A range. So this is Class A IP Address. This IP Address can be written as 100.228.111.225/8 in cidr notation because 8 bits are represented as network part.

**Network ID(First):** 100.0.0.0 </br>
**Broadcard ID(Last):** 100.255.255.255


The total number of host = 2^24-2 = 2097150. We are subtracting 2 because of Network ID and Broadcast ID are taken from host IP range. The valid IP Address range from 100.0.0.1 to 172.255.255.254


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

- An IP Address is consists of 4 octects each octet is devided by dot(.)
    - An Octet is group of 8 bits.
    - So IPv4 is 32 bits because 8 bits in each octel * 4 total octels in an IP address == 32 bits
    - 8 bits in each octet is displayed as decimal number. 
- If we convert above IP address in binary form, it will look like this: 11000000.10101000.01100100.11100000
- 


## Subnet Mask

## Gateway

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

#### Example

**IP Address:** 192.168.100.225<br>
**Subnet Mask:** 255.255.255.0<br>
**Gateway:** 192. 168.100.1<br>

- Please note the IP Address in above example, it's first octal is 192 which comes under Class C range. So this is Class C IP Address.




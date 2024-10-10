# Internet

- The Internet is a collection of networks containing small and large networks of different types.
- It was introduced by Tim Berners-Lee in 1989 with the introduction of the World Wide Web.
- It works on the basics of one of the first network models introduced by the US military, ARPANET.

# IP Address

- An IP address is defined as an address that is assigned when a device is connected to the internet.
- It can be of 2 types:
  1. **Public**: A public IP is unique for each device on the internet. It is assigned by Internet Service Providers (ISPs) to devices like routers, servers, or any device communicating directly with the internet.
  2. **Private**: A private IP is assigned to a device in a private network. These IPs are not directly routable on the internet. Instead, these devices connect to the outside world using a public IP. Examples include devices like PCs, laptops, smartphones, etc.

- The following ranges are reserved for private IP addresses:
  - `10.0.0.0` to `10.255.255.255`
  - `172.16.0.0` to `172.31.255.255`
  - `192.168.0.0` to `192.168.255.255`

## IPv4
- It is one of the core protocols of the IP suite.
- It is made up of 32 bits.
- These 32 bits are divided into 4 octets, where the value of each octet lies between 0-255.
- The IPv4 address space can be subdivided into smaller segments called subnets, allowing for efficient IP address management.

- There are 5 classes in IPv4:

1. **Class A**: 
   - **Range**: `1.0.0.0` to `126.255.255.255`
   - **First Bit**: Always `0`
   - **Default Subnet Mask**: `255.0.0.0`
   - **Number of Networks**: 128
   - **Total Number of Hosts** (excluding broadcasting): 16 million
   - **Usage**: Typically used for very large networks.

2. **Class B**: 
   - **Range**: `128.0.0.0` to `191.255.255.255`
   - **First 2 Bits**: `1` and `0`
   - **Subnet Mask**: `255.255.0.0`
   - **Number of Networks**: 16,384
   - **Number of Hosts per Network**: 65,534
   - **Usage**: Mainly used for medium to large-sized networks.

3. **Class C**: 
   - **Range**: `192.0.0.0` to `223.255.255.255`
   - **First 3 Bits**: Always `1, 1, 0`
   - **Subnet Mask**: `255.255.255.0`
   - **Total Number of Networks**: More than 2 million
   - **Hosts per Network**: 254
   - **Usage**: Used for small to medium-sized networks.

4. **Class D**: 
   - **Range**: `224.0.0.0` to `239.255.255.255`
   - **First 4 Bits**: `1, 1, 1, 0`
   - **Usage**: Used to send data to multiple receivers at the same time (multicast).

5. **Class E**: 
   - **Range**: `240.0.0.0` to `255.255.255.255`
   - **First 4 Bits**: `1, 1, 1, 1`
   - **Usage**: Reserved for experimental purposes and future use.

### Note
- The last address in all networks is preserved for broadcasting purposes. Any packet sent to this address will be broadcasted to all other hosts on the same network (usually ending in `.255`).

## Loopback Addresses
- **Range**: `127.0.0.0` to `127.255.255.255`
- **Usage**: Reserved for loopback, allowing a device to communicate with itself.
- **Purpose**: Used for troubleshooting and testing if IP/TCP is functioning properly.
- **Security**: Packets sent to this network are never routed to an external network, enhancing security.

## Special Addresses
- **0.0.0.0**: Used as an invalid IP address or represents the default route for routers.
- **Usage**: Addresses in the `0.0.0.0` to `0.255.255.255` range are not routable on the public internet. They are meant for internal use within networks or for special administrative functions, ensuring that they do not interfere with global addressing schemes.

## Subnetting
- Subnetting is the process of dividing a large IP network into smaller, more manageable networks.
- It helps organize the network into more manageable forms.
- Each subnet is divided into two parts: the network part and the host part.
- A subnet mask determines which portion is the network and which is the host.
- For example :- The subnet mask of class A is 255.0.0.0. which means that the first octet is consumed for network selection and rest of them which contain zero are used for hosts on each network.

## IPv6

- IPv6 is totally different from IPv4.
- It is a 128 bits address, making 16 bytes, divided into 8 portions known as hextets.
- Each portion is 4 bits long.
- Instead of using dot notations, we use : in IPv6 addresses.
- It uses something known as SLAAC to shorten the IP address.
- The rules for shortening are simple, we can emit the leading zeroes in any hextetx.
- Rule no 2 is we can remove the whole continous section containg zeros by using :: but the ommision can be performed only once.
- We can do unicast, multicast and anycast in IPv6.
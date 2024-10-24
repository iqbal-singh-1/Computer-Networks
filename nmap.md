# What is NMAP??

- **Nmap** is a powerful tool designed for network analysis and security audits.
- While it can be dangerous in the hands of malicious users, it is also incredibly beneficial for cybersecurity professionals.
- Nmap performs a variety of operations to gather extensive information about a host machine, including:
  - The operating system in use
  - The status of the host (online or offline)
  - Open port scanning
  - Firewall types in place
  - Services running on open ports, among other details.
- Cybercriminals may use this tool to gather critical information about their targets, highlighting the importance of understanding its capabilities.
- Additionally, security auditors leverage Nmap to identify vulnerabilities and effectively manage network security.

## Performing network analysis using nmap

- `nmap < ip >` :- running this command checks for a lot of information about the IP like host discovery, OS detection, open ports available on the system, services running on the system and so on.
- `nmap < ip >` :- takes an aggressive scan of the host and provide all the necessary information.
- `nmap -sn < ip >` :- it is used to scan a network IP to check whether the host is online or not. Basically, this command sends a ping request to the IP address and focuses only on host discovery, it shows that the given host is online.
- `nmap < ip > -PR` :- the -PR option is used to send an ARP packet to the host machine to check connectivity with the host device and to get its MAC address. It is normally used when the host has turned on its firewall and is not accepting tcp/ip packets.
- `nmap -sn --traceroute` :- this feautre can be used to determine the path followed by the packet to a particular IP address or the host machine. IT shows how many routers did the packet crossed before reaching to the destination.
- `nmap -sn --dns-servers <server-IP>` :- it can be used to change the dns server through which we are trying to send packets.
- `nmap -n` :- skips the name resolution and directly goto the site. 
- `nmap -Pn` :- turns off ping signal and assume that the host is online.
- `nmap -p` :- looks for whether the specific port/ports are open or not.
- `nmap -p-` :- scans all ports of the ip.
- `nmap -sT` :- scans for all the TCP ports only not udp.
- `nmap -sU` :- scans for all the UDP ports.

## Host discovery
- One of the basic use of nmap is to do host discovery. It is very important in cyber.
- It can be used to filter out the large number of IPs to a relatively small number.
- Nmap offers a variety of options for host discovery.

1. **using -iL**
  - Suppose that we want to scan a number of IP addresses on a network. Typing all the IPs on the command line will look very messy and will make the command line awkward.
  - So to escape this situation, we can use `-iL` suffix with nmap.
  - All we have to do is create a file and throw bunch of IPs to be scanned in the file.
  - Now, all we have to do is specify the file name with -iL suffix and it will automatically detect the IPs to be scanned.
  - File may contain CIDR notations, normal IPs, DNS or any other format recognized by nmap.

2. **using -iR** 
  - This is basically used when we want to choose our targets at random from a number of IPs that are provided to it.
  - It usually skips IPs like those in private networks, multicasting etc.
  - nmap -sS -PS80 -iR 0 -p 80 is the command we are lokking for.

3. **excluding targets**
  - --exclude or --excludefile command is used along with nmap to skip some kind of hosts that we do not want to be scanned. Reasons for not scanning an IP could be numerous and the command we are looking for is this only.

## Finding IPs of an organisation
- IP finding can be very useful for an organisation.
- Here are some tricks to find an IP address.

1. **Using DNS** 
  - DNS of a company can be dissolved to gather information about different servers the company is using.
  - To get this info, we can use two commands :- `host` or `dig`.
  - Host command is used to send a DNS query to the DNS server and corresponding info is delivered to the user.
  - Ex:- `host -t ns target.com` , here, -t is used to specify the type of record we are searching for, which in this case is "name server" (ns).
  - Dig command shows more detailed info about the target.

2. **Routing**
  - Routing protocols like BGP can be used to get the routing tables which can provide a lot of info like packet path, IP of sender and reciever
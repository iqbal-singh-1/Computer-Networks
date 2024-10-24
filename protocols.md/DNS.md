# DNS
- Domain Name System or DNS refers to collection of records of all the IPs present over the internet.
- You can think of it as a diary that contains contact information of different people.
- When a request is made to web browser for a particular wesite or webpage, it is the DNS which points us to particular IP on the internet.
- Due to DNS, there is no need to remember the IP address of each site.

## How it works???
- Let's assume that the domain we are searching for is "www.sample.com"
- Firstly when we are looking for this domain, we will encounter a Root DNS server.
- This root server does not hold the information about what our domain. However, what it does know is some other DNS servers which can provide some info about the searched domain.
- So now our query is forwarded to a "Top Level Domain(TLD)". These servers usually search for the last word in our domain name. For ex:- In our choosen domain "www.sample.com" , TLD looks for servers that unserstands ".com".
- Now, the next step is to look for SLD or "Second Level Domain". SLD will look for "sample" and forward the request to "Third Level Domain or Sub-domain" in case a sub-domain exists.
- Finally, the IP address is found and it can be send to the user requesting it.
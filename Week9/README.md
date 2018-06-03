Lab

Milestone 0

Network Config
![0](https://user-images.githubusercontent.com/37943892/40754059-0f8a0442-642c-11e8-8ea2-e68b54af30ba.PNG)

Ping
![ping](https://user-images.githubusercontent.com/37943892/40754093-431d2a96-642c-11e8-9135-05520bc49f45.PNG)

Nslookup
![nslookup](https://user-images.githubusercontent.com/37943892/40754331-b301104c-642d-11e8-8b13-6765608a01bb.PNG)

Traceroute
![tracert](https://user-images.githubusercontent.com/37943892/40754671-3f7ea34e-642f-11e8-8deb-f950c5c70acb.PNG)
Only the first 3 hops are the same 
Codepath has 12 hops compared to google with 7

Telnet
One thing that makes telnet insecure is that it send packets in plaintext, which could be easily intercepted by a hacker sniffing the network
![telnet](https://user-images.githubusercontent.com/37943892/40814132-4bf4e51a-64f3-11e8-9b5a-f02c27b0f8f0.PNG)

Curl and Wget
Wget lets you download files from http/https and ftp servers and builds the request automatically
curl allows you to build the request as you wish and supports more protocols compared to wget
wget supports recursive downloading
curl is more likely to be found on a Linux OS
Syntax for downloading a file "curl -0 [url]

SSH and SCP
Key authentication is harder to crack and stored on your computer. It also doesn't have to be rememberd by the user
Passwords on the other hand, are easy to forget and crack
scp /path/to/source-file user@host:/path/to/destination-folder/

Milestone 1
![nmap](https://user-images.githubusercontent.com/37943892/40814789-4d669c5a-64f7-11e8-854d-98369e723f3c.PNG)

Milestone 2
Challenge 1
codepath tcpdump
![tcpdump](https://user-images.githubusercontent.com/37943892/40815630-9dc650d2-64fc-11e8-9130-c221d76c2bc7.PNG)
225 requests and most of the content were javacripts and png images

security.codepath.com tcpdump
![codepath tcp](https://user-images.githubusercontent.com/37943892/40815802-d5946444-64fd-11e8-96b6-71f635dd9575.PNG)
There are less packets dumped. The difference is that there aren't as many things loaded onto the securit codepath pages as the codepath website

Challenge 2
![challenge 2](https://user-images.githubusercontent.com/37943892/40815930-c771ecfa-64fe-11e8-98e7-1e687d326f8a.PNG)

Milestone 3
![wireshark](https://user-images.githubusercontent.com/37943892/40817068-3446b35a-6505-11e8-9ef9-ba3a2e6c0ecc.PNG)
Half the traffic is inbound and half is outbound
 
nslookup
![wireshark 2](https://user-images.githubusercontent.com/37943892/40817200-ffeba77c-6505-11e8-85a1-c72746c46120.PNG)

ARP
![wireshark 3](https://user-images.githubusercontent.com/37943892/40817239-379049b2-6506-11e8-9052-fefcfad331c6.PNG)

Milestone 4
The purpose of checkip.dyndns.org is to check your current IP address
The 3 jpeg reuqests are from the website with the malware imbedded in the pictures. 
The malware was embedded in the email attachment that was sent to mike. He opened it up and it was injected into his computer
 
Milestone 5
executable malware
![milestone 5](https://user-images.githubusercontent.com/37943892/40881799-69c40bf0-6685-11e8-8535-782164f28747.PNG)
 
Milestone 6
![milstone 6](https://user-images.githubusercontent.com/37943892/40881576-8cc1c63a-667e-11e8-9e9e-727b27c1e23e.PNG)

Milestone 7 
![protocol](https://user-images.githubusercontent.com/37943892/40881650-e0e2c87a-6680-11e8-800c-87c8d7c5dbe1.PNG)
![ssid](https://user-images.githubusercontent.com/37943892/40881658-1557c808-6681-11e8-8939-4123f83ee410.PNG)
![hash](https://user-images.githubusercontent.com/37943892/40881745-cbfbd138-6683-11e8-9279-457bb33dd766.PNG)
A nonce is a number generated and used once for session authentication

Assignments
Milestone 0
![milestone 0](https://user-images.githubusercontent.com/37943892/40677573-e6f39574-6332-11e8-941c-a6afd80b0117.PNG)

Milestone 1
![milestone 1](https://user-images.githubusercontent.com/37943892/40696221-caa1043c-6379-11e8-9161-0450aea0e12f.PNG)

Milestone 2
![milestone 2](https://user-images.githubusercontent.com/37943892/40696266-0396a7d8-637a-11e8-8b4b-a233279ad8d0.PNG)

Milestone 3
![milestone 3](https://user-images.githubusercontent.com/37943892/40696749-f2c3d9e2-637b-11e8-8649-aaab0a34d1c4.PNG)

Milestone 4
For this milestone I was not able to access the admin console. 
Whenever I would try to install the MHN admin application using the sudo ./install.sh command this would pop up
![mhn](https://user-images.githubusercontent.com/37943892/40881339-b9d680e4-6678-11e8-8ff7-519529abf747.PNG)
I typed in the same username and password I created but it would not let me have access. I've also tried redoing everything on a new computer with a new email and it would prompt the exact same result. It never asked me to choose a new email or password like they're suppose to in milestone 2 but instead asked me to log in right away.
![mhn](https://user-images.githubusercontent.com/37943892/40881367-951bcec0-6679-11e8-9d61-6ad80b01556e.JPG)
Because of this I was not able to do milestone 5

Concept Review
1) A packet is a small bit data sent form a source IP to a destination IP
2) You can find the protocols they're using, IP addresses, and the data being sent 
3) yes you can make it publicly accessible and invisible using certain configurations
4) It can give the attacker data about how the traffic is flowing through the network. From here he can find vulnerabilities in the network and launch his attack from there
5) Information of the vulnerabilities found can be used to patch it up. This will prevent future attacks coming from this vector
6) Sniffing is analyzing the packets that are going thorugh the network
7) Special privileges are required to allow tcpdump and wireshark to read packet information
8) nencrypted wifi network allows hackers to access the network with full view of everything that is going on. Hackers can get into the network easily and embed malware, destroy data, and steal information
9) SSL(secure socket layer) is a protocol that allows encrypted communication between two networks. TLS(transport layer protocol) is a more updated and secure version of SSL



**1. 주소 해결 프로토콜의 기능을 설명하는 문장은 무엇입니까?**  
  
- ARP는 로컬 네트워크에서 호스트의 IP 주소를 검색하는 데 사용됩니다.  
- ARP는 로컬 네트워크의 모든 호스트의 MAC 주소를 검색하는 데 사용됩니다.  ✅
- ARP는 다른 네트워크에 있는 모든 호스트의 MAC 주소를 검색하는 데 사용됩니다.  
- ARP는 다른 네트워크에서 호스트의 IP 주소를 검색하는 데 사용됩니다.


**2. 전시를 참조하세요. R1에서 서버 B로 이동할 프레임을 구성할 때 R1은 목적지의 MAC 주소로 무엇을 사용하나요?**  
![Networking Devices and Initial Configuration Module 7 - 9 Checkpoint Exam Q2](https://itexamanswers.net/wp-content/uploads/2015/05/i215038v1n1_215038.jpg)

- IPv4 주소에 해당하는 대상 MAC 주소가 ARP 캐시에 없는 경우 R1은 ARP 요청을 보냅니다.  ✅
- 패킷은 PPP 프레임에 캡슐화되고 R1은 프레임에 PPP 목적지 주소를 추가합니다.  
- R1은 필드를 비워두고 데이터를 PC로 전달합니다.  
- R1은 S1의 목적지 MAC 주소를 사용합니다.


**3. 알려진 논리 주소에서 물리적 주소를 검색하는 데 사용되는 프로토콜은 무엇이며 어떤 메시지 유형을 사용하나요?**

- PING, broadcast
- DNS, unicast
- DNS, broadcast
- PING, multicast
- ARP, multicast
- ARP, broadcast ✅


**4. 컴퓨터가 처음으로 다른 컴퓨터에 핑을 보낼 때, 다른 장치의 MAC 주소를 결정하기 위해 네트워크에 어떤 유형의 메시지를 표시하나요?**  
  
- 로컬 네트워크에 연결된 모든 레이어 3 장치에 대한 멀티캐스트  
- RFI(정보 요청) 메시지  
- ARP 요청 ✅  
- ICMP 핑


**5. 사용자가 원격 네트워크의 웹 서버에 HTTP 요청을 보냅니다. 이 요청을 캡슐화하는 동안 프레임의 주소 필드에 목적지를 표시하기 위해 어떤 정보가 추가되나요?**

- 기본 게이트웨이의 IP 주소  
- 대상 호스트의 MAC 주소  
- 대상 호스트의 네트워크 도메인  
- 기본 게이트웨이의 MAC 주소 ✅


**6. 전시를 참조하세요. PC1이 PC3로 패킷을 전송하려는 경우 ARP 요청에 응답할 장치의 IP 주소는 다음과 같습니다**

![Networking Devices and Initial Configuration Module 7 - 9 Checkpoint Exam Q6](https://itexamanswers.net/wp-content/uploads/2022/07/2022-07-24_152556.jpg)

- 192.168.1.2
- 192.168.1.254
- 192.168.0.1 ✅
- 192.168.0.3
- 192.168.0.2
- 192.168.0.254
- 192.168.1.1

**Explanation:** When a network device has to communicate with a device on another network, it broadcasts an ARP request asking for the default gateway MAC address. The default gateway (RT1) unicasts an ARP reply with the Fa0/0 MAC address.

**7. What are two problems that can be caused by a large number of ARP request and reply messages? (Choose two.)**

- The ARP request is sent as a broadcast, and will flood the entire subnet. ✅
- The network may become overloaded because ARP reply messages have a very large payload due to the 48-bit MAC address and 32-bit IP address that they contain.
- Switches become overloaded because they concentrate all the traffic from the attached subnets.
- All ARP request messages must be processed by all nodes on the local network. ✅
- A large number of ARP request and reply messages may slow down the switching process, leading the switch to make many changes in its MAC table.

**Explanation:** ARP requests are sent as broadcasts:  
(1) All nodes will receive them, and they will be processed by software, interrupting the CPU.  
(2) The switch forwards (floods) Layer 2 broadcasts to all ports.

A switch does not change its MAC table based on ARP request or reply messages. The switch populates the MAC table using the source MAC address of all frames. The ARP payload is very small and does not overload the switch.

**8. A user reports that the corporate web server cannot be accessed. A technician verifies that the web server can be accessed by its IP address. What are two possible causes of the problem? (Choose two.)**

- The network connection is down.
- The default gateway address is misconfigured on the workstation.
- The DNS server address is misconfigured on the workstation. ✅
- The web server is misconfigured.
- The web server information is misconfigured on the DNS server. ✅

**Explanation:** The fact that the web server can be accessed by its IP address indicates that the web server is working and there is connectivity between the workstation and the web server. However, the web server domain name is not resolving correctly to its IP address. This could be caused by a misconfiguration of the DNS server IP address on the workstation or the wrong entry of the web server in the DNS server.

**9. Which DHCP IPv4 message contains the following information?**  
**Destination address: 255.255.255.255**  
**Client IPv4 address: 0.0.0.0**  
**Default gateway address: 0.0.0.0**  
**Subnet mask: 0.0.0.0**

- DHCPREQUEST
- DHCPACK
- DHCPDISCOVER ✅
- DHCPOFFER

**Explanation:** A client will first send the DHCPDISCOVER broadcast message to find DHCPv4 servers on the network. This message will have the limited broadcast address, 255.255.255.255, as the destination address. The client IPv4 address, the default gateway address, and subnet fields will all be 0.0.0.0 because these have not yet been configured on the client. When the DHCPv4 server receives a DHCPDISCOVER message, it reserves an available IPv4 address to lease to the client and sends the unicast DHCPOFFER message to the requesting client. When the client receives the DHCPOFFER from the server, it sends back a DHCPREQUEST broadcast message. On receiving the DHCPREQUEST message, the server replies with a unicast DHCPACK message.

**10. Which two commands could be used to check if DNS name resolution is working properly on a Windows PC? (Choose two.)**

- nbtstat cisco.com
- net cisco.com
- ping cisco.com ✅
- ipconfig /flushdns
- nslookup cisco.com ✅

**Explanation:** The ping command tests the connection between two hosts. When ping uses a host domain name to test the connection, the resolver on the PC will first perform the name resolution to query the DNS server for the IP address of the host. If the ping command is unable to resolve the domain name to an IP address, an error will result.

Nslookup is a tool for testing and troubleshooting DNS servers.

**11. Which three statements describe a DHCP Discover message? (Choose three.)**

- Only the DHCP server receives the message.
- The message comes from a client seeking an IP address. ✅
- The source MAC address is 48 ones (FF-FF-FF-FF-FF-FF).
- The message comes from a server offering an IP address.
- All hosts receive the message, but only a DHCP server replies. ✅
- The destination IP address is 255.255.255.255. ✅

**Explanation:** When a host configured to use DHCP powers up on a network it sends a DHCPDISCOVER message. FF-FF-FF-FF-FF-FF is the L2 broadcast address. A DHCP server replies with a unicast DHCPOFFER message back to the host.

**12. What IPv4-related DNS record type is used by a DNS server in response to a host requesting for a web server address via the URL?**

- NS record
- A record ✅
- MX record
- AAAA record

**Explanation:** A DNS server uses an A record type for an IPv4 end device address. The AAAA record is for an IPv6 end device address. The MX record is used to map the domain name to mail exchange servers. The NS record indicates the authoritative name server.

**13. Which two tasks can be performed by a local DNS server? (Choose two.)**

- retrieving email messages
- providing IP addresses to local hosts
- mapping name-to-IP addresses for internal hosts ✅
- forwarding name resolution requests between servers ✅
- allowing data transfer between two network devices

**Explanation:** Two important functions of DNS are to (1) provide IP addresses for domain names such as www.cisco.com, and (2) forward requests that cannot be resolved to other servers in order to provide domain name to IP address translation. DHCP provides IP addressing information to local devices. A file transfer protocol such as FTP, SFTP, or TFTP provides file sharing services. IMAP or POP can be used to retrieve an email message from a server.

**14. A DHCP configured PC boots up. What is the order of the messages that are sent and received by this PC in order to obtain an appropriate IP address?**

- DHCPOFFER, DHCPDISCOVER, DHCPREQUEST, DHCPACK​
- DHCPDISCOVER, DHCPOFFER, DHCPREQUEST, DHCPACK​ ✅
- DHCPDISCOVER, DHCPREQUEST, DHCPOFFER, DHCPACK​
- DHCPREQUEST, DHCPOFFER, DHCPDISCOVER, DHCPACK​

**Explanation:** During the boot process, the PC starts by broadcasting a DHCPDISCOVER message to request an available IP address. A DHCP server replies with a DHCPOFFER message, which offers a lease to the device. This message contains the IP address and other information. The PC may receive multiple DHCPOFFER messages if there is more than one DHCP server. In this case, the PC must choose one of the server DHCP offerings. The PC broadcasts a DHCPREQUEST message that identifies the explicit server and lease offer that the PC is accepting. Then the server will return a DHCPACK message that acknowledges to the PC that the lease is finalized.

**15. Refer to the exhibit. Host A and the file server have established a TCP session to exchange data. What acknowledgement number will the file server send to host A to acknowledge receipt of the first three segments of data?**

![Networking Devices and Initial Configuration Module 7 - 9 Checkpoint Exam 15](https://itexamanswers.net/wp-content/uploads/2022/07/2022-07-24_152712.jpg)

Networking Devices and Initial Configuration Module 7 – 9 Checkpoint Exam Q15

- 3000
- 1002
- 3001 ✅
- 4000
- 1000

**Explanation:** The file server will send back an acknowledgement number of 3001 to host A after receiving the first three segments. The starting sequence number was 1. 1000 bytes were sent in each of the three segments for a total of 3000 bytes. Because the initial sequence number was 1, the last byte sent was byte number 3000. The file server will now expect to receive byte number 3001 and above. Therefore, it communicates to host A through the acknowledgement number of 3001.

**16. A host device needs to send a large video file across the network while providing data communication to other users. Which feature will allow different communication streams to occur at the same time, without having a single data stream using all available bandwidth?**

- port numbers
- multiplexing ✅
- acknowledgments
- window size

**Explanation:** Multiplexing is useful for interleaving multiple communication streams. Window size is used to slow down the rate of data communication. Port numbers are used to pass data streams to their proper applications. Acknowledgments are used to notify a sending device that a stream of data packets has or has not been received.

**17. What does a client application select for a TCP or UDP source port number?**

- a random value in the range of the registered ports ✅
- a random value in the well-known port range
- a predefined value in the well-known port range
- a predefined value in the range of the registered ports

**Explanation:** The client randomly selects an available source port in the range of the registered ports.

**18. A client is establishing a TCP session with a server. How is the acknowledgment number in the response segment to the client determined?**

- The acknowledgment number is set to 11 to signify an acknowledgment packet and synchronization packet back to the client.
- The acknowledgment number field uses a random source port number in response to the client.
- The acknowledgment number field is modified by adding 1 to the randomly chosen initial sequence number in response to the client. ✅
- The acknowledgment number is set to 1 to signify an acknowledgment packet back to the client.

**Explanation:** To establish a session with the client, the TCP server will acknowledge the receipt of the SYN segment from the client. The server sends a segment back to the client with the ACK flag set indicating that the acknowledgment number is significant.The value of the acknowledgment number field is equal to the randomly chosen initial sequence number (ISN) plus 1.

**19. Which two TCP header fields are used to confirm receipt of data? (Choose two.)**

- checksum
- acknowledgment number ✅
- sequence number ✅
- preamble
- FCS

**Explanation:** Together the TCP sequence number and acknowledgment number fields are used by the receiver to inform the sender of the bytes of data that the receiver has accepted.

**20. What is a socket?**

- the combination of the source and destination IP address and source and destination Ethernet address
- the combination of a source IP address and port number or a destination IP address and port number ✅
- the combination of the source and destination sequence and acknowledgment numbers
- the combination of the source and destination sequence numbers and port numbers

**Explanation:** A socket is a combination of the source IP address and source port or the destination IP address and the destination port number.

**21. What TCP mechanism is used to enhance performance by allowing a device to continuously send a steady stream of segments as long as the device is also receiving necessary acknowledgements?**

- socket pair
- sliding window ✅
- three-way handshake
- two-way handshake

**Explanation:** TCP uses windows to attempt to manage the rate of transmission to the maximum flow that the network and destination device can support while minimizing loss and retransmissions. When overwhelmed with data, the destination can send a request to reduce the of the window. The process of the destination sending acknowledgments as it processes bytes received and the continual adjustment of the source send window is known as sliding windows.

**22. Refer to the exhibit. PC1 issues an ARP request because it needs to send a packet to PC3. In this scenario, what will happen next?**  
![](https://itexamanswers.net/wp-content/uploads/2020/10/2020-10-26_082551.jpg)

- RT1 will send an ARP reply with its own Fa0/1 MAC address.
- SW1 will send an ARP reply with its Fa0/1 MAC address.
- RT1 will send an ARP reply with the PC3 MAC address.
- RT1 will forward the ARP request to PC3.
- RT1 will send an ARP reply with its own Fa0/0 MAC address. ✅

**Explanation:** When a network device has to communicate with a device on another network, it broadcasts an ARP request asking for the default gateway MAC address. The default gateway (RT1) unicasts an ARP reply with the Fa0/0 MAC address.

**23. Refer to the exhibit. What does the value of the window size specify?**  
![](https://itexamanswers.net/wp-content/uploads/2020/05/2_i206128v1n1_206128-1.jpg)

- the amount of data that can be sent at one time
- the amount of data that can be sent before an acknowledgment is required ✅
- the total number of bits received during this TCP session
- a random number that is used in establishing a connection with the 3-way handshake

**Explanation:** The window size determines the number of bytes that can be sent before expecting an acknowledgment. The acknowledgment number is the number of the next expected byte.
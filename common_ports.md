# Common Ports and Protocols Cheat Sheet
The following tables cover services (and malware) that use common TCP ports and some UDP or SCTP ports.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Well-known/System Ports: 0 – 1023
| Port Number | Service Name               | Transport Protocol         | Description                                                                                                     |
|-------------|----------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------|
| 7           | Echo                       | TCP, UDP                   | Echo service                                                                                                   |
| 19          | CHARGEN                    | TCP, UDP                   | Character Generator Protocol, has severe vulnerabilities and thus is rarely used nowadays                     |
| 20          | FTP-data                   | TCP, SCTP                  | File Transfer Protocol data transfer                                                                           |
| 21          | FTP                        | TCP, UDP, SCTP             | File Transfer Protocol command control                                                                         |
| 22          | SSH/SCP/SFTP               | TCP, UDP, SCTP             | Secure Shell, secure logins, file transfers (`scp, sftp`), and port forwarding                                 |
| 23          | Telnet                     | TCP                        | Telnet protocol, for unencrypted text communications                                                          |
| 25          | SMTP                       | TCP                        | Simple Mail Transfer Protocol, used for email routing between mail servers                                     |
| 42          | WINS Replication           | TCP, UDP                   | Microsoft Windows Internet Name Service, vulnerable to attacks on a local network                             |
| 43          | WHOIS                      | TCP, UDP                   | Whois service, provides domain-level information                                                               |
| 49          | TACACS                     | UDP; can also use TCP      | Terminal Access Controller Access-Control System, provides remote authentication and related services          |
| 53          | DNS                        | TCP, UDP                   | Domain Name System name resolver                                                                               |
| 67          | DHCP/BOOTP                 | UDP                        | Dynamic Host Configuration Protocol and its predecessor Bootstrap Protocol Server; server port                 |
| 68          | DHCP/BOOTP                 | UDP                        | Dynamic Host Configuration Protocol and its predecessor Bootstrap Protocol Server; client port                 |
| 69          | TFTP                       | UDP                        | Trivial File Transfer Protocol                                                                                 |
| 70          | Gopher                     | TCP                        | Gopher is a communication protocol for distributing, searching, and retrieving documents in IP networks        |
| 79          | Finger                     | TCP                        | Name/Finger protocol and Finger user information protocol                                                      |
| 80          | HTTP                       | TCP, UDP, SCTP             | Hypertext Transfer Protocol (HTTP) versions 1.x and 2 use TCP; HTTP/3 uses QUIC over UDP                       |
| 88          | Kerberos                   | TCP, UDP                   | Network authentication system                                                                                  |
| 102         | Microsoft Exchange ISO-TSAP| TCP                        | Microsoft Exchange ISO Transport Service Access Point (TSAP) Class 0 protocol                                  |
| 110         | POP3                       | TCP                        | Post Office Protocol, version 3 (POP3)                                                                         |
| 113         | Ident                      | TCP                        | Identification Protocol, for identifying the user of a particular TCP connection                               |
| 119         | NNTP (Usenet)              | TCP                        | Network News Transfer Protocol                                                                                 |
| 123         | NTP                        | UDP                        | Network Time Protocol                                                                                           |
| 135         | Microsoft RPC EPMAP        | TCP, UDP                   | Microsoft Remote Procedure Call (RPC) Endpoint Mapper (EPMAP) service                                         |
| 137         | NetBIOS-ns                 | TCP, UDP                   | NetBIOS Name Service, used for name registration and resolution                                                |
| 138         | NetBIOS-dgm                | TCP, UDP                   | NetBIOS Datagram Service, used for providing access to shared resources                                       |
| 139         | NetBIOS-ssn                | TCP, UDP                   | NetBIOS Session Service                                                                                         |
| 143         | IMAP                       | TCP, UDP                   | Internet Message Access Protocol (IMAP), management of email messages on a server                              |
| 161         | SNMP-agents (unencrypted)  | UDP                        | Simple network management protocol; agents communicate on this port                                            |
| 162         | SNMP-trap (unencrypted)    | UDP                        | Simple network management protocol; listens for asynchronous traps                                             |
| 177         | XDMCP                      | UDP                        | X Display Manager Control Protocol                                                                             |
| 179         | BGP                        | TCP                        | Border Gateway Protocol                                                                                        |
| 194         | IRC                        | UDP                        | Internet Relay Chat                                                                                            |
| 201         | AppleTalk                  | TCP, UDP                   | AppleTalk Routing Maintenance. Trojan horses and viruses have used UDP port 201                               |
| 264         | BGMP                       | TCP, UDP                   | Border Gateway Multicast Protocol                                                                              |
| 318         | TSP                        | TCP, UDP                   | Time Stamp Protocol                                                                                            |
| 381         | HP Openview                | TCP, UDP                   | HP performance data collector                                                                                  |
| 383         | HP Openview                | TCP, UDP                   | HP data alarm manager                                                                                          |
| 389         | LDAP                       | TCP, UDP                   | Lightweight directory access protocol                                                                          |
| 411         | (Multiple uses)            | TCP, UDP                   | Direct Connect Hub, Remote MT Protocol                                                                         |
| 412         | (Multiple uses)            | TCP, UDP                   | Direct Connect Client-to-Client, Trap Convention Port                                                          |
| 427         | SLP                        | TCP                        | Service Location Protocol                                                                                       |
| 443         | HTTPS (HTTP over SSL)      | TCP, UDP, SCTP             | Hypertext Transfer Protocol Secure (HTTPS) versions 1.x and 2 use TCP; HTTP/3 uses QUIC over UDP               |
| 445         | Microsoft DS SMB           | TCP, UDP                   | Microsoft Directory Services                                                                                   |
| 464         | Kerberos                   | TCP, UDP                   | For password settings on Kerberos                                                                              |
| 465         | SMTP over TLS/SSL, SSM     | TCP                        | Authenticated SMTP over TLS/SSL (SMTPS)                                                                        |
| 497         | Dantz Retrospect           | TCP, UDP                   | A software suite for backing up operating systems                                                              |
| 500         | IPSec / ISAKMP / IKE       | UDP                        | Internet Protocol Security / Internet Security Association and Key Management Protocol / Internet Key Exchange |
| 512         | rexec                      | TCP                        | Remote Process Execution                                                                                       |
| 513         | rlogin                     | TCP                        | The Unix program `rlogin` allows users to log in on another host using a network                               |
| 514         | syslog                     | UDP                        | Syslog Protocol, for collecting and organizing all of the log files sent from the various devices on a network |
| 515         | LPD/LPR                    | TCP                        | Line Printer Daemon protocol, or Line Printer Remote protocol                                                  |
| 520         | RIP                        | UDP                        | Routing Information Protocol, used to find the optimal path between source and destination networks            |
| 521         | RIPng (IPv6)               | UDP                        | Routing Information Protocol next generation, the IPv6 compatible version of RIP                               |
| 540         | UUCP                       | TCP                        | Unix-to-Unix Copy Protocol                                                                                      |
| 548         | AFP                        | TCP                        | Apple Filing Protocol                                                                                           |
| 554         | RTSP                       | TCP, UDP                   | Real Time Streaming Protocol                                                                                   |
| 546         | DHCPv6                     | TCP, UDP                   | Dynamic Host Configuration Protocol version 6. DHCPv6 Clients listen for DHCPv6 messages on UDP port 546       |
| 547         | DHCPv6                     | TCP, UDP                   | DHCPv6 Servers and DHCPv6 Relay Agents listen for DHCPv6 messages on UDP port 547                              |
| 560         | rmonitor                   | UDP                        | Remote Monitor                                                                                                  |
| 563         | NNTP over TLS/SSL          | TCP, UDP                   | Network News Transfer Protocol with encryption and verification                                                |
| 587         | SMTP                       | TCP                        | For email message submission via SMTP                                                                          |
| 591         | FileMaker                  | TCP                        | FileMaker Web Companion                                                                                        |
| 593         | Microsoft DCOM             | TCP, UDP                   | Distributed Component Object Model                                                                             |
| 596         | SMSD                       | TCP, UDP                   | SysMan Station daemon                                                                                          |
| 631         | IPP                        | TCP                        | Internet Printing Protocol                                                                                     |
| 636         | LDAP over TLS/SSL          | TCP, UDP                   | Lightweight Directory Access Protocol over TLS/SSL                                                             |
| 639         | MSDP (PIM)                 | TCP                        | Multicast Source Discovery Protocol                                                                            |
| 646         | LDP (MPLS)                 | TCP, UDP                   | Label Distribution Protocol                                                                                     |
| 691         | Microsoft Exchange         | TCP                        | Microsoft Exchange Routing                                                                                     |
| 860         | iSCSI                      | TCP                        | Internet Small Computer Systems Interface                                                                      |
| 873         | rsync                      | TCP                        | The `rsync` file synchronization protocol                                                                      |
| 902         | VMware Server              | TCP, UDP                   | VMware ESXi, a hypervisor                                                                                      |
| 989         | FTPS                       | TCP                        | File Transfer Protocol (data) over TLS/SSL                                                                     |
| 990         | FTPS                       | TCP                        | File Transfer Protocol (control) over TLS/SSL                                                                  |
| 993         | IMAP over SSL (IMAPS)      | TCP                        | Internet Message Access Protocol over TLS/SSL                                                                  |
| 995         | POP3 over SSL (POP3S)      | TCP, UDP                   | Post Office Protocol 3 over TLS/SSL                                                                            |
----------------------------------------------------------------
## Registered Ports: 1024 – 49151
| Port Number       | Service Name                 | Transport Protocol          | Description                                                                                   |
|-------------------|------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------|
| 1025              | Microsoft RPC               | TCP                         | Microsoft Remote Procedure Call                                                              |
| 1026-1029         | Windows Messenger           | UDP                         | Windows Messenger popup spam                                                                 |
| 1080              | SOCKS proxy                 | TCP (or UDP since SOCKS5)   | SOCKS stands for Socket Secure. This protocol exchanges network packets through a proxy server. |
| 1080              | MyDoom                      | TCP                         | Computer virus                                                                               |
| 1194              | OpenVPN                     | TCP, UDP                    | OpenVPN                                                                                      |
| 1214              | KAZAA                       | TCP                         | A peer-to-peer file-sharing protocol                                                        |
| 1241              | Nessus                      | TCP, UDP                    | Nessus Security Scanner                                                                      |
| 1311              | Dell OpenManage             | TCP                         | Dell EMC OpenManage Server Administrator Web GUI                                            |
| 1337              | WASTE                       | TCP                         | WASTE peer-to-peer encrypted file-sharing program                                            |
| 1589              | Cisco VQP                   | TCP, UDP                    | Cisco VLAN Query Protocol (VQP)                                                              |
| 1701              | L2TP VPN                    | TCP                         | Layer Two Tunneling Protocol Virtual Private Networking                                      |
| 1720              | H.323                       | TCP                         | H.323 Call Control Signaling, a VoIP call control protocol                                   |
| 1723              | Microsoft PPTP              | TCP, UDP                    | Point-to-Point Tunneling Protocol Virtual Private Networking                                 |
| 1725              | Steam                       | UDP                         | Valve Steam Client uses port 1725                                                           |
| 1741              | CiscoWorks SNMS 2000        | TCP                         | CiscoWorks Small Network Management Solution web server                                      |
| 1755              | MMS                         | TCP, UDP                    | Microsoft Media Server                                                                       |
| 1812              | RADIUS                      | UDP                         | RADIUS server authentication and authorization                                              |
| 1813              | RADIUS                      | UDP                         | RADIUS server accounting                                                                     |
| 1863              | (Multiple uses)             | TCP, UDP                    | MSN Messenger, Xbox Live 360                                                                 |
| 1900              | UPnP                        | UDP                         | Universal Plug and Play                                                                      |
| 1985              | Cisco HSRP                  | UDP                         | Hot Standby Router Protocol                                                                  |
| 2000              | Cisco SCCP                  | TCP                         | Skinny Client Control Protocol                                                               |
| 2002              | Cisco ACS                   | TCP                         | Access Control Server                                                                        |
| 2049              | NFS                         | UDP                         | Network File Sharing                                                                         |
| 2082              | cPanel                      | TCP, UDP                    | cPanel default                                                                               |
| 2083              | radsec, cPanel              | TCP, UDP                    | Secure RADIUS Service (`radsec`), cPanel default SSL                                         |
| 2100              | amiganetfs                  | TCP                         | Amiga Network Filesystem                                                                     |
| 2222              | DirectAdmin                 | TCP                         | Graphical web hosting control panel                                                         |
| 2302              | Gaming                      | UDP                         | The game HALO uses this port extensively                                                    |
| 2483              | Oracle                      | TCP, UDP                    | Oracle database listening for insecure client connections to the listener, replaces port 1521 |
| 2484              | Oracle                      | TCP, UDP                    | Oracle database listening for SSL client connections to the listener                         |
| 2745              | Bagle.C – Bagle.H           | TCP                         | Computer worms                                                                               |
| 2967              | Symantec AV                 | TCP, UDP                    | Symantec System Center agent (SSC-AGENT)                                                    |
| 3050              | Interbase DB                | TCP, UDP                    | Borland Interbase database                                                                   |
| 3074              | XBOX Live                   | TCP, UDP                    | Gaming: Xbox LIVE and Games for Windows – Live                                              |
| 3127              | MyDoom                      | TCP                         | Computer worm                                                                               |
| 3128              | HTTP Proxy                  | TCP                         | Common web proxy server ports: 80, 8080, 3128, 6588                                         |
| 3222              | GLBP                        | TCP, UDP                    | Gateway Load Balancing Protocol                                                             |
| 3260              | iSCSI Target                | TCP, UDP                    | Microsoft iSCSI Target Server                                                               |
| 3306              | MySQL                       | TCP                         | MySQL database system                                                                       |
| 3389              | RDP                         | TCP                         | Windows Remote Desktop Protocol (Microsoft Terminal Server)                                 |
| 3689              | DAAP                        | TCP                         | Digital Audio Access Protocol, used by Apple’s iTunes and AirPort Express                   |
| 3690              | SVN                         | TCP, UDP                    | Apache Subversion, a version control system                                                |
| 3724              | World of Warcraft           | TCP, UDP                    | Some Blizzard games, Unofficial Club Penguin Disney online game for kids                   |
| 3784-3785         | Ventrilo VoIP               | TCP, UDP                    | Ventrilo’s Voice over Internet Protocol program                                             |
| 4333              | mSQL                        | TCP                         | Mini SQL server                                                                             |
| 4444              | Blaster                     | TCP, UDP                    | Computer worm                                                                               |
| 4500              | IPSec NAT Traversal         | UDP                         | Internet Protocol Security Network Address Translation (NAT) Traversal                     |
| 4664              | Google Desktop              | TCP                         | Google Desktop’s built-in HTTP server and indexing software                                 |
| 4672              | eMule                       | UDP                         | Peer-to-peer file-sharing software                                                          |
| 4899              | Radmin                      | TCP                         | Remote computer control software                                                            |
| 5000              | UPnP                        | TCP                         | Universal Plug and Play                                                                      |
| 5001              | iperf                       | TCP                         | Tool for measuring TCP and UDP bandwidth performance                                        |
| 5004-5005         | RTP, RTSP                   | UDP                         | Real-time Transport Protocol, Real Time Streaming Protocol                                  |
| 5050              | Yahoo! Messenger            | TCP                         | Instant messaging service from Yahoo                                                        |
| 5060              | SIP                         | TCP, UDP                    | Session Initiation Protocol                                                                 |
| 5061              | SIP-TLS                     | TCP                         | Session Initiation Protocol over TLS                                                       |
| 5190              | (Multiple uses)             | TCP, UDP                    | ICQ, AIM (AOL Instant Messenger), Apple iChat                                               |
| 5222-5223         | XMPP                        | TCP, UDP                    | Extensible Messaging and Presence Protocol Client Connection                                |
| 5353              | MDNS                        | UDP                         | Multicast DNS                                                                               |
| 5432              | PostgreSQL                  | TCP                         | PostgreSQL database system                                                                   |
| 5500              | VNC                         | TCP                         | Virtual Network Computing: Listening Viewer             |
| 5554              | Android Debug Bridge        | TCP                         | Often targeted by malware for unauthorized access       |
| 5631              | PCAnywhere                  | TCP                         | Symantec Remote Control Software                        |
| 5632              | PCAnywhere                  | UDP                         | Symantec Remote Control Software                        |
| 5800              | VNC                         | TCP                         | Virtual Network Computing: Web-Based                    |
| 5900-5901         | VNC                         | TCP                         | Virtual Network Computing: Display 0 and Display 1      |
| 6000-6063         | X11                         | TCP                         | X Window System display server                          |
| 6660-6669         | IRC                         | TCP                         | Internet Relay Chat                                     |
| 6679              | IRC SSL                     | TCP                         | Internet Relay Chat over SSL                            |
| 6697              | IRC SSL                     | TCP                         | Alternative port for Internet Relay Chat with SSL       |
| 6881-6889         | BitTorrent                  | TCP, UDP                    | Peer-to-peer file-sharing protocol                      |
| 6970-6999         | RTP Streaming               | UDP                         | Real-Time Protocol for video/audio streaming            |
| 8000-8080         | HTTP Proxy                  | TCP                         | Common ports for HTTP web servers                       |
| 8443              | HTTPS                       | TCP                         | HTTPS secured web servers                               |
| 8888              | Alternate HTTP              | TCP                         | Alternate web server port                               |
| 9000-9001         | Tor Network                 | TCP                         | Tor anonymizing overlay network                         |
| 9090              | Openfire Admin Console      | TCP                         | XMPP Server Admin Console                               |
| 9100              | HP JetDirect Print Services | TCP                         | Printer control                                         |
| 9999              | Multiple uses               | TCP                         | Commonly used for custom services                       |
| 10000             | Webmin                      | TCP                         | Webmin administrative interface                         |
| 12345             | NetBus                      | TCP                         | Remote administration tool, often exploited by attackers|
| 31337             | Back Orifice                | TCP                         | Remote administration tool, often exploited as a backdoor|
| 33434+      | traceroute   | UDP                | Utility for displaying paths and measuring transit delays of packets across a network |

---------------------------------------------------------------------------
## Dynamic/Private Ports: 49152 – 65535
| Port Number     | Service Name     | Transport Protocol | Description                                                       |
|------------------|------------------|--------------------|-------------------------------------------------------------------|
| 49152-65535     | Ephemeral Ports  | TCP, UDP           | Ports dynamically allocated for client-side communications        |

--------------------------------------------------------------------------
## The Most Common Ports for CCNA Exam
| Port Number | Service                |
|-------------|------------------------|
| 7           | Echo                  |
| 20, 21      | FTP                   |
| 22          | SSH/SCP               |
| 23          | Telnet                |
| 25          | SMTP                  |
| 53          | DNS                   |
| 67, 68      | DHCP/BOOTP            |
| 69          | TFTP                  |
| 80          | HTTP                  |
| 88          | Kerberos              |
| 110         | POP3                  |
| 123         | NTP                   |
| 137         | NetBIOS               |
| 143         | IMAP                  |
| 161         | SNMP                  |
| 194         | IRC                   |
| 389         | LDAP                  |
| 443         | HTTPS                 |
| 445         | Microsoft DS SMB      |
| 464         | Kerberos password settings |
| 547         | DHCPv6                |
| 596         | SMSD                  |
| 636         | LDAP over SSL         |
| 1720        | H.323                 |
| 3389        | RDP                   |
| 5060        | SIP                   |
| 5061        | SIP over TLS          |

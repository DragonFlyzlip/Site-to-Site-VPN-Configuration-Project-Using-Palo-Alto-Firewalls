# Site-to-Site-VPN-Configuration-Project-Using-Palo-Alto-Firewalls

## Objective

The objective of this project is to gain hands-on experience in configuring a site-to-site VPN using Palo Alto firewalls, a critical skill for anyone working in network security. By setting up and managing secure VPN tunnels, the project allows you to understand how to securely connect different networks over the internet, ensuring that sensitive data can be transmitted safely between locations. You’ll learn to configure Palo Alto firewall interfaces, virtual routers, zones, NAT policies, and IPSec VPN tunnels, all of which are essential elements in establishing a reliable and secure network architecture. Completing this project not only builds technical proficiency but also enhances your ability to troubleshoot and manage complex network security setups, which is invaluable for both security professionals and network administrators. Through this hands-on approach, you'll develop a deep understanding of VPN technology and how to implement it to safeguard communications across distributed networks.

### Skills Learned

Palo Alto Firewall Configuration: Setting up and managing firewall interfaces, zones, and virtual routers.
IPSec VPN Setup: Configuring secure site-to-site VPN tunnels.
NAT Policy Management: Implementing and troubleshooting NAT policies for secure traffic flow.
Network Security: Strengthening network security through encrypted communication channels.
Routing and Traffic Management: Handling routing protocols and traffic through VPN tunnels.
Firewall Policy and Rule Configuration: Defining and applying security policies and rules.
VPN Troubleshooting: Diagnosing and resolving issues in VPN connectivity.
Network Architecture Design: Building and optimizing network designs for secure remote connections.

### Tools Used


- Palo Alto Firewalls: For configuring security policies, VPN tunnels, and managing network traffic.
- GlobalProtect: For testing VPN connectivity and secure remote access.
- Command Line Interface (CLI): For advanced firewall configuration and troubleshooting.
- Palo Alto Panorama (optional): For centralized management of multiple Palo Alto devices.
- Wireshark: For packet capture and analysis of VPN traffic.
- Ping & Traceroute: For testing network connectivity and diagnosing routing issues.
- Web Interface (GUI): For configuring and managing the firewall through a graphical interface.

  
## Steps
![image](https://github.com/user-attachments/assets/a04fe2d8-59d4-4772-9055-9f99840f7412)

*Ref 1: Network Diagram*

![image](https://github.com/user-attachments/assets/2b023e9b-9363-4368-9c4c-312d1f83bacd)

*Fig 1.1 shows the Interfaces on the Headquarters site*

![image](https://github.com/user-attachments/assets/87f800a8-8ec0-45d7-ab73-28b301299ea1)

*Fig 1.2 shows the Tunnel on the Headquarters site.*

![image](https://github.com/user-attachments/assets/03a221b3-3ee7-4c40-8129-963f47c52bca)

*Fig 1.3 shows the Zones on the Headquarters site.*

![image](https://github.com/user-attachments/assets/10fa957a-0d56-448a-8a7f-6970dfd15121)

*Fig 1.4 shows the Virtual Routers on the Headquarters site.*

![image](https://github.com/user-attachments/assets/d3a5f8be-27c0-4614-a54b-3011dd07ea64)

*Fig 1.9 shows the Tunnel on the Branch site.*


![image](https://github.com/user-attachments/assets/d19abff0-b6b7-4faf-a9e1-aff83fb8d8c0)

*Fig 1.10 shows the Zones on the Branch site.*

![image](https://github.com/user-attachments/assets/5d5902c3-a6fc-4a26-bf0c-057a1f5e938d)

*Fig 1.11 shows the Virtual Routers on the Branch site.*

![image](https://github.com/user-attachments/assets/384724cb-a956-4b87-a01b-da5de4c02bcd)

*Fig 1.12 shows the IPSec Tunnels on the Branch site.*

![image](https://github.com/user-attachments/assets/be1b7c67-7ae1-4239-a6f9-7ad336865ae4)

*Fig 1.13 shows the IKE Gateways on the Branch site.*

![image](https://github.com/user-attachments/assets/2226e54d-1ad5-4ce9-8811-933b6a088770)

*Fig 1.14 shows the Interface Mgmt on the Branch site.*

![image](https://github.com/user-attachments/assets/b810c88a-11fe-4e38-9e79-ca91723ad7bd)

*Fig 1.15 shows Troubleshooting for testing the site-to-site VPN Tunnel IKE phase 1 on the Headquarters site.*

![image](https://github.com/user-attachments/assets/8729343e-5631-4b98-9add-d5368b3b99a6)

*Fig 1.16 shows Troubleshooting for testing the site-to-site VPN Tunnel IKE phase 2 on the Headquarters site.*

![image](https://github.com/user-attachments/assets/3bc2b01b-e8cf-404f-af40-aff9e6119bec)

*Fig 1.17 shows Troubleshooting for testing the site-to-site VPN Tunnel IKE phase 1 on the Branch site.*

![image](https://github.com/user-attachments/assets/df7898dd-072f-49ed-b764-1fafe9fe464d)

*Fig 1.18 shows Troubleshooting for testing the site-to-site VPN Tunnel IKE phase 2 on the Branch site.*

![image](https://github.com/user-attachments/assets/6e7d7929-2097-440b-b403-ff7ce58b6953)

Fig 1.19 shows the IPSec Tunnels on the Headquarters site.

![image](https://github.com/user-attachments/assets/cbb728e3-1b66-4201-926d-0d20ec294191)

*Fig 1.20 shows the IPSec Tunnels on the Branch site.*

![image](https://github.com/user-attachments/assets/15321116-2a93-49e1-8fd2-b443d84036ae)

*Fig 1.21 shows the Security Policy on the Headquarters site.*

![image](https://github.com/user-attachments/assets/86703855-2da6-4d7e-a056-45741b67753f)

*Fig 1.22 shows the Security Policy on the Branch site.*

![image](https://github.com/user-attachments/assets/3bbe205e-bded-4822-b932-a580723d0ac3)

*Fig 1.23 shows the NAT Policy on the Headquarters site.*

![image](https://github.com/user-attachments/assets/50ce546c-049d-4841-9e94-215ee4678977)

*Fig 1.24 shows the NAT Policy on the Branch site.*

![image](https://github.com/user-attachments/assets/513b72d9-7a73-453a-b184-241f0481026b)

*Fig 1.25 shows INSIDE at the branch site have access to DMZ at the headquarters site via a confidential site-to-site VPN.*


![image](https://github.com/user-attachments/assets/d4f0b68a-97b6-4363-8149-43f8612f95a0)

*Fig 1.26 shows INSIDE at the headquarters site have INTERNET access.*


![image](https://github.com/user-attachments/assets/336a878b-bfe0-4592-8c00-c7c3e2b07248)

*Fig 1.27 shows GUEST at the headquarters site is allowed only INTERNET access.*


![image](https://github.com/user-attachments/assets/54b025ce-e16e-454d-aa60-86599254548e)

*Fig 1.28 shows GUEST at the branch site is allowed only INTERNET access.*


![image](https://github.com/user-attachments/assets/b16f1679-e7a7-4af1-8147-baf209eb30d0)

*Fig 1.29 shows INSIDE at the headquarters site have access to DMZ at headquarters.*


![image](https://github.com/user-attachments/assets/24473989-0c65-45c9-9137-f3348ee3dceb)

*Fig 1.30 shows INSIDE at the branch site have INTERNET access.*































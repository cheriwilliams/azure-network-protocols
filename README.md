<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Filter ICMP traffic in Wireshark 
- Observe ICMP traffic between Ubuntu Server and Windows 10
- Disable incoming traffic with Network Security Group
- Filter SSH and observe traffic 
- Filter DHCP and observe traffic
- Filter DNS and observe traffic  
- Filter RDP and observe traffic 

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/YWFc6f5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above image shows traffic being pinged from Windows 10 Virtual Machine to Ubuntu Virtual Machine. The traffic between the two machines was successful showing 4 packets sent and 4 packets received. 
</p>
<br />

<p>
<img src="https://i.imgur.com/HLbKOPX.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Incoming traffic has been disabled from the firewall in Azure. Network Security Group was utilized and the security rule was applied to deny traffic and the ping request stopped. 
</p>
<br />

<p>
<img src="https://i.imgur.com/Oce0ZY2.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the above image, a significant amount of SSH (Secure Shell) traffic has spammed in Wireshark from the pwd command being entered into the command line. 
</p>
<br />

<p>
<img src="https://i.imgur.com/q7eomXT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
While using the command ipconfig /renew, an IP address lease is renegotiated from the DHCP server to the VM. A small amount of DHCP (Dynamic Host Configuration Protocol) traffic was generated from that command. 
</p>
<br />

<p>
<img src="https://i.imgur.com/KmGufGo.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above image shows the command nslookup being prompted to find the IP addresss for www.google.com, DNS (Domain Name System) traffic is then generated in Wireshark from nslookup. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DimpbiF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
RDP (Remote Desktop Protocol) traffic constantly coming through Wireshark because of the active running connection of the Windows VM. 
</p>
<br />

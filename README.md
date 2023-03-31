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
- Observe SSH
- Observe DHCP Traffic
- DNS Traffic 
- RDP Traffic 

<h2>Actions and Observations</h2>

<p>
<img src=https://i.imgur.com/evLjJoU.jpg/>
</p>
<p>
The above image shows traffic being pinged from Windows 10 VM to Ubuntu VM. The traffic between the two machines was successful showing 4 packets sent and 4 packets received. 
</p>
<br />

<p>
<img src=https://i.imgur.com/8uRELl2.jpg/>
</p>
<p>
Incoming traffic has been disabled from the firewall in Azure. Network Security Group was utilized and the security rule was applied to deny traffic and the ping request stopped. 
</p>
<br />

<p>
<img src=https://i.imgur.com/JC9Alzl.jpg/>
</p>
<p>
In the above image, a significant amount of SSH traffic has spammed in Wireshark from the pwd command being entered into the command line. 
</p>
<br />

<p>
<img src=https://i.imgur.com/jAShtVx.jpg/>
</p>
<p>
While using the command line ipconfig /renew, a new IP address can be issued for the VM, and a small amount of DHCP traffic was generated from that command. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

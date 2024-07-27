# Exploring-the-Seven-Domains-of-a-Typical-IT-Infrastructure

## Objective
I will explore the seven domains within a virtual lab environment in this lab. Along the way, I will review several foundational IT concepts, including operating systems, server roles, and network connectivity.

### Skills Learned
- Identify and navigate the seven domains of a typical IT infrastructure.
- Use common command-line utilities to gather relevant system information.
- Use PuTTY to connect to network devices remotely.
- Identify common network devices, including switches, routers, and firewalls.
- Identify common server roles, including domain controllers, web servers, and file servers.

### Tools and Software Used
- PuTTY
- Ping
- Open vSwitch
- TrueNAS
- pfSense
- Traceroute
- Nslookup
- OpenVPN
- OWASP Juice Shop

### Topology
- vWorkstation (Windows: Server 2022)
- Switch01 (Linux: Debian 11)
- FileServer01 (FreeBSD)
- pfSense-office (FreeBSD)
- pfSense-dc (FreeBSD)
- DomainController01 (Windows: Server 2019)
- WebServer01 (Linux: Ubuntu 20)
- RemoteWindows01 (Windows: Server 2019)
- AttackLinux01 (Linux: Kali)

### Lab Overview
STEP 1 of this lab has three parts, which should be completed in the order specified.
 
- I will review basic security controls on a Windows workstation.

- I will explore additional devices on the LAN segment, including a Linux-based switch and a FreeBSD-based file server.

- I will connect to a router-firewall device and learn about the network perimeter.

STEP 2
- I will extend my exploration of the lab environment to the WAN, Remote Access, and System/Application Domains.



<h2>Program walk-through:</h2>

## STEP 1

### Part 1: Explore the Workstation Domain

<p align="center">
vWorkstation login-screen: <br/>
<img src="https://i.imgur.com/l9b0ELy.png" height="80%" width="80%" alt="vWorkstation log-in screen"/>
<br />
<br />
Your info page:  <br/>
<img src="https://i.imgur.com/mlIkCWv.png" height="80%" width="80%" alt="Your info page"/>
<br />
<br />
Sign-in Options Page: <br/>
<img src="https://i.imgur.com/eEEklYz.png" height="80%" width="80%" alt="Sign-in Options page"/>
<br />
<br />
Search for Windows Updates:  <br/>
<img src="https://i.imgur.com/d9JIS0p.png" height="80%" width="80%" alt="Search for Windows Updates"/>
<br />
<br />
Click view Policies Link:  <br/>
<img src="https://i.imgur.com/hOilG24.png" height="80%" width="80%" alt="click view policies link"/>
<br />
<br />
View Policies Link:  <br/>
<img src="https://i.imgur.com/mWawGyu.png" height="80%" width="80%" alt="view policies link"/>
<br />
<br />
Windows Security page:  <br/>
<img src="https://i.imgur.com/yoRfrgD.png" height="80%" width="80%" alt="windows security page"/>
  <br />
<br />
Virus & Threat Protection Page:  <br/>
<img src="https://i.imgur.com/V1ReOEh.png" height="80%" width="80%" alt="virus and threat protection page"/>
<br />
<br />
Double-click the Thunderbird icon:  <br/>
<img src="https://i.imgur.com/SErUM0x.png" height="80%" width="80%" alt="thunderbird icon"/>
  <br />
<br />
Inbox:  <br/>
<img src="https://i.imgur.com/LhKevAG.png" height="80%" width="80%" alt="Inbox"/>
<br />
<br />
Click on the first email:  <br/>
<img src="https://i.imgur.com/HRUpPqN.png" height="80%" width="80%" alt="first email"/>
  <br />
<br />
Second email:  <br/>
<img src="https://i.imgur.com/6FGH403.png" height="80%" width="80%" alt="second email"/>
<br />
<br />
Block Attachment message:  <br/>
<img src="https://i.imgur.com/WJhg5Jv.png" height="80%" width="80%" alt="block attachment message"/>
    <br />
<br />
File Explorer icon, Navigate to Network and then Employees Folder:  <br/>
<img src="https://i.imgur.com/M27BfaH.png" height="80%" width="80%" alt="block attachment message"/>
<br />
<br />
Successful connections to the Adodson user folder:  <br/>
<img src="https://i.imgur.com/iP5ntUB.png" height="80%" width="80%" alt="Adodson folder"/>
  <br />
<br />
Failed connection to another user folder:  <br/>
<img src="https://i.imgur.com/0EZV3nQ.png" height="80%" width="80%" alt="failed connection"/>
<br />
<br />
Click on Shared Folder:  <br/>
<img src="https://i.imgur.com/IJb48t9.png" height="80%" width="80%" alt="shared folder"/>
<br />
<br />
Sign Out Dodson Account:  <br/>
<img src="https://i.imgur.com/KdQC83E.png" height="80%" width="80%" alt="Sign out"/>
</p>
<br/>

### Part 2: Explore the LAN Domain

<p align="center">
Alice login-screen: <br/>
<img src="https://i.imgur.com/xrEumxs.png" height="80%" width="80%" alt="Alice log-in screen"/>
<br />
<br />
Command Prompt:  <br/>
<img src="https://i.imgur.com/oxcHsws.png" height="80%" width="80%" alt="Command Prompt"/>
<br />
<br />
Network Interfaces: <br/>
<img src="https://i.imgur.com/pzqsjco.png" height="80%" width="80%" alt="Network Interfaces"/>
<br />
<br />
ARP table:  <br/>
<img src="https://i.imgur.com/IHLhWeq.png" height="80%" width="80%" alt="ARP table"/>
<br />
<br />
Ping the pfSense-office device:  <br/>
<img src="https://i.imgur.com/iVDqbp9.png" height="80%" width="80%" alt="ping the pfSense office"/>
<br />
<br />
Ping the Switch01 device:  <br/>
<img src="https://i.imgur.com/4RxbmQh.png" height="80%" width="80%" alt="ping the Switch01"/>
<br />
<br />
Ping the FileServer01:  <br/>
<img src="https://i.imgur.com/OZlmZOQ.png" height="80%" width="80%" alt="ping the fileServer"/>
  <br />
<br />
vWorkstation updated ARP table and close the cmd:  <br/>
<img src="https://i.imgur.com/B47HQth.png" height="80%" width="80%" alt="ARP updated"/>
<br />
<br />
PuTTY configuration window and click open:  <br/>
<img src="https://i.imgur.com/800ezg0.png" height="80%" width="80%" alt="PuTTY"/>
  <br />
<br />
Log-in prompt by typing credentials for username and password:  <br/>
<img src="https://i.imgur.com/9gfIF71.png" height="80%" width="80%" alt="Log-in prompt"/>
<br />
<br />
 Network interfaces on Switch01:  <br/>
<img src="https://i.imgur.com/1xCXdOP.png" height="80%" width="80%" alt="Network interfaces on Switch01"/>
  <br />
<br />
Open vSwitch configuration database:  <br/>
<img src="https://i.imgur.com/C7seco5.png" height="80%" width="80%" alt="open vSwitch"/>
<br />
<br />
Open vSwitch forwarding table and then close PuTTY:  <br/>
<img src="https://i.imgur.com/trakQSd.png" height="80%" width="80%" alt="open vSwitch forwarding"/>
    <br />
<br />
</p>


### Part 3: Explore the LAN-to-WAN

<p align="center">
Click the Firefox icon and Firefox navigation bar: <br/>
<img src="https://i.imgur.com/ippc4T3.png" height="80%" width="80%" alt="Firefox navigation bar"/>
<br />
<br />
pfsense log-in screen:  <br/>
<img src="https://i.imgur.com/ILKUhUw.png" height="80%" width="80%" alt="pfsense log-in screen"/>
<br />
<br />
Firewall NAT: <br/>
<img src="https://i.imgur.com/1WnM123.png" height="80%" width="80%" alt="Firewall NAT"/>
<br />
<br />
Outbound NAT Settings:  <br/>
<img src="https://i.imgur.com/1imNhX2.png" height="80%" width="80%" alt="Outbound NAT Settings"/>
<br />
<br />
Firewall Rules:  <br/>
<img src="https://i.imgur.com/c56nXKv.png" height="80%" width="80%" alt="Firewall Rules"/>
<br />
<br />
LAN Rules:  <br/>
<img src="https://i.imgur.com/8ESnAf6.png" height="80%" width="80%" alt="LAN Rules"/>
<br />
<br />
System Routing:  <br/>
<img src="https://i.imgur.com/nhuMC89.png" height="80%" width="80%" alt="system routing"/>
  <br />
<br />
Static Routes:  <br/>
<img src="https://i.imgur.com/bhg34Ie.png" height="80%" width="80%" alt="Static Routes"/>
<br />
<br />
Open cmd and type tracert 172.30.0.5:  <br/>
<img src="https://i.imgur.com/v2PSAUn.png" height="80%" width="80%" alt="Traceroute results"/>
  <br />
<br />
Result of tracert to the pfsense-dc appliance:  <br/>
<img src="https://i.imgur.com/X8Gy08w.png" height="80%" width="80%" alt="result tracert"/>
<br />
<br />
Get back to the Firewall Virtual IPs:  <br/>
<img src="https://i.imgur.com/QMe9aJD.png" height="80%" width="80%" alt="Firewall virtual IPs"/>
  <br />
<br />
Port Forwarding rules for the web server:  <br/>
<img src="https://i.imgur.com/Iw0FW5t.png" height="80%" width="80%" alt="Port forwarding"/>
<br />
<br />
DMZ Rules:  <br/>
<img src="https://i.imgur.com/foVNI5v.png" height="80%" width="80%" alt="DMZ rules"/>
    <br />
<br />
</p>



## STEP 2
### Part 1: Explore the WAN Domain

<p align="center">
</p>

### Part 2: Explore the Remote Access Domain
<p align="center">

</p>


### Part 3: Explore the System/Application Domain
<p align="center">

</p>

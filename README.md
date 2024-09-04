<p align="center">

![Traffic Examination](https://github.com/user-attachments/assets/15aa33d7-4592-46cd-9d55-0564615eceaa)


<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark.
<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (ICMP, RDP, DNS)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)
- Ubuntu Server 20.04

<h2>List of Prerequisites</h2>

-  Microsoft Azure Account
-  Laptop/DeskTop with RDP capability 
-  HighSpeed WIFI

<h2>Overview</h2>

- Observe ICMP Traffic
- Observe RDP Traffic
- Observe DNS Traffic

<h2>Create Resource Group and VM's</h2>

![2024-08-19 20_30_37-azure](https://github.com/user-attachments/assets/43bb9a37-bb65-4362-9e32-dfe7cf347be1)

- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM) inside the newly created Resource Group
- While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet
- Create a Linux (Ubuntu) VM
- While creating the VM, select the previously created Resource Group and Vnet
- Observe Your Virtual Network within Network Watcher

<h2>Observe ICMP Traffic</h2>

![ICMP tarffic](https://github.com/user-attachments/assets/288c8bf6-4cc8-47a3-8bbe-1c6413210f58)

- Use Remote Desktop to connect to the Windows 10 VM
- Within Windows 10 Virtual Machine, Download and Install Wireshark
- Open Wireshark and filter for ICMP traffic only
- Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM
- Observe ping requests and replies within WireShark

<h2>Observe RDP Traffic</h2>

![RDP Traffic](https://github.com/user-attachments/assets/a6ebd368-c965-448f-aca7-fd1e61fe2c23)

- In Wireshark, filter for RDP traffic only (tcp port 3389)
- Observe the immediate non-stop traffic this is because the RDP (protocol) is constantly showing you a live stream from one computer to another, therefor traffic is always being transmitted

<h2>Observe DNS Traffic</h2>  

![DNS traffic](https://github.com/user-attachments/assets/b06a8965-bf28-4991-af29-0b77e6290b8e)

- In Wireshark, filter for DNS traffic only
- From your Windows 10 VM within the command line, use the nslookup command to see what the IP address for google.com displays
- Observe the DNS traffic being shown in WireShark

  

<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 Pro, 25H2

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Domain Controller(DC-1) in Azure
- Setup Client-1 In Azure
- Install Active Directory
- Setup Remote Desktop
- Create Users Accounts

<h2>Deployment and Configuration Steps</h2>

<p><img width="1700" height="1021" alt="Screenshot 2026-10-26 214011" src="https://github.com/user-attachments/assets/8f2e1dc3-4123-4caf-9c2d-263bb44e3641" />
<img width="1917" height="1110" alt="Screenshot 2026-10-26 204440" src="https://github.com/user-attachments/assets/02f50881-905c-4a29-9863-bb4f8753f75f" />
<img width="1413" height="1116" alt="Screenshot 2026-10-26 205041" src="https://github.com/user-attachments/assets/f98668b8-c778-480b-848f-9001afabd391" />


</p>
<p>
## Azure Windows Server Lab – DC-1

Create a basic Azure lab by setting up a Resource Group, Virtual Network, and Windows Server virtual machine named **DC-1**. Configured the network interface card (NIC) with a static private IP address. Disabled Windows Firewall to test network connectivity.
</p>
<br />

<p><img width="1386" height="1107" alt="Screenshot 2026-10-26 211303" src="https://github.com/user-attachments/assets/f09d90cb-db6c-4be7-9256-5c236fd73d02" />

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a second virtual machine named Client-1 in the same Azure region and virtual network as DC-1. Configure the virtual network's DNS settings to use DC-1's private IP address. Restart Client-1 from the Azure Portal and log into the virtual machine. Then ping DC-1's private IP address to test the network connection and make sure the ping was successful.&#x20;

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Active Directory Domain Services (AD DS) on DC-1 and create a new forest. After setting up the domain, restart the server and log back in using the domain administrator account.&#x20;

</p>
<br />
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

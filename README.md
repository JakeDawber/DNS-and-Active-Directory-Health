<h1>DNS and Active Directory Health</h1>


<h2>Process</h2>

DNS Service Verification: Used netstat to confirm that DNS is listening on TCP and UDP port 53 on the domain controller's assigned IPv4 address. Successful DNS resolution and Active Directory DNS diagnostics were verified separately.

<img src="Screenshots/Power on VM.png"/>

<h2>Environment</h2>

Virtualisation: VMware Workstation

Operating System: Windows Server 2022 Standard

Server hostname: JH-DC01

Domain name: jakehomelab.test

Server IP address: 192.168.193.10/24

Server role: Domain Controller

Roles installed: Active Directory Domain Services (AD DS) and DNS Server

<h2>Implementation</h2>

1. Virtual Machine and Network Configuration

Created a Windows Server 2022 virtual machine and configured a static IPv4 address to ensure the server remained accessible at a consistent address. The server was connected to an isolated host-only virtual network.

<img src="Screenshots/Power on VM.png"/>

2. Active Directory Domain Services

Installed the AD DS role through Server Manager and promoted the server to a Domain Controller. Created a new Active Directory forest using the domain name jakehomelab.test.

<img src="Screenshots/Roles and sever.png"/>

Whilst adding the DNS role to the server, I came across a problem. My troubleshooting process can be found [here](https://github.com/JakeDawber/Lab-setup/tree/main)

3. DNS Configuration and Verification

Configured DNS as part of the Domain Controller setup. Created and verified the relevant DNS records, including forward and reverse lookup records, to support hostname resolution across the lab environment.

Used PowerShell, nslookup and dcdiag /test:dns to investigate DNS behaviour and verify that the domain controller and its DNS configuration were functioning correctly.

<h2>Outcome</h2>

Successfully established the initial Active Directory environment, providing a foundation for the next stages of the project. This environment will be expanded with domain users, organisational units (OUs), security groups, Group Policy and a Windows client machine to simulate common IT support scenarios.

<h2>Skills Demonstrated</h2>

Windows Server installation and configuration

Virtual machine and network setup

Active Directory Domain Services deployment

Domain Controller promotion and forest creation

DNS configuration and troubleshooting

PowerShell and command-line diagnostics

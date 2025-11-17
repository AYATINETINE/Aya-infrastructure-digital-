– Project 1: DHCP Server with Windows 10 Client (Windows Server 2019)

## Project Overview
This project demonstrates the deployment of a Windows Server 2019 DHCP environment in VMware Workstation Pro. The DHCP server is configured to automatically assign IP addresses to a Windows 10 client. The goal is to understand DHCP setup, IP management, and client integration in a virtualized network.

## Tools & Platform
- VMware Workstation Pro
- Windows Server 2019 (Server 1)
- Windows 10 Client
- Host-only Networking

## Virtual Machine Configuration
- Server 1: 4 GB RAM, 4 CPU cores, 60 GB disk, Host-only network
- Windows 10 Client: 2 GB RAM, 2 CPU cores, 30 GB disk, Host-only network

## Network Configuration
- Server 1 IP Address: 192.168.1.3, Subnet Mask: 255.255.255.0, Default Gateway: 192.168.1.1
- Windows 10 Client: DHCP, reserved IP 192.168.1.205 based on MAC address 00:0C:29:65:E0:CC

## DHCP Server Configuration
- Scope Name: LAN Virtuel
- IP Range: 192.168.1.200 – 192.168.1.209
- Excluded IP Address: 192.168.1.203
- Lease Duration: 8 days
- Reservation: 192.168.1.205 assigned to Windows 10 Client based on MAC address

## Steps Performed
1. Created Virtual Machines (Server 1 and Windows 10 Client) in VMware Workstation Pro.
2. Configured Host-only networking for internal communication.
3. Set static IP for Server 1 (192.168.1.3).
4. Installed the DHCP role on Server 1.
5. Created a scope with defined IP range, exclusion, and lease duration.
6. Added reservation for Windows 10 Client based on its MAC address.
7. Powered on Windows 10 Client and verified it received the reserved IP automatically.

## Key Learnings
- Deployment and configuration of DHCP server on Windows Server 2019.
- IP address management using scopes, exclusions, and reservations.
- Integration of client machines in a virtualized network.
- Host-only network configuration in VMware Workstation Pro.

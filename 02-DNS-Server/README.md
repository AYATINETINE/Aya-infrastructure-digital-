Project 2: DNS Configuration with Primary & Secondary Zones (Windows Server 2019)

This project demonstrates the configuration of a DNS infrastructure using two Windows Server 2019 machines. The setup includes a Primary DNS Zone on Server 1 and a Secondary DNS Zone on Server 2 to ensure redundancy and zone replication.


• Tools & Environment

VMware Workstation Pro

Windows Server 2019 – Server 1 (Primary DNS)

Windows Server 2019 – Server 2 (Secondary DNS)

Host-only Network

Server 1 IP: 192.168.1.3

Server 2 IP: 192.168.1.2

• DNS Configuration – Server 1 (Primary DNS)

1. Direct Lookup Zone (Forward Lookup Zone)

Created a Primary Zone

Domain name: formation.local

Zone file: formation.local.dns


2. DNS Records Created
   
the first record Dns

Hostname :serveur1
FQDN:serveur1.formation.local
IP Address:192.168.1.3

the second record Dns

Hostname:www
FQDN:www.formation.local
IP Address:192.168.1.20

3. Reverse Lookup Zone

Type: Primary Zone

Network ID: 192.168.1

Created PTR records linked to A records



• DNS Configuration – Server 2 (Secondary DNS)

1. Secondary Zone Setup

Zone Type: Secondary Zone

Domain name: formation.local

Master DNS server: 192.168.1.3

Server 2 gets all DNS records from Server 1 automatically


• Final Result

Primary DNS (Server 1) and Secondary DNS (Server 2) fully synchronized

Forward and reverse zones working correctly

Redundancy ensured through zone replication

DNS resolution functional using A and PTR records

# Network Design

## Overview
Current configuration includes a home router configured with DHCP for IP assignment. Domain Controller (DC-02) is the primary DNS server.
(Will be upgrading to enterprise Cisco router and managed switch)

## Network
- Subnet: 192.168.1.0/24, single subnet for all devices.
  - Gateway: 192.168.1

## Services
- DHCP 
  - Server: 192.168.1.1
  - 192.168.1.2 reservation for domain controller DC-02.homelab.com
  - DNS option: domain controller assigned as DNS server for DHCP clients.

- DNS
  - Server: 192.168.1.2, DC-02.homelab.com
  - DNS server configured along side Active Directory services on DC-02.
  - Used to resolve hostnames within the network. All external DNS queries are forwarded to a public DNS server such as 8.8.8.8

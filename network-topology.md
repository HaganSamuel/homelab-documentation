# Network Topology

## Overview

The home lab uses a single physical host running Proxmox VE. Virtual machines and containers are connected through a virtual bridge and share access to the home router network.

## Basic Layout

Internet
→ ISP Modem/Router
→ Home Router
→ Proxmox Host
→ Virtual Machines / Containers

## Devices

| Device | Purpose | Connection |
|---|---|---|
| Home Router | Gateway, DHCP, internet access | Physical network |
| Proxmox Host | Runs VMs and containers | Ethernet |
| Ubuntu Server VM | Linux administration / Docker host | Virtual bridge |
| Windows Server VM | Active Directory / DNS / DHCP practice | Virtual bridge |
| Windows Client VM | Domain-joined test machine | Virtual bridge |

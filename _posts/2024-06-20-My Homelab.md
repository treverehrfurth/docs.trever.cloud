---
title: My Homelab
description: An overview of my current homelab including hardware, software, and networking.
date: 2024-06-20 12:00:00 -0500
categories: [Homelab, Overview]
tags: [homelab]     # TAG names should always be lowercase
---

A lot of years, money and sleepless nights later, this homelab has gone through two or three major iterations

## Whats in the Rack:
1. UDM-PRO - networking and security cams for inside and outside my house.
2. USW-16-POE
3. TP-Link 24 port gigabyte switch
4. Patchbox Plus + Cat 6a 
5. 48-Port blank Keystone
6. CyberPower Pure Sine Wave UPS
6. Kinan 8-port KVM console
7. Supermicro 847 36 Bay chassis for TrueNAS Scale 
12 x 10 TB (2 x RaidZ2)
12 x 14 TB (2 x RaidZ2)
6 x 1TB SSD (RaidZ2)
Xenon W-1290P | 128 GB DDR4-3200 ECC RAM

Servers:
Running 5 servers in a High Available cluster 
All are from old gaming rigs. Every 3 years or so I buy a new gaming rig and toss the previous moba, ram, cpu, and psu into Rosewill 4U chassis.
Server 1: i7-12700K | GTX 1080TI
Server 2: i7-9700K | GTX 980TI
Server 3: i7-6700K
Server 4: i7-4790K
Server 5: AMD Ryzen 5 3600

As you can see from my Homepage dashboard, I run a bunch of services across multiple VM's with high availability. If I ever take any server down, the VM's are spun up on the remaining nodes in the cluster. Here are some of my services starting with the coolest.

## Servies 
Clusterplex: I took plex onestep further and deployed clusterplex by pabloromeo on github. This amazing developer created add-on is a way to distribute transcode jobs from one Plex server across multiple VM's or workers. This has allowed me to scale out plex without ever taking up too much processing on any given server/VM. It is meant for Kubernetes and docker swarm but can be configured to work in normal docker containers.
Also using Tautulli for better metrics and observability of Plex
Wazuh: A wonderful SIEM solution I have deployed on all servers and computers on the network with active response rules, alerts to discord and vulnerability monitoring. 

Uptime-Kuma: Super easy and quick uptime monitor for all services with notifications linked to discord for any outages. 

Not shown on dashboard: Pterodactyl Game server

NGINX Proxy Manager: Reverse proxy for ip's

Automated eBook and Audiobook library using Calibre, Readarr and Calibre-Web. (Account with myanonymouse)

Vaultwarden: selfhosted Bitwarden

Immich: Photo/Video backup Solution
# Overview
These topology files are intended to be imported into your instance of Cisco Modeling Labs to explore a feature or use case. Labs generally include a lab guide as part of the YAML file for you to reference inside CML.

You can make importing these labs into CML simpler by adding this repository directly to your CML instance. See the link below for more information.
https://developer.cisco.com/docs/modeling-labs/managing-lab-repositories/

## Atomic_Config_Manager
Note this feature is not yet considered GA.

The purpose of this lab is to understand the new Atomic Configuration Manager feature introduced in controlled availability in IOS-XE 17.18. This feature allows you to apply configuration changes as a transaction. ACM supports syntax validation, config diffs, and automatic or manual rollback in the event the change is not successful. 

This lab requires IOS-XE 17.18.2 for Catalyst 8000V. The image definition must be named "c8000v-17-18-2", or you must modify the yaml file accordingly before importing it.

## 8000v Forwarding
This lab helps us understand software-based forwarding platforms such as the Catalyst 8000 (C8500L or smaller) as well as Secure Router 8000 platfroms (8400 and smaller). We explore how traffic is load-balanced across different data plane processes.

## PnP Discovery
These two labs are meant to be used in conjunction with an external Catalyst Center instance. We leverage DHCP and authoritative DNS on a cisco device to enable PnP discovery on Catalyst 9000v switches and Catalyst 9800-CL wireless LAN controllers. You can explore this using front-panel ports as configured, or change the topology to use the management interfaces if you desire on the C9000v.

Notes: the default node definition in CML for C9000v includes a start-up configuration. The presence of start-up config disabled PnP. You'll need need to modify the default node definition or duplicate it. This lab will need to to be edited to match the name of your new node definition.

## GIR Demo (NX-OS)
Graceful Insertion and Removal allows us to isolate a network device from the topology to minimize the impact of maintenance. Here we use a Nexus 9000v to showcase this behavior, but it can be done on many other platforms as well.

## Simple EVPN L3VNI
Uses EPVN L3VNI to transport TrustSec tags across an unfriendly provider network. We also showcase basic tenant routed multicast.

## Simple ePBR
Policy-based routing using NBAR protocol match is a very useful tool for SSE integration. Some traffic does not benefit from an SSE service, e.g., encrypted applications leveraging certificate pinning. Other traffic should always take the most optimal path for the sake of user experience -- such as voice. This lab uses a simple telnet vs. ssh example to showcase the feature.

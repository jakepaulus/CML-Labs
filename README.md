# Overview
These topology files are intended to be imported into your instance of Cisco Modeling Labs to explore a feature or use case. Labs generally include a lab guide as part of the YAML file for you to reference inside CML.

You can make importing these labs into CML simpler by adding this repository directly to your CML instance. See the link below for more information.
https://developer.cisco.com/docs/modeling-labs/managing-lab-repositories/

## Atomic_Config_Manager
The purpose of this lab is to understand the new Atomic Configuration Manager feature introduced in IOS-XE 17.18. This feature allows you to apply configuration changes as a transaction. ACM supports syntax validation, config diffs, and automatic or manual rollback in the event the change is not successful. 

This lab requires IOS-XE 17.18.2 for Catalyst 8000V. The image definition must be named "c8000v-17-18-2", or you must modify the yaml file accordingly before importing it.

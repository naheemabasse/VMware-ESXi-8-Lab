# Deployment and Administration of a nested VMware ESXi 8 Virtualization Environment using VMware Workstation Pro
![Nested ESXi Lab Architecture](./assets/architecture.jpg)

## Table of Contents

## 1. Overview
This project documents the deployment and administration of a VMware ESXi virtualization environment running as a nested hypervisor inside a VMware Workstation VM.
Configured ESXi and browser-based management, provisioned a VMFS datastore, and deployed an Ubuntu Server 26.04.1 virtual machine on top of it.

The lab was done this way due to a lack of a dedicate bare-metal machine on which ESXi could run. 
The environment runs on a Windows host with limited hardware resources, making it a small-scale lab for learning and testing virtualization concepts.

## 2. Objectives
Enterprise environments run VMware vSphere platform on dedicated server hardware, which is not available to most students. The goal of this lab was to build a working ESXi environment on a single laptop using nested virtualization, in order to:

- Understand the basics of the VMware vSphere platform and its features, including: vCenter Server, live VM migration (vMotion), high availability (HA), distributed resource scheduling (DRS), etc.; 
- Understand how EXSi is installed, configured and administered;
- Gain hands-on experience on performing core ESXi administration tasks are run: networking, storage, and VM deployment;

## 3. Architecture
```
Physical PC: Windows 10 Pro, Intel Core i5-7440HQ
 └─ VMware Workstation (Type 2 hypervisor)
     └─ ESXi VM (running ESXi 8 - Type 1 hypervisor, nested)
         ├─ Virtual networking: vSwitch
         ├─ VMFS datastore
         └─ Ubuntu Server 26.04.1 VM
```

## Proof of Execution
![ESXi Web UI and VMFS Datastore](./assets/esxi-vmfs-ui.png)
*Caption: ESXi Host Client showing active host status, VMFS datastore, and the Ubuntu Server VM.*

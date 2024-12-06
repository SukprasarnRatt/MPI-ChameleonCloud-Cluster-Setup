# MPI-ChameleonCloud-Cluster-Setup

**Setup and Configuration of a Virtual Machine Cluster to Run MPI Programs**

---

## Objective

This repository showcases the process of setting up a virtual machine (VM) cluster on Chameleon Cloud to execute MPI-based parallel programs. It includes detailed configurations for shared storage using NFS, installation of MPICH, and execution of a distributed "Hello World" program.

---

## Features

- **Virtual Machine Deployment and Configuration**:  
  Set up a cluster with multiple VMs for parallel computing.

- **NFS Server Setup**:  
  Configure a shared storage system for seamless data sharing between nodes.

- **MPICH Installation**:  
  Install and configure the MPICH library for running MPI programs.

- **Distributed Program Execution**:  
  Run and verify a parallel "Hello World" program across the cluster.
  
---

## Set Up Environment

- **Create 3 Virtual Machines using CentOS Stream9**:  
  These virtual machines will be set up as a cluster in the future as shown in the images below. We will access these clusters using SSH public and private keys.

  <img src="screenshots/vm_creation_1.png" width="400">
  <img src="screenshots/vm_creation_2.png" width="400">
  <img src="screenshots/vm_creation_3.png" width="400">
  <img src="screenshots/vm_creation_4.png" width="400">

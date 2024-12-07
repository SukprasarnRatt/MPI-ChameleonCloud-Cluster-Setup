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

### **Create 3 Virtual Machines using CentOS Stream9**  
These virtual machines are configured as a cluster to enable distributed computing. Access to the cluster is secured using an SSH key pair, consisting of a public key (stored on the virtual machines) and a private key.

<img src="screenshots/Picture1.png" width="400"><br>
<img src="screenshots/Picture2.png" width="400"><br>
<img src="screenshots/Picture3.png" width="400"><br>
<img src="screenshots/Picture4.png" width="400"><br>

---

### **Create NFS Server**  
Create an NFS server with a 5GB volume. Attach the volume to the NFS server to enable shared storage for the cluster.

<img src="screenshots/Picture5.png" width="400"><br>
<img src="screenshots/Picture6.png" width="400"><br>
<img src="screenshots/Picture7.png" width="400"><br>
<img src="screenshots/Picture8.png" width="400"><br>
<img src="screenshots/Picture9.png" width="400"><br>

---

### **Modify `/etc/hosts`**  
Configuring the `/etc/hosts` file on each virtual machine enables hostname resolution within the cluster. By editing this file, we ensure that all the nodes in the cluster can communicate using human-readable hostnames instead of hard-to-remember IP addresses.

Example `/etc/hosts` configuration:

```bash
[cc@2074557-3 ~]$ cat /etc/hosts
127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6
10.56.1.56  2074557-1.novalocal
10.56.3.137 2074557-2.novalocal
10.56.1.160 2074557-3.novalocal
10.56.0.214 nfs-2074557.novalocal
[cc@2074557-3 ~]$

# Kali Linux Network Configuration Lab

A step-by-step practical lab for setting up a Kali Linux virtual machine in VirtualBox, configuring a NAT Network, assigning a static IP address, configuring the default gateway, and verifying network and DNS connectivity.

---

## Table of Contents

1. [About the Lab](#1-about-the-lab)
2. [Objectives](#2-objectives)
3. [Lab Environment](#3-lab-environment)
4. [Prerequisites](#4-prerequisites)
5. [Create a GitHub Account](#5-create-a-github-account)
6. [Create the GitHub Repository](#6-create-the-github-repository)
7. [Install VirtualBox](#7-install-virtualbox)
8. [Set Up Kali Linux](#8-set-up-kali-linux)
9. [Create a NAT Network](#9-create-a-nat-network)
10. [Configure Kali Network Adapter](#10-configure-kali-network-adapter)
11. [Start Kali Linux](#11-start-kali-linux)
12. [Check the Network Interface](#12-check-the-network-interface)
13. [Configure the Static IP](#13-configure-the-static-ip)
14. [Configure the Default Gateway](#14-configure-the-default-gateway)
15. [Verify the Routing Table](#15-verify-the-routing-table)
16. [Test Gateway Connectivity](#16-test-gateway-connectivity)
17. [Test Internet Connectivity](#17-test-internet-connectivity)
18. [Test DNS Resolution](#18-test-dns-resolution)
19. [Final Network Configuration](#19-final-network-configuration)
20. [Evidence and Screenshots](#20-evidence-and-screenshots)
21. [Troubleshooting](#21-troubleshooting)
22. [Conclusion](#22-conclusion)

---

# 1. About the Lab

This lab demonstrates the basic network configuration of a Kali Linux virtual machine using Oracle VirtualBox.

The virtual machine is connected through a NAT Network and configured with a static IPv4 address. The default gateway is then configured, followed by connectivity tests to verify communication with the gateway, Internet, and DNS services.

---

# 2. Objectives

The main objectives of this lab are:

* Create and configure a GitHub repository for documenting the lab.
* Set up Kali Linux in a virtual environment.
* Create a NAT Network in VirtualBox.
* Configure the Kali Linux network interface.
* Assign a static IPv4 address.
* Configure the default gateway.
* Verify the routing table.
* Test gateway connectivity.
* Test Internet connectivity.
* Verify DNS resolution.
* Document the configuration and results.

---

# 3. Lab Environment

| Component         | Configuration     |
| ----------------- | ----------------- |
| Operating System  | Kali Linux        |
| Virtualization    | Oracle VirtualBox |
| Network Mode      | NAT Network       |
| Network Interface | eth0              |
| IP Address        | 10.0.0.2          |
| Subnet Mask       | 255.255.255.0     |
| Default Gateway   | 10.0.0.1          |
| Internet Test     | 8.8.8.8           |
| DNS Test          | google.com        |

---

# 4. Prerequisites

Before starting the lab, the following are required:

* A computer with Internet access
* Oracle VirtualBox
* Kali Linux virtual machine
* GitHub account
* Basic Linux terminal knowledge

---

# 5. Create a GitHub Account

1. Open GitHub.
2. Select **Sign Up**.
3. Enter the required account details.
4. Verify the email address.
5. Log in to the newly created GitHub account.

The GitHub account is used to store and document the practical lab work.

---

# 6. Create the GitHub Repository

1. Log in to GitHub.
2. Click **New Repository**.
3. Enter a suitable repository name.

Example:

```text
kali-linux-network-lab
```

4. Add a short repository description.
5. Select the required repository visibility.
6. Select **Add a README file**.
7. Click **Create Repository**.

The README file will contain the complete documentation of the practical work.

---

# 7. Install VirtualBox

1. Download and install Oracle VirtualBox.
2. Open VirtualBox after installation.
3. Verify that VirtualBox starts correctly.
4. Make sure the Kali Linux virtual machine is available.

---

# 8. Set Up Kali Linux

1. Open Oracle VirtualBox.
2. Select the Kali Linux virtual machine.
3. Check the virtual machine settings.
4. Verify the network adapter configuration.
5. Start the Kali Linux virtual machine.

---

# 9. Create a NAT Network

A NAT Network allows virtual machines to communicate with each other while providing access to external networks through Network Address Translation.

### Steps

1. Open **VirtualBox**.
2. Open **Tools → Network Manager**.
3. Select **NAT Networks**.
4. Create a new NAT Network.
5. Configure the required network range.
6. Enable DHCP if required by the lab.
7. Save the configuration.

For this lab, the network uses:

```text
Network: 10.0.0.0/24
Gateway: 10.0.0.1
```

---

# 10. Configure Kali Network Adapter

Open the Kali Linux VM settings:

**Settings → Network → Adapter 1**

Configure:

```text
Attached to: NAT Network
Name: <Created NAT Network>
```

Make sure the network adapter is enabled.

Save the settings.

---

# 11. Start

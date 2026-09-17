# Kali Linux Network Configuration Lab

## 1. Create a GitHub Account

1. Open GitHub and create a new account.
2. Verify the email address.
3. Log in to the GitHub account.

## 2. Create a GitHub Repository

1. Click **New Repository**.
2. Enter a suitable repository name.
3. Select **Public** or **Private** as required.
4. Initialize the repository with a **README.md** file.
5. Click **Create Repository**.

## 3. Install and Set Up VirtualBox

1. Install Oracle VirtualBox.
2. Open VirtualBox.
3. Create or import the **Kali Linux Virtual Machine**.
4. Start the Kali Linux VM.

## 4. Configure NAT Network

1. Open **VirtualBox → Tools → Network Manager**.
2. Create a new **NAT Network**.
3. Configure the network according to the lab requirements.
4. Enable **DHCP** if required.
5. Attach the Kali VM's network adapter to the created NAT Network.

## 5. Log in to Kali Linux

1. Start the Kali Linux VM.
2. Log in using the configured user account.
3. Open the Terminal.

## 6. Check the Network Interface

Run:

```bash
ifconfig
```

Identify the `eth0` network interface.

## 7. Configure the Static IP Address

Assign the required IP address:

```bash
sudo ifconfig eth0 10.0.0.2 netmask 255.255.255.0
```

Verify:

```bash
ifconfig eth0
```

The interface should show:

```text
inet 10.0.0.2
```

## 8. Configure the Default Gateway

Set the gateway:

```bash
sudo route add default gw 10.0.0.1
```

Verify the routing table:

```bash
route -n
```

The default route should point to:

```text
10.0.0.1
```

## 9. Test Gateway Connectivity

Run:

```bash
ping -c 4 10.0.0.1
```

Successful replies confirm connectivity between Kali Linux and the gateway.

## 10. Test Internet Connectivity

Run:

```bash
ping -c 4 8.8.8.8
```

Successful replies confirm Internet connectivity.

## 11. Test DNS Resolution

Run:

```bash
ping -c 4 google.com
```

Successful replies confirm that DNS resolution is working.

## 12. Final Verification

The completed configuration is:

| Configuration         | Value         |
| --------------------- | ------------- |
| Interface             | eth0          |
| IP Address            | 10.0.0.2      |
| Subnet Mask           | 255.255.255.0 |
| Default Gateway       | 10.0.0.1      |
| Gateway Connectivity  | Successful    |
| Internet Connectivity | Successful    |
| DNS Resolution        | Successful    |

All connectivity tests completed with **0% packet loss**.

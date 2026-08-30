# Getting Started with Linux Networking

## Learning Objectives

The learning objective is to gain knowledge on:

* becoming familiar with **Linux networking**.
* understanding basic **Linux networking commands**.
* understanding network interface configuration.
* understanding basic network connectivity and troubleshooting commands.
* understanding routing and network diagnostic tools.
* understanding basic DNS lookup functionality.

---

## About the Course

Linux networking is a broad field that encompasses various network-related tasks and technologies.

The course covers:

* Linux networking fundamentals.
* Network configuration and management.
* Network troubleshooting.
* Network interfaces.
* IP addresses.
* `ifconfig`.
* `ip`.
* `ifup`.
* `ifdown`.
* `ifquery`.
* `ethtool`.
* LAN and WAN.
* `ping`.
* `traceroute`.
* `mtr`.
* `route`.
* `nmcli`.
* `netstat`.
* `nmap`.
* `nslookup`.
* Network performance analysis.
* Network service debugging.
* DNS resource-record lookup.

Linux provides flexibility, stability, and support for a wide range of networking protocols, making it suitable for both personal and professional networking needs.

---

# Linux Networking Commands

Linux provides a set of networking and troubleshooting commands that can be used to:

* Configure network interfaces.
* Display network information.
* Test connectivity.
* Examine routing.
* Troubleshoot network problems.
* Analyze network performance.
* Inspect network services.
* Interact with DNS servers.

---

# Network Interfaces

A **network interface** provides a way for a Linux system to communicate over a network.

The course demonstrates the IP addresses associated with network interfaces, including:

* Loopback interface.
* LAN/network interface.

Network interfaces can be configured, activated, disabled, and queried using different Linux networking commands.

---

# `ifconfig` Command

The `ifconfig` command is used for configuring and displaying information about network interfaces.

It can be used to:

* Display network interface information.
* Assign an IP address.
* Activate an interface.
* Disable an interface.
* Configure network interfaces.

The command provides information about the network interfaces configured on a Linux system.

---

# `ip` Command

The **`ip` command** is a useful command-line tool for displaying and modifying:

* Routing information.
* Network devices.
* Network interfaces.
* IP addresses.

It is a modern replacement/substitute for several traditional networking tasks.

---

## Displaying IP Address Information

The `ip` command can be used to display the IP address and other information associated with a network interface.

For example:

```bash
ip addr
```

This provides information about network interfaces and their configured addresses.

---

# `ifup` Command

The `ifup` command is used to bring a network interface **up**.

Bringing an interface up makes it available for:

* Data transmission.
* Data reception.

Conceptually:

```text
ifup
 ↓
Enable network interface
 ↓
Allow data transmission and reception
```

---

# `ifdown` Command

The `ifdown` command is used to disable a network interface.

When an interface is brought down, it is stopped from:

* Sending data.
* Receiving data.

Conceptually:

```text
ifdown
 ↓
Disable network interface
 ↓
Stop data transmission and reception
```

---

# `ifquery` Command

The `ifquery` command can be used to query the **current configuration of network interfaces**.

It helps determine how a network interface is configured.

---

# `ethtool` Command

`ethtool` is a command-line tool used to inspect and modify settings associated with:

* Device drivers.
* Network interface controllers.

It can be used to view parameters of network interfaces.

Example:

```bash
ethtool interface
```

The course demonstrates using `ethtool` to view network-interface parameters.

---

# LAN and WAN

The course introduces two common network types:

## LAN

**LAN** stands for:

```text
Local Area Network
```

A LAN connects systems within a relatively local area.

---

## WAN

**WAN** stands for:

```text
Wide Area Network
```

A WAN connects systems across larger geographical areas.

---

# `ping` Command

The **`ping`** command is used to test connectivity between two systems.

`ping` stands for:

```text
Packet Internet Groper
```

It communicates with network nodes using:

```text
ICMP
```

ICMP stands for:

```text
Internet Control Message Protocol
```

The `ping` command is useful for determining whether a destination system is reachable over a network.

---

# `traceroute` Command

The **`traceroute`** command is used to trace the route from a local system to another network system.

It displays the path taken by packets toward the destination.

The command can show:

* The route to the destination.
* The number of hops.
* Intermediate network devices encountered along the route.

Conceptually:

```text
Local System
     ↓
   Hop 1
     ↓
   Hop 2
     ↓
   Hop 3
     ↓
Destination Server
```

This makes `traceroute` useful for network troubleshooting.

---

# `mtr` Command

**MTR** is a network diagnostic tool that combines the functionality of:

* `ping`
* `traceroute`

MTR stands for **My Traceroute**.

It is a contemporary command-line network diagnostic tool.

By default, its output is updated in **real time**.

The program continues running until it is terminated.

The course indicates that the **`q` key** can be pressed to quit the program.

---

# `route` Command

The `route` command is a command-line tool used for viewing or modifying the **IP routing table** on Linux systems.

It can be used to view routing information and configure static routes.

Static routes to particular:

* Hosts.
* Networks.

can be configured through a specified interface.

---

## Viewing the Routing Table

The routing table can be displayed using:

```bash
route
```

The command displays the **kernel IP routing table**.

---

# `nmcli` Command

**`nmcli`** is a simple-to-use command-line tool for managing network connections.

It can also be used to control the **NetworkManager** in relation to the Linux networking subsystem.

It provides command-line control over network connections and NetworkManager functionality.

---

# `netstat` Command

The `netstat` command is a command-line network utility.

It can display information such as:

* Network connections.
* Routing tables.
* Network interface statistics.
* Other network-related information.

It is useful for:

* Network performance analysis.
* Network troubleshooting.
* Network service debugging.

---

## Viewing Listening Ports

`netstat` can be used to identify applications that are **listening on network ports**.

This is particularly useful when debugging network services.

It allows users to determine which applications are listening on which ports.

The course provides an example command for displaying **TCP ports that are listening**, together with the applications using them.

---

# `nmap` Command

**Nmap**, or **Network Mapper**, is a powerful and flexible network tool.

It can be used to:

* Collect information about a single host.
* Investigate an entire network.
* Perform network port scanning.
* Scan ports on remote hosts.
* Perform security checks.

Nmap is useful for network discovery and network security analysis.

---

# `nslookup` Command

**`nslookup`** is a command-line tool used to interact with **DNS servers**.

It can be used to:

* Look up DNS resource records.
* Query DNS information.
* Discover information associated with domain names and IP addresses.

DNS lookup functionality allows users to obtain information such as the IP address associated with a domain.

---

# DNS

**DNS** is used to resolve domain names and provide corresponding network information.

The `nslookup` command can interact with DNS servers to retrieve resource records.

For example, DNS lookup can be used to discover an **IP address** associated with a domain name.

---

# Network Troubleshooting

Linux networking commands provide different ways to troubleshoot network problems.

A basic troubleshooting workflow can involve:

```text
Network Interface
       ↓
   IP Address
       ↓
     ping
       ↓
  traceroute / mtr
       ↓
 Routing Information
       ↓
 Listening Services
       ↓
      DNS
```

Different commands provide different types of network information.

---

# Network Command Summary

| Command      | Main Purpose                                                                                   |
| ------------ | ---------------------------------------------------------------------------------------------- |
| `ifconfig`   | Configure and display network interfaces                                                       |
| `ip`         | Display and modify network devices, interfaces, addresses, and routing                         |
| `ifup`       | Enable a network interface                                                                     |
| `ifdown`     | Disable a network interface                                                                    |
| `ifquery`    | Query network-interface configuration                                                          |
| `ethtool`    | Inspect and modify network-interface/device-driver settings                                    |
| `ping`       | Test network connectivity                                                                      |
| `traceroute` | Trace the route to a destination                                                               |
| `mtr`        | Combine ping and traceroute functionality                                                      |
| `route`      | View or modify the IP routing table                                                            |
| `nmcli`      | Manage network connections through NetworkManager                                              |
| `netstat`    | Display network connections, routing information, interface statistics, and listening services |
| `nmap`       | Network discovery, port scanning, and security checks                                          |
| `nslookup`   | Query DNS servers and DNS resource records                                                     |

---

# Course Completion

After completing the course, the learner should now be able to:

* Become familiar with **Linux networking**.
* Understand basic Linux networking commands.
* Understand network-interface configuration.
* Display IP-address information.
* Enable and disable network interfaces.
* Query network-interface configuration.
* Inspect network-interface parameters.
* Test connectivity using `ping`.
* Trace network paths using `traceroute`.
* Use `mtr` for network diagnostics.
* View and modify routing information.
* Manage network connections using `nmcli`.
* Analyze network connections and listening services using `netstat`.
* Understand basic uses of `nmap`.
* Perform DNS lookups using `nslookup`.

---

# Assessment

The course concludes with an assessment to check the learner's knowledge.

The required passing score is:

```text
80%
```

If the learner is ready, they can proceed to the assessment.

If the learner is not ready, they can select the option to **retake/review the course** before attempting the assessment again.

---

# Course Summary

The key concepts covered in this course are:

* Linux provides a broad set of networking and troubleshooting capabilities.
* `ifconfig` can be used to configure and display network interfaces.
* `ip` is used to display and modify network devices, interfaces, addresses, and routing information.
* `ifup` enables a network interface.
* `ifdown` disables a network interface.
* `ifquery` queries the current configuration of network interfaces.
* `ethtool` can inspect and modify device-driver and network-interface-controller settings.
* **LAN** stands for Local Area Network.
* **WAN** stands for Wide Area Network.
* `ping` is used to test connectivity between systems.
* `ping` communicates using **ICMP**.
* `traceroute` traces the route from a local system to a destination.
* `mtr` combines `ping` and `traceroute` functionality.
* `route` can be used to view or modify the Linux IP routing table.
* `nmcli` provides command-line management of network connections and NetworkManager.
* `netstat` displays network connections, routing tables, interface statistics, and other network information.
* `netstat` can help identify applications listening on network ports.
* `nmap` is used for network discovery, port scanning, and security checks.
* `nslookup` is used to interact with DNS servers and retrieve DNS resource records.
* DNS can be used to discover the IP address associated with a domain.
* Linux networking commands are useful for network configuration, troubleshooting, diagnostics, and analysis.
* The course requires **80%** to pass the final assessment.

---

## Course Files

```text
Track10-Linux-Networking/
├── lecture.md
├── assessment.md
└── Certificate.pdf
```

# networkwalks-B082-week1-Cybersecurity-labsetup
# 🔐 Cybersecurity Lab Setup

A hands-on cybersecurity lab environment built using VirtualBox and Kali Linux for practicing cybersecurity, networking, ethical hacking, and security analysis in a controlled environment.

## 🎯 Objectives

- Set up a practical cybersecurity laboratory.
- Configure VirtualBox networking.
- Create a custom NAT Network.
- Configure Kali Linux networking.
- Verify network connectivity.
- Create VM snapshots for safe lab experimentation.
- Prepare the environment for future cybersecurity and SOC practice.

## 🛠️ Lab Environment

| Component      | Configuration     |
|----------------|-------------------|
| Hypervisor     | Oracle VirtualBox |
| Security VM    | Kali Linux        |
| Network Type   | NAT Network       |
| Network Name   | NatNetwork        |
| Network CIDR   | 10.0.0.0/24       |
| Kali IP        | 10.0.0.2/24       |
| Gateway        | 10.0.0.1          |
| DHCP           | Enabled           |
| IPv6           | Disabled          |

## 🌐 Lab Architecture

```text
                 HOST WINDOWS PC
                       │
                   VirtualBox
                       │
              ┌────────┴────────┐
              │    NatNetwork   │
              │   10.0.0.0/24   │
              └────────┬────────┘
                       │
                  ┌────┴────┐
                  │  Kali   │
                  │10.0.0.2 │
                  └─────────┘
🧪 Phase 1 — Kali Linux Lab Setup
1. VirtualBox NAT Network
A custom NAT Network named NatNetwork was created using the 10.0.0.0/24 network.
Network: 10.0.0.0/24
DHCP: Enabled
IPv6: Disabled
2. Kali Linux Network Configuration
Kali Linux was connected to the custom NatNetwork.
The assigned IPv4 address was:
10.0.0.2/24
3. Network Connectivity Testing
The network configuration was verified using ICMP ping tests.
Gateway Test
ping -c 4 10.0.0.1
Result:
4 packets transmitted
4 packets received
0% packet loss
Internet Connectivity Test
ping -c 4 8.8.8.8
Result:
4 packets transmitted
4 packets received
0% packet loss
4. VM Snapshot
A clean snapshot was created after successfully configuring and testing the Kali Linux environment.
Snapshot:
Kali-Clean-Network-Setup
📸 Evidence
Screenshots documenting the setup and verification will be added here.
📚 What I Learned
Through this lab setup, I gained practical experience with:
Virtual machines
VirtualBox networking
NAT Networks
IPv4 addressing
/24 subnet configuration
Gateway connectivity
Network connectivity testing
Kali Linux networking
VM snapshots
Cybersecurity lab documentation
🚀 Future Work
The lab will be expanded with additional virtual machines and practical cybersecurity exercises, including:
Windows VM setup
Kali-to-Windows connectivity
Network traffic analysis
Wireshark
Nmap
Windows Event Log analysis
Linux log analysis
Security monitoring
Incident investigation
SOC Analyst practice labs
⚠️ Ethical Use
This laboratory is intended for authorized cybersecurity learning and experimentation in a controlled environment.
All security testing should only be performed against systems for which permission has been obtained.
📌 Project Status
Phase 1 — Completed ✅
[x] VirtualBox setup
[x] NAT Network configuration
[x] Kali Linux setup
[x] Kali IP configuration
[x] Gateway connectivity test
[x] Internet connectivity test
[x] Kali VM snapshot
Phase 2 — Upcoming 🚧
[ ] Windows VM setup
[ ] Windows network configuration
[ ] Kali ↔ Windows connectivity
[ ] Additional cybersecurity exercises

# Day 1 — Building the Home Lab

**Date:** 11 August 2026
**Goal:** Get three virtual machines running and networked — one attacker box and two targets.

---

## Why a virtual lab

Everything I practise from here on needs a machine I am allowed to attack. Scanning or exploiting anything I do not own is illegal, so the whole lab lives inside my own laptop as virtual machines. If I break something, I roll back a snapshot instead of rebuilding my actual computer.

## Choosing the hypervisor

There are two common free options:

1. **VirtualBox** — free and open source
2. **VMware Workstation Pro** — now free for personal use

The training plan I am following suggested VirtualBox, but I went with **VMware Workstation Pro**. Both work fine for this; I found VMware's networking configuration easier to understand as a beginner, and performance on my machine was better. Worth noting so anyone reading this knows the difference is deliberate, not an accident.

## The three machines

| VM | Role | Notes |
|---|---|---|
| Kali Linux | Attacker | Comes with most offensive tooling preinstalled |
| Ubuntu Server | Target | Linux target, and where I will practise log analysis |
| Windows 10 Enterprise (Evaluation) | Target | Windows target — Event Viewer, later Active Directory |

---

## 1. Kali Linux

Kali's download page offers several formats. The important thing: **there is a prebuilt virtual machine image as well as an installer ISO.**

- If you download the **prebuilt VMware image**, you do not install anything. Extract the archive and open the `.vmx` file in VMware — the machine is already built.
- If you download the **installer ISO**, you create a new VM and install Kali from scratch, the same way you would install any OS.

The prebuilt image is faster to get running. The default credentials on it are `kali` / `kali`.

**Change the default password immediately:**

```bash
passwd
```

This changes the password for the account you are currently logged in as. That is the correct command for this job.

**A separate thing** — if you want an *additional* user account:

```bash
sudo adduser <username>
```

`sudo` runs the command with administrative privileges. Creating users modifies system files that a normal user cannot touch, which is why it is needed here. These are two different tasks and I confused them at first (see Mistakes below).

## 2. Ubuntu Server

Download the ISO from ubuntu.com. In VMware: **Create a New Virtual Machine → select the ISO → configure resources.**

What I allocated:

- RAM: 2 GB
- Processors: 2 cores
- Disk: 25 GB
- Network: see the networking section below

The installer walks you through language, keyboard, disk partitioning, and then asks you to create a user account. That account is your login. Installation takes a while — leave it running.

## 3. Windows 10 Enterprise

Microsoft publishes a free **90-day evaluation** of Windows 10 Enterprise. Download the ISO, then the process is identical to Ubuntu: new VM, point it at the ISO, allocate resources, install.

When it asks for a **product key, leave it blank** — the evaluation edition does not need one. Give it more resources than the Linux VMs (4 GB RAM if you can spare it); Windows is heavier.

---

## Networking — the part that actually matters

Every VM gets **two network adapters**, and understanding the difference between them is the whole point of this step.

**NAT**
The VM shares my laptop's internet connection. It can reach the internet — updates, downloads, TryHackMe. It sits behind my host machine like a device behind a home router.

**Host-only**
A private network between the VMs and my host machine, with **no route to the internet**. The VMs can see each other here.

**Why both?**

I use NAT when I need to install or update something. But when I run a scan or an exploit against Ubuntu or Windows, I switch to **host-only** so the traffic stays inside the lab. That means:

- No accidental scanning of my home network or my ISP's equipment
- No malware sample reaching the internet
- The traffic I capture in Wireshark is only lab traffic, not my laptop's background noise

**One caveat I learned:** host-only still lets the VMs reach my *host machine*. If I want the lab fully sealed off from my laptop too, VMware calls that a **LAN Segment** (VirtualBox calls it *Internal Network*). I will move to that once I start handling anything genuinely malicious.

---

## Snapshots

Before doing anything else, I took a snapshot of each VM in its clean state. If I break a machine badly — wrong permissions, broken package, failed configuration — I restore the snapshot instead of reinstalling for two hours.

This is not optional. Take the snapshot.

---

## Mistakes and things I got wrong

- **I thought `sudo adduser` was how you change the default Kali password.** It is not — that creates a *new* user and leaves the original `kali`/`kali` login intact and still weak. The correct command is `passwd`. Small distinction, but leaving a known default credential live on an internet-facing machine is exactly the misconfiguration I will be looking for in a SOC role.
- **I initially only added one adapter (NAT)** and then realised I had no safe way to run scans without touching my real network. Added host-only afterwards.

## Verification

- [x] All three VMs boot
- [x] Kali reaches the internet on NAT (`ping 8.8.8.8`)
- [x] Default Kali password changed
- [x] Clean snapshot taken on each VM
- [ ] Confirm all three VMs can ping each other on host-only — carrying to Day 2

## Commands used today

```bash
ip a          # show network interfaces and IP addresses
whoami        # show current user
pwd           # print working directory
passwd        # change current user's password
sudo adduser  # create a new user account
ping          # test connectivity
```

## Next

Day 2 — TCP vs UDP, the three-way handshake, common ports, and capturing my own traffic in Wireshark.

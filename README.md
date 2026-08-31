# Cybersecurity-home-lab
A Personal cybersecurity home lab built with VMware, Ubuntu and Kali Linux
## 🎯 Objectives

- Practice cybersecurity concepts in a controlled environment
- Improve Linux administration skills
- Understand virtual networking
- Perform security experiments
- Practice system hardening
- Document my learning journey

## 🖥️ Environment
- VMware
- Ubuntu
- Kali Linux

## 📚 Project Roadmap

1. Lab setup
2. Network configuration
3. Reconnaissance
4. Ubuntu hardening
5. Final documentation

## 🚧 Status
Project in progress.
## 🖥️ Virtual Machines

### Ubuntu

- VMware Workstation
- Network Adapter 1: NAT
- Network Adapter 2: VMnet1
- Private IP: `192.168.221.128/24`

### Kali Linux

- VMware Workstation
- Network Adapter 1: NAT
- Network Adapter 2: VMnet1
- Private IP: `192.168.221.129/24`

## 🔗 Connectivity Test

From Kali Linux:

```bash
ping -c 4 192.168.221.128 RESULT: 4 packets transmitted, 4 received, 0% packet loss

## 🔎 Reconnaissance réseau avec Nmap

Depuis Kali Linux, un premier scan de la machine Ubuntu a été réalisé :

```bash
nmap 192.168.221.128

Résultat initial :

* Hôte actif
* 1000 ports TCP courants fermés

Un serveur SSH a ensuite été installé sur Ubuntu : 
sudo apt install openssh-server

Le service SSH a été vérifié avec : 
sudo systemctl status ssh 

État : active (running)

Un nouveau scan depuis Kali a permis de détecter le service : 
22/tcp  open  ssh

Une détection de version a ensuite été réalisée :
nmap -sV -p 22 192.168.221.128
